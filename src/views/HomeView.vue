<template>
  <div id="app">
    <nav>
      <router-link to="/home">Home</router-link> | 
      <router-link to="/carrito">Carrito</router-link> | 
      <router-link to="/signup">Registrarse</router-link> | 
      <router-link to="/">Salir</router-link>
    </nav>
        <div class="container">
          <h1>Productos</h1>
            <div class="row row-cols-1 row-cols-md-3" >
              <div class="col mb-4" style="margin-top: 50px" v-for="product in products" :key="product.id">
                  <div class="card h-100 shadow p-3 mb-5 bg-white rounded" style="margin-bottom: 0">
                      <img :src="product.picture" class="card-img-top" :style="product.estilo" />
                      <div class="card-body">
                          <h5 class="card-title">{{product.title}}</h5>
                          <h5 class="card-title" style="position: absolute; bottom: 45px; left: 40%; font-weight: bold">{{product.price | formatPrecio}}</h5>
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
    name: 'HomeView',
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

  h1{
  margin: 30px 0px 0px 0px;
  font-size: 30px;
  font-weight: bold;
}
</style>