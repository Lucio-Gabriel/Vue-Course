<template>
    <div>
        <h1>Olá VUE</h1>
        <p>Meu nome é: {{ name }}</p>
        <p>Profissão: {{ profession }}</p>
        <p>Idade: {{ age }}</p>
    </div>
</template>

<script>
    export default {
        name: 'FirstComponent',
        data() {
            return { 
                name: "Lucio Azevedo",
                profession: "Desenvolvedor de Software",
                age: 22
            }
        }
    }
</script>