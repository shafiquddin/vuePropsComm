<template>
    <div>
        <h2>Manage User</h2>
        <input type="text" ref="name">
        <button @click="addName">Add</button>
        <teleport to="body">
        <error-alert v-if="inputIsInvalid">
            <h2>Error Alert!</h2>
            <h3>This is an Invalid Input</h3>
            <button @click="inputIsInvalid=false">Okey</button>
        </error-alert>
    </teleport>
    </div>
</template>
<script>
import ErrorAlert from './Model/ErrorAlert.vue';
export default {
    data(){
        return{
            inputIsInvalid:false,
        }
    },
  components: { ErrorAlert },
    methods:{
        addName(){
            const enteredValue=this.$refs.name.value;
            if(enteredValue===''){
                this.inputIsInvalid=true;
            }
        }
    }

}
</script>
<style scoped>

</style>