<template>
    <div>
    <ul>
        <li v-for="goal in goals" :key="goal">
            <slot :item="goal" etcProp="..."></slot>
        </li>
    </ul>
</div>
</template>

<script>
export default {
    data(){
        return{
            goals:['Complete the sessions','Learn Vue'],
        }
    }
}
</script>
<style scoped>
div {
    margin: 2rem auto;
    max-width: 30rem;
    border-radius: 12px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
    padding: 1rem;
  }
  
</style>


