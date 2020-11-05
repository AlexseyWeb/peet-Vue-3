<template>
    <div></div>
</template>






<script>
export default {
    data() {
        return {
            show: true
        }
    },
    methods: {
       toogleShow: function() {
           this.show = !this.show;
        }
    }
}

</script>






<style scoped>
p {
    margin-top: 50px;
}
</style>