<template>
  <div>
    <h2 class="text-success">Homework Components</h2>
    
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <div class="card mb-3" v-for="(item,i) in info" :key="i">
            <div class="row no-gutters">
              <div class="col-md-4">
                <img :src="item.item_photo" class="card-img" alt="...">
              </div>
              <div class="col-md-8">
                <div class="card-body">
                <h5 class="card-title">Code: {{item.item_codeno}}</h5>
                  <h5 class="card-title">Name: {{item.item_name}}</h5>
                  <p class="card-text">Price: {{item.item_price}} Ks</p>
                  <p class="card-text">{{item.brand.brand_name}}</p>
                  <p class="card-text">{{item.subcategory.subcategory_name}}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
      
        

  </div>
</template>

<script type="text/javascript">
  export default {
    name: 'Homework',
    data(){
      return {
        loading: true,
        error: false,
        info: null
      }
    },
    mounted(){
      this.getData();
    },
    methods:{
      getData(){
        this.$http.get('http://jetpackmall.shwesinwin.me/api/items')
                .then(res=>{
                  console.log(res);
                  this.info = res.data.data;
                })
                .catch(err=>{
                  this.error = true;
                  console.log(err);
                })
                .finally(()=>{
                  this.loading = false;
                })
      }
    }
  }
</script>

<style type="text/css">
  
</style>