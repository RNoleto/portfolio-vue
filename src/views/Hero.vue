<script setup>
import TerminalCard from '../components/ui/TerminalCard.vue';
</script>

<template>
    <section class="overflow-hidde content-center">
        <h1 class="title">Construindo o futuro com código</h1>

        <TerminalCard
            :content="[
                'npm install @vue/cli -g',
                'vue create my-project',
                'cd my-project',
                'npm run serve',
            ]"
            buttonText="Criar projeto"
            @onButtonClick="() => window.open('https://cli.vuejs.org/')"
        />
    </section>
</template>

<style scoped></style>