<template>
<div>
    <tabs :links="$router.options.routes" :current="$route.path"></tabs>
    <section class="section">
        <div class="container">
            <div class="content">
                <nuxt/>
            </div>
        </div>
    </section>  
</div>
</template>

<script>
import Tabs from '../components/Tabs.vue';
export default {
  components: { Tabs },

}
</script>

<style>

</style>