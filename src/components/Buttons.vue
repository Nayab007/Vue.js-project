<template>
    
    <button class="button-62" @click="prev">Delete</button>
   <button class="button-62" @click="prev">Reply</button>
   <button class="button-62" @click="prev">Forward</button>

</template>

<script>


export default {
        name: 'message-api',
        data() {
            return{
                messages: null
                  
            }
                
            }
        }
</script>

<style scoped>
    .button-62 {
  background: linear-gradient(to bottom right, #ef4765, #ff9a5a);
  border: 0;
  border-radius: 12px;
  color: #ffffff;
  cursor: pointer;
  display: inline-block;
  font-size: 10px;
  line-height: 2.5;
  outline: transparent;
  padding: 0 1rem;
  text-align: center;
  text-decoration: none;
  transition: box-shadow 0.2s ease-in-out;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  white-space: nowrap;
}
</style>
