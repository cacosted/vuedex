<template>
    <div class="table">
        
        <div class="item" v-for="profile in profilesData">
            <Profile :details="profile"/>
        </div>
            
    </div>
</template>

<script>
    import Profile from '@/components/Profile'

    export default {
        name: 'CardList',
        
        data() {
            return {
            }
        },

        props: {
            profilesData: Array,
        },

        components: {
            Profile,
        },

        methods: {
        },

    }
</script>

<style lang="scss" scoped>
    .table {
        display: grid;
        gap:5px;
        
        grid-template-columns: repeat(4,1fr);
    
        .item {
            background-color: white;
            border-radius: 6px ;
            overflow: hidden;
        }
    }
    
</style>
