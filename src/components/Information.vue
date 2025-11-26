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
    </div>
</template>

<script>
    export default {
        name: "Information",
        data() {
            return {
                in_work: true, 
                view_email: true,
                email: 'lucioazevedo0405@gmail.com'
            }
        }
    }
</script>