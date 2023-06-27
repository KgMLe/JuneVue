<template>
    <div>
        <div class="container">
            <div class="row">
                <div class="col" v-for="item in data" :key="item.ID"> 
                    <!-- this is for the key value pairs -->
                    <div class="class" style="width: 18rem">
                        <img :src="item.image" class="card-img-top" alt="..">
                        <div class="card-body">
                          <h1>{{ item.title }}</h1>
                          <h4>{{ item.price }}</h4>
                        </div> 
                    </div>
                </div>
            </div>
        </div>

    </div>
</template>

<script>
    export default {
        data() {
            return{
                data: []
            }
        },
        methods: {
        async fetchData(){
        const  res = await fetch ('https://codebeans2022.github.io/JSON-Server/data.json');
        let parsedData =  await res.json()
        this.data = parsedData.products
            }
        },
        mounted (){
            this.fetchData()
        }
    }
</script>

<style scoped>

</style>