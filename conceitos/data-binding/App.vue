<!-- Templates só podem ter um elemento root -->
<template>
    <div>
        <!-- Ao invés de ficar escrevendo v-bind:style, 
            posso substituir apenas por :style -->
        <h1 v-bind:style="{ textDecoration: decoration }">Fala ae {{ name }}</h1>
        <input v-model="name">
        <br>
        <a :href="link">Link para o curso</a>
    </div>
</template>

<script>
export default {
    data: () => ({
        name: 'Rafael',
        decoration: 'underline',
        link: 'https://treinamento.vuejsbrasil.org'
    })
}
</script>

<style>

</style>