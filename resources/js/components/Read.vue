<template>
  <div class="container-fluid">
    <div v-if="!show">
      <form>
        <div class="form-group">
          <label for="exampleInputEmail1">Email</label>
          <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">
          </div>
        <div class="form-group">
          <label for="exampleInputPassword1">Password</label>
          <input type="password" class="form-control" id="exampleInputPassword1">
        </div>
      </form>
      <button
        @click="clicked" 
        type="button"
        class="btn btn-primary btn-lg btn-block text-dark border-light"
        style="margin-top: 45px;
              background: linear-gradient(to left, #F37335, #FDC830);">
        Login
      </button>
      <button type="button" class="btn btn-link">Forgot password ?</button>
    </div>

    <div v-if="show">
      <div v-for="member in members" :key="members.name"
        class="card border-light shadow mt-4"
        style="border-radius: 20px;">
        <div class="row no-gutters">
          <div class="col-md-2 ml-4">
            <img
              :src="member.img"
              style="width: 100px; border-radius: 50%;"
              class="mt-2 mb-2 card-img"
              alt="img">
          </div>
          <div class="col-md-8">
            <div class="card-body">
              <h5 class="card-title font-weight-bold">{{ member.name }}</h5>
              <p class="card-text">{{ member.email }}</p>
            </div>
          </div>
        </div>
      </div>
      <button
        type="button"
        class="btn btn-primary btn-lg btn-block text-dark border-light"
        style="margin-top: 45px;
              background: linear-gradient(to left, #F37335, #FDC830);">
        Next
      </button>
    </div>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        members: [
          {
            name: 'John',
            email: 'adi@email.com',
            img: 'https://ucc.edu.gh/sites/default/files/default_images/img_avatar_0.png'
          },
          {
            name: 'Anna',
            email: 'ana@email.com',
            img: 'https://www.w3schools.com/howto/img_avatar2.png'
          },
          {
            name: 'Bella',
            email: 'bella@email.com',
            img: 'https://www.w3schools.com/howto/img_avatar2.png'
          },
          {
            name: 'Danny',
            email: 'adi@email.com',
            img: 'https://ucc.edu.gh/sites/default/files/default_images/img_avatar_0.png'
          },
          {
            name: 'Will',
            email: 'ana@email.com',
            img: 'https://ucc.edu.gh/sites/default/files/default_images/img_avatar_0.png'
          },
          {
            name: 'Zoe',
            email: 'bella@email.com',
            img: 'https://www.w3schools.com/howto/img_avatar2.png'
          }
        ],
        show: false
      }
    },
    mounted() {
      this.fetch()
    },
    methods: {
      fetch() {
        console.log('dbshdhs')
      },
      clicked() {
        this.show = true
      }
    }
  }
</script>