<template>
  <div class="container">
    <product-list :listdata="list" />
    <cart-list :cart="cart" @emitDelete="deleteItem" />
    <button-form text="Check Out" color="blue" @emitClick="payItem(cart)"/>
  </div>
</template>

<script>
export default {
    data:function(){
        return{
            cart: [
                {
                    title: "Jas Hujan",
                    description: 'Jas Anti Air Kualitas Super',
                    stock: 50,
                    price: 100000
                },
                {
                    title: "Payung",
                    description: 'Sedia Payung Sebelum Hujan',
                    stock: 50,
                    price: 25000
                },
                {
                    title: "Kanebo",
                    description: 'Lap Menyerap Air',
                    stock: 50,
                    price: 10000
                },
            ],
            list: [
                {
                    title: "Jas Hujan",
                    description: 'Jas Anti Air Kualitas Super',
                    stock: 50,
                    price: 100000
                },
                {
                    title: "Payung",
                    description: 'Sedia Payung Sebelum Hujan',
                    stock: 50,
                    price: 25000
                },
                {
                    title: "Kanebo",
                    description: 'Lap Menyerap Air',
                    stock: 50,
                    price: 10000
                },
            ],
        }
    },
    methods:{
        deleteItem(index){
            this.cart.splice(index,1);
            alert("Success Delete !")
        },
        payItem(index){
            this.cart.splice(index);
            alert("Payment Success !")
        }
        // addToCart(){
        //     let cart = {
        //         title = list.title,
        //           description =list.description,
        //           price = list.price
        //     }
        //     return this.list[index];
        //     this.cart.push(list, index)
        //     // this.input = ""
        // },
        
    },
}
</script>

<style>

</style>