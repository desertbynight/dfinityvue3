<template>
    <div>
        <h1>Hello World!</h1>
        <TestComponent />
    </div>
</template>

<script>
import { dfinityvue3 } from '../../declarations/dfinityvue3';

import TestComponent from './components/TestComponent.vue';

export default {
    components: {
        TestComponent
    },

    async mounted() {
        const greeting= await dfinityvue3.greet();
        console.log(greeting);
    }
}
</script>
