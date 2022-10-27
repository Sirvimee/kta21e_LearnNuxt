<template>
    <button class="button is-primary" @click="copy()">Copy to Clipboard</button>
</template>
  
<script>
export default {
    methods: {
        copy() {
            navigator.clipboard.writeText("<empty clipboard>").then(() => {

            });
        }
    }
}
</script>
  
<style>

</style>