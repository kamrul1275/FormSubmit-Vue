<template>
    <div>
        <h1>This is contact page</h1>
    </div>
</template>

<script>
export default {
    name: 'ContactView',

    data() {
        return {
            
        };
    },

    beforeCreate() {
        
        alert('before create');
    },
created() {
        
        alert('then create....... 2nd');
    },

    methods: {
        
    },
};
</script>

<style lang="scss" scoped>

</style>