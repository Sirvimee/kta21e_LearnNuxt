<template>
    <div>
        <div v-if="hasConnection" class="notification is-primary">
            You have a connection
        </div>
        <div v-if="!hasConnection" class="notification is-danger">
            You don't have connection
        </div>
    </div>
</template>
    
<script>
export default {
    mounted() {
        if (process.client) {
            // console.log(this);
            // let updateConnectionStatus = () => {
            //     console.log(this);
            //     console.log(navigator.connection);
            //     this.hasConnection = navigator.connection.downlink > 0;
            // }
            // navigator.connection.addEventListener('change', updateConnectionStatus);
            window.addEventListener('online', () => this.hasConnection = true);
            window.addEventListener('offline', () => this.hasConnection = false);
        }
    },
    data() {
        return {
            hasConnection: true
        }
    }
}
</script>
    
<style>

</style>