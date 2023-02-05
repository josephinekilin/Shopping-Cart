<template>
  <div>
    <h1>All Products</h1>
      <table class="table is-striped">
        <thead>
          <tr>
            <th>Name</th>
            <th>Description</th>
            <th>Stock</th>
            <th>Price</th>
            <th></th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(list, index) in listdata" :key="index">
            <td >{{list.title}}</td>
            <td>{{list.description}}</td>
            <td>{{list.stock}}</td>
            <td>Rp.{{list.price}}</td>
            <td><button-form text="Add To Cart" color="blue" @emitClick="addToCart(list)"/></td>
          </tr>
        </tbody>
    </table>
  </div>
</template>
<script>
export default {
  props:{
        listdata:{
            type: Array,
            default: () => {
                return []
            }
        },
    },
    methods:{
        addToCart(list){
            console.log("masih belum tau cara mindahin isi arraynya :'(");
            alert("Added To Cart !")
        },
    }
}
</script>