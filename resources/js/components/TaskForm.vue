<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">TaskForm Component</div>

                    <div class="card-body">
                        <form @submit.prevent="addPost" class="form">
                          <div class="form-group">
                            <input type="text" v-model="title" placeholder="Enter Title" class="form-control">
                          </div>
                          <div class="form-group">
                            <input type="submit" value="Submit" class="btn btn-primary form-control m-2">
                          </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
      data(){
        return {
          title: '',
        }
      },

      methods: {
        addPost(){
          axios.post('./api/posts', this.title).then((response) => {
            console.log(response)
            this.title = '';
          }).catch(error => {
            console.error("something wrong happened");
          })
        }
      },

      mounted() {
          console.log('Component mounted.')
      }
    }
</script>

<style scoped>
.container{
  margin-top: 20px;
}
</style>