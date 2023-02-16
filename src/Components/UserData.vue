<template>
    <form @submit.prevent="AddDetails">
        <div>
            <label>Name:</label>
            <input type="text" v-model="name">
        </div>
        <div>
            <label>Age:</label>
            <input type="text" v-model="age">
        </div>
        <button>Add User</button>
    </form>
</template>

<script>

export default{
    data(){
        return {
            name:'',
            age:'',
        }
    },
    methods:{
        AddDetails(){
            this.$emit('add-details',this.name,this.age);
        } 
    }
}

</script>