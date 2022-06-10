<template>
    <h5>Contador: {{ contador }} </h5>
</template>

<script>
import { inject } from '@vue/runtime-core'
export default {

    setup() {
        const contador = inject('contador');

        return { contador }
    }

}
</script>

<style>

</style>