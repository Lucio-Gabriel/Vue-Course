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
                view_email: true,
                email: 'lucioazevedo0405@gmail.com',
                my_link: 'https://google.com'
            }
        }
    }
</script>