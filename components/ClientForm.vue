<template>
    <form class="flex flex-col gap-4" @submit.prevent="submit">
        <div>
            <label for="Name">Nome</label>
            <input required class="w-full p-2 border rounded placeholder:text-gray-800 outline-none" type="text" id="name" v-model="form.name" placeholder="Insira seu nome" :class="invalid && form.name === '' ? 'border-red-500':'border-primary'">
        </div>

        <div>
            <label for="mail">Email</label>
            <input required class="w-full p-2 border rounded placeholder:text-gray-800 outline-none" type="mail" id="mail" v-model="form.email" placeholder="insira seu email" :class="invalid && form.email === '' ? 'border-red-500':'border-primary'">
        </div>

        <div>
            <label for="Phone">Telefone</label>
            <input required v-maska data-maska="(##) # ####-####" class="w-full p-2 border rounded placeholder:text-gray-800 outline-none" type="text" id="Phone" v-model="form.phone" placeholder="insira seu telefone" :class="invalid && form.phone === '' ? 'border-red-500':'border-primary'">
        </div>
        <div class="w-full flex justify-end py-2">
            <button type="submit" class="p-4 flex justify-center items-center bg-primary rounded text-white xs:w-full font-bold md:w-[200px] h-[50px] disabled:bg-primary/40" :disabled="form.email === '' || form.name === '' || form.phone === ''">
                <LoaderCircle class="animate-spin" :size="20" v-if="loading"/>
                <span v-else>Enviar</span>
            </button>
        </div>
    </form>


    <transition enter-active-class="animate__animated animate__fadeInRight" leave-active-class="animate__animated animate__fadeOutRight">
        <div class="fixed top-4 right-4 rounded-md shadow-md border border-white p-10 w-[300px]" :class="poupopStatus.type === 'success' ? 'bg-primary ' : 'bg-red-400'" v-if="poupopStatus.show">
            <button class="absolute top-2 right-2" @clearPoupop="clearPoupop">
                <X color="white" :size="25"/>
            </button>
            <div class="flex items-center justify-center gap-4">
                <MailCheck color="white" v-if="poupopStatus.type === 'success'"/>
                <MailWarning color="white" v-else/>
                <p class="text-white">{{ poupopStatus.message }}</p>
            </div>
        </div>
    </transition>
</template>

<script setup lang="ts">
import { LoaderCircle, MailCheck, MailWarning, X } from 'lucide-vue-next';

const apiURL = 'https://sunriseenergy.gdgestao.com.br/Consumidor/CadastrarProspeccaoCliente'

const form = reactive({
    name: '',
    email: '',
    phone: '',
})

const invalid = ref(false)

const poupopStatus = reactive({
    type: '',
    show: false,
    message: ''
})

const loading = ref(false)

const submit = async() => {
    if(form.name === '' || form.email === '' || form.phone === '') {
        poupopStatus.show = true
        poupopStatus.message = 'E necessário preencher todos os campos'
        poupopStatus.type = 'error'
        invalid.value = true
        return
    }

    const PC = {
        Nome: form.name,
        Email: form.email,
        Telefone: form.phone
    };

    const formData = new FormData();
    formData.append("PC.Nome", PC.Nome);
    formData.append("PC.Email", PC.Email);
    formData.append("PC.Telefone", PC.Telefone);

    invalid.value = false
    loading.value = true
    try {
        const response = await fetch(apiURL, {
            method: 'POST',
            body: formData
        })
        if (response.ok) {
            poupopStatus.show = true
            poupopStatus.message = 'Cadastro realizado com sucesso'
            poupopStatus.type = 'success'
            clearForm()
        }
    } catch (error) {
        poupopStatus.show = true
        poupopStatus.message = 'Erro ao realizar cadastro'
        poupopStatus.type = 'error'
    } finally {
        loading.value = false
        timeToClearPopoup()
    }
}

const clearPoupop = () => {
    poupopStatus.show = false
    poupopStatus.message = ''
    poupopStatus.type = ''
}

const timeToClearPopoup = () => {
    setTimeout(() => {
        poupopStatus.show = false
        poupopStatus.message = ''
        poupopStatus.type = ''
    }, 5000)
}

const clearForm = () => {
    form.name = ''
    form.email = ''
    form.phone = ''
}

</script>
