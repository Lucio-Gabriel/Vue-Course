<template>
    <img 
        :src="avatar" 
        :alt="description" 
    />
</template>

<script>
    export default {
        name: 'Picture',
        data() {
            return {
                avatar: "/img/vite.svg",
                description: "Lucio Azevedo"
            }
        }
    }
</script>