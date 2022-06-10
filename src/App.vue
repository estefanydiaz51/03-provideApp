<template>
    <h1>App contador: {{ contador }}</h1>
    <contador-uno></contador-uno>
    <contador-accion></contador-accion>
</template>

<script>
import ContadorAccion from './components/ContadorAccion'
import ContadorUno from './components/ContadorUno'
import { ref } from '@vue/reactivity'
import { provide } from '@vue/runtime-core';

export default {
    name: 'App',
    components: {
    ContadorAccion,
        ContadorUno,
    },
    setup() {
        const contador = ref(0);

        provide('contador', contador);

        return { contador }
    }
}
</script>

<style>

</style>
