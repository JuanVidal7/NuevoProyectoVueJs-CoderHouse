<!-- <template>
  <div>
      <h1>
          Fetch Api
      </h1>

      <div v-for="post in posts" :key="post.id" >
          <h2>{{post.id}} - {{post.title}}</h2>
          <p>{{post.body}}</p>

      </div>
  </div>
</template>

<script>
export default {
    name: 'FetchApi',

    data(){
        return{
            posts: []
        }
    },

    created(){
        let url = 'https://jsonplaceholder.typicode.com/posts';

        fetch(url)
        .then(response => response.json())
        .then(data => this.posts = data)
    }   
}
</script>

<style>

</style> -->

<!-- 
<template>
  <div>
      <h1>
          Imágenes
      </h1>

    <div v-for="image in images" :key="image.id" >
          <h2>{{image.id}} - {{image.title}}</h2>
          <img :src="image.thumbnailUrl" alt="">
      </div>

  </div>
</template>

<script>
import axios from 'axios'

export default {
    name: 'AxiosImage',

    data(){
        return{
            images: []
        }
    },

    async created(){
        let url = 'https://jsonplaceholder.typicode.com/photos';

        await axios.get(url).then((response) => (this.images = response.data))
    }

}
</script>

<style>

</style> -->

<template>
  <div id="app">
        <div class="container">
          <div class="row row-cols-1 row-cols-md-3" >
            <div class="col mb-4" style="margin-top: 50px" v-for="product in products" :key="product.id">
                <div class="card h-100 shadow p-3 mb-5 bg-white rounded" style="margin-bottom: 0">
                    <img src="" class="card-img-top" style="product.estilo" />
                    <div class="card-body">
                        <h5 class="card-title">{{product.title}}</h5>
                        <h5 class="card-title" style="position: absolute; bottom: 45px; left: 40%; font-weight: bold">{{product.price}}</h5>
                        <div class="container-fluid">
                            <div style=" display: flex; justifyContent: center ">
                                <button class="botonAgregarCarrito" style="position: absolute; bottom: 0; width: 100%; border-radius: 0">Ver Detalle</button>
                            </div>
                        </div>
                    </div>
                </div>
              </div>
          </div>
        </div>
  </div>
</template>

<script>
import productsData from "./productos.json";

export default {
  data() {
    return {
      products: productsData,
    };
  },
};
</script>

<style scoped>
  .botonAgregarCarrito{
    width: 401px; 
    font-size: 15px; 
    background-color: #c47500; 
    color: white; 
    padding-top: 5px; 
    padding-bottom: 5px; 
    border: 1px solid #c47500;
    border-radius: 5px; 
    outline: none; 
    cursor: pointer; 
    letter-spacing: 2px;
    font-family: 'Poppins';
  }

  .botonAgregarCarrito:focus{
    outline: none;
  }
</style>