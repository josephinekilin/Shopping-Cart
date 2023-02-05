<template>
  <div class="cart">
    <h1>Your Cart</h1>
    <p v-show="!cart.length">
      <i>Your cart is empty!</i>
    </p>
    <table class="table is-striped">
        <thead>
          <tr>
            <th>Name</th>
            <th>Description</th>
            <th>Price</th>
            <th>Action</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(cart, index) in cart" :key="index">
            <td>{{cart.title}}</td>
            <td>{{cart.description}}</td>
            <td>Rp.{{cart.price}}</td>
            <td><button-form text="Delete" color="red" @emitClick="deleteItem(index)"/></td>
          </tr>
        </tbody>
    </table>
    
  </div>
</template>
<script>
export default {
    props:['cart'],
    methods:{
        deleteItem(index){
            this.$emit('emitDelete', index)
        }
    },
}
</script>