<template>
    <div>
        <p v-if="in_work">Estou trabalhando no momento.</p>
        <p v-else>Estou em busca de novas oportunidades!</p>
        <p>Utilizo as seguintes tecnlogias:</p>
        <ul>
            <li>PHP</li>
            <li>Laravel</li>
            <li>Livewire</li>
        </ul>
        <div>
            <button @click="showEmail">{{ textBtn }}</button>
        </div>
        <p v-show="view_email">Mande uma mensagem para: {{ email }}</p>
        <p>Para acessar meu portifólio  
            <a v-bind:href="my_link" target="_blank">
                Basta clicar aqui
            </a>
        </p>

        <Picture />
    </div>
</template>

<script>
import Picture from './Picture.vue';

    export default {
        name: "Information",
        components: {
            Picture
        },
        data() {
            return {
                in_work: true, 
                view_email: false,
                email: 'lucioazevedo0405@gmail.com',
                my_link: 'https://google.com',
                textBtn: 'Mostrar E-mail'
            }
        },
        methods: {
             showEmail() {
                this.view_email = !this.view_email
                if(!this.view_email) {
                    this.textBtn = 'Mostrar E-mail'
                } else {
                    this.textBtn = 'Ocultar E-mail'
                }
             }
        }
    }
</script>