<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <hello-world msg="Welcome to Your Vue.js + TypeScript App"/>
  </div>
</template>

<script lang="ts">
import HelloWorld from '@/components/HelloWorld.vue'
import {defineComponent, ref} from "vue"; // @ is an alias to /src

export default defineComponent({
    components: {
        HelloWorld
    },
    props: {
        msg: String
    },
    setup() {
        const count = ref(0)
        const increase = () => {
            count.value++
        }

        return {
            count,
            increase,
        }
    }
});
</script>
