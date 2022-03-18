<template>
  <div>
    <h1>Listado de Productos</h1>
    <div class="tableProducts">
      <table class="col-md-6" :class="newClass">
        <thead class="thead-dark">
          <tr>
            <th scope="col">#</th>
            <th scope="col">Nombre</th>
            <th scope="col">Precio</th>
            <th scope="col">Descripcion</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th scope="row">1</th>
            <td>{{ nombre[0] }}</td>
            <td>{{ precio[0] | formatPrecio }}</td>
            <td>{{ descripcion[0] }}</td>
          </tr>
          <tr>
            <th scope="row">2</th>
            <td>{{ nombre[1] }}</td>
            <td>{{ precio[1] | formatPrecio }}</td>
            <td>{{ descripcion[1] }}</td>
          </tr>
          <tr>
            <th scope="row">3</th>
            <td>{{ nombre[2] }}</td>
            <td>{{ precio[2] | formatPrecio }}</td>
            <td>{{ descripcion[2] }}</td>
          </tr>
          <tr>
            <th scope="row">4</th>
            <td>{{ nombre[3] }}</td>
            <td>{{ precio[3] | formatPrecio }}</td>
            <td>{{ descripcion[3] }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  name: "MiComponente",
  data() {
    return {
      nombre: ['Hershey Blanca', 'Hershey Negra', 'M & M', 'Ferrero Rocher'],
      precio: [2500, 3000, 1500, 12000],
      descripcion: [`Cookies 'n' creme es una barrita de chocolate blanco con bits de galleta similares en sabor y textura a las Oreo.`, 
      `La barrita de chocolate con leche Hershey's, tiene un sabor único característico, amargo y picante. Esta es su variedad chocolate negro.`, 
      `Pequeños pedazos de chocolate con leche revestidos de azucar.`,
      `Los bombones están formados por una capa de barquillo rellena con pasta de cacao y avellanas, recubierta por una capa de chocolate con avellanas trituradas y una avellana entera en el interior, envueltos en papel metalizado y colocados individualmente sobre un molde de papel engrasado.`],
      newClass: 'table table-hover'
    }
  }
};
</script>

<style scoped>

.tableProducts {
  display: flex;
  justify-content: center;
}

h1{
  font-size: 30px;
  padding: 0px 0px 30px 0px;
  font-weight: bold;
}
</style>