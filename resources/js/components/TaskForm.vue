<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">TaskForm Component</div>

                    <div class="card-body">
                        <form @submit.prevent="addTask">
                          <input type="text" name="title" placeholder="Enter Title" class="form-control">
                          <input type="submit" value="Submit" class="btn btn-primary form-control btn-sm d-inline-block p-2">
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
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