<template>
    <div>
        <h2>Manage User</h2>
        <input type="text" ref="name">
        <button @click="AddName">Add</button>
        <error-alert v-if="inputIsInvalid">
            <h2>Alert</h2>
            <p>This is invalid Input</p>
            <button @click="inputIsInvalid=false">Okey</button>
        </error-alert>
    </div>
</template>
<script>
import ErrorAlert from './ErrorAlert.vue';

export default {
    data(){
        return{
           inputIsInvalid:false, 
        }
    },
    components:{
        ErrorAlert,
    },
    methods:{
        AddName(){
            const enteredValue=this.$refs.name.value;
            if(enteredValue===''){
                this.inputIsInvalid=true;
            }
        }
    }
}
</script>