<template>
    <div class="hello container mt-5">
         <div class="input-group mb-5">
            <input type="text" class="form-control" placeholder="Please your word.." v-model="message" aria-label="Recipient's username" aria-describedby="button-addon2">
            <div class="input-group-append">
                <button class="btn btn-outline-primary" @click="submitMessage" type="button" id="button-addon2">Send</button>
            </div>
        </div>
        <div class="media my-3" v-for="item in messages">
            <img v-if="item.username != username" class="align-self-start mr-3" src="http://lorempixel.com/100/100/sports" alt="Generic placeholder image">
            <div class="media-body">
                <h5 class="mt-0">{{item.username}}</h5>
                <p>{{item.message}}</p>
            </div>
        <img v-if="item.username == username" class="ml-3" src="http://lorempixel.com/100/100/sports" alt="Generic placeholder image">
        </div>
       <!-- <div class="media">
            <div class="media-body">
                <h5 class="mt-0 mb-1">Media object</h5>
                Cras sit amet nibh libero, in gravida nulla. Nulla vel metus scelerisque ante sollicitudin. Cras purus odio, vestibulum in vulputate at, tempus viverra turpis. Fusce condimentum nunc ac nisi vulputate fringilla. Donec lacinia congue felis in faucibus.
            </div>
            <img class="ml-3" src="http://lorempixel.com/100/100/sports" alt="Generic placeholder image">
        </div> -->
    </div>
</template>

<script>
  export default {
      name:'item',
      data(){
          return {
              msg: 'welcome to Your Vue.js App',
              username:'JC Chin',
              message:'',
              messages:[{
                username:'JC Chin',
                message:'Hi sup!'
              },
              {
                  username:'Iron Man',
                  message:"Hey man! how's going?"
              }
              ]
          }
      },
      methods:{
          submitMessage(){ //equal to sumbitMessage: function (){}
            let vm = this
            vm.messages.unshift({ //let the message be put at front rahter than puting at last(by using 'push')
                username:vm.username,
                message: vm.message
            })
          }
      }
          
     
  }
</script>

<style>
</style>
