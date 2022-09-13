<template>

  <h2 class="Email">Messages</h2>

  
 
  <pre   v-if="messages?.conversationHistory">
    <h2 class=action>action:</h2>"{{ messages.conversationHistory[0].action }}"
    <h2 class=action>messageId:</h2>"{{ messages.conversationHistory[0].messageId }}"
    <h2 class=action>attachments:</h2>"{{ messages.conversationHistory[0].attachments }}"
    <h2 class=action>body:</h2>"{{ messages.conversationHistory[0].body }}"
    <h2 class=action>from:</h2>"{{ messages.conversationHistory[0].from }}"
    <h2 class=action>to:</h2>"{{ messages.conversationHistory[0].to }}"
    <h2 class=action>cc:</h2>"{{ messages.conversationHistory[0].cc }}"
    <h2 class=action>subject:</h2>"{{ messages.conversationHistory[0].subject }}"
    <h2 class=action>sent:</h2>"{{ messages.conversationHistory[0].sent }}"
  </pre> 
  <pre   v-if="messages?.conversationHistory">
    <h2 class=action>action:</h2>"{{ messages.conversationHistory[1].action }}"
    <h2 class=action>messageId:</h2>"{{ messages.conversationHistory[1].messageId }}"
    <h2 class=action>attachments:</h2>"{{ messages.conversationHistory[1].attachments }}"
    <h2 class=action>body:</h2>"{{ messages.conversationHistory[1].body }}"
    <h2 class=action>from:</h2>"{{ messages.conversationHistory[1].from }}"
    <h2 class=action>to:</h2>"{{ messages.conversationHistory[1].to }}"
    <h2 class=action>cc:</h2>"{{ messages.conversationHistory[1].cc }}"
    <h2 class=action>subject:</h2>"{{ messages.conversationHistory[1].subject }}"
    <h2 class=action>sent:</h2>"{{ messages.conversationHistory[1].sent }}"
  </pre> 
  <pre   v-if="messages?.conversationHistory">
    <h2 class=action>action:</h2>"{{ messages.conversationHistory[2].action }}"
    <h2 class=action>messageId:</h2>"{{ messages.conversationHistory[2].messageId }}"
    <h2 class=action>attachments:</h2>"{{ messages.conversationHistory[2].attachments }}"
    <h2 class=action>body:</h2>"{{ messages.conversationHistory[2].body }}"
    <h2 class=action>from:</h2>"{{ messages.conversationHistory[2].from }}"
    <h2 class=action>to:</h2>"{{ messages.conversationHistory[2].to }}"
    <h2 class=action>cc:</h2>"{{ messages.conversationHistory[2].cc }}"
    <h2 class=action>subject:</h2>"{{ messages.conversationHistory[2].subject }}"
    <h2 class=action>sent:</h2>"{{ messages.conversationHistory[2].sent }}"
  </pre> 
  <pre   v-if="messages?.conversationHistory">
    <h2 class=action>action:</h2>"{{ messages.conversationHistory[3].action }}"
    <h2 class=action>messageId:</h2>"{{ messages.conversationHistory[3].messageId }}"
    <h2 class=action>attachments:</h2>"{{ messages.conversationHistory[3].attachments }}"
    <h2 class=action>body:</h2>"{{ messages.conversationHistory[3].body }}"
    <h2 class=action>from:</h2>"{{ messages.conversationHistory[3].from }}"
    <h2 class=action>to:</h2>"{{ messages.conversationHistory[3].to }}"
    <h2 class=action>cc:</h2>"{{ messages.conversationHistory[3].cc }}"
    <h2 class=action>subject:</h2>"{{ messages.conversationHistory[3].subject }}"
    <h2 class=action>sent:</h2>"{{ messages.conversationHistory[3].sent }}"
  </pre> 
 
 
  
</template>
    
    <script>
    import axios from 'axios';
    
    
    export default {
        name: 'message-api',


  
        data(){
            return{
                messages: {
                  
                }
                
            }
        },
    
        created() {
            axios.get(`http://sa-test-task-2022.s3-website.eu-north-1.amazonaws.com/messages`)
                .then(response => {
                    // JSON responses are automatically parsed.
                    this.messages = response.data
                })
                .catch(e => {
                    this.errors.push(e)
                });
        },
        methods: {
            remove(id){
               this.$delete(this.conversationHistory, id);
            }
        }
    }
    </script>


    <style scoped>
      Chat {
        margin-left: 10vw;
        
        
      }
      .p {
  white-space: pre-line;
}

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

.action {
  position: relative;
  display: inline-flex;
  font-size: 16px;
  margin-left: -40vw;
  line-height: .5;
  text-align: center;
  word-spacing: 2rem;
 
}

    </style>