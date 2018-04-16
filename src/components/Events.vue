<template>
    <div id="cart-app">
        <div class="main">
            <div class="products">
                <div class="product" v-for="(item, index) in items">
                    <div>
                        <div class="product-image">
                          <img v-bind:src="item.image">
                        </div>
                    </div>
                    <div class="product-box">
                        <h4 class="product-title">{{ item.title }}</h4>
                        <button v-on:click="addItem(index)" class="add-to-cart btn">Add to cart</button>
                    </div>
                    
                </div>
                
            </div>
            <div class="cart">
                <h2>Shopping Cart</h2>
                <ul>
                    <li class="cart-item" v-for="item in cart">
                        <div class="item-title">{{ item.title }}</div>
                        <span class="item-qty">{{ item.price | currency }} x {{ item.qty }}</span>
                        <button class="btn" v-on:click="inc(item)">+</button>
                        <button class="btn" v-on:click="dec(item)">-</button>
                    </li>
                </ul>
                <div v-if="cart.length">
                    <div>Total: {{ total | currency }} </div>
                </div>
                <div v-else class="empty-cart">
                    No items in the cart.
                </div>
            </div>
        </div>
    </div>
</template>
<script>


export default {
   data() {
    return {
        PRICE : 20,
        total : 0,
        items: [
            {id:1, title: 'FC Barcelona Home Kit 2017-18', image: './assets/one.png'},
            {id:2, title: 'FC Barcelona Away Kit 2017-18', image: './assets/two.jpg'},
            {id:3, title: 'FC Barcelona Third Kit 2017-18', image: './assets/three.jpg'}
        ],
        cart: []
        
    }
  },
    

  methods: {
      
      addItem: function(index) {
        this.total += this.PRICE;
        var item = this.items[index];
        var found = false;
        for (var i=0; i< this.cart.length; i++){
            if (this.cart[i].id == item.id) {
                found = true;
                this.cart[i].qty++;
                break;
            }
        }
        if (!found) {
            this.cart.push({
                id: item.id,
                title: item.title,
                qty: 1,
                price: this.PRICE
            });
        }
    },

    inc: function(item) {
        item.qty++;
        this.total += this.PRICE;
    },
    dec: function(item) {
        item.qty--;
        this.total -= this.PRICE;
        if (item.qty <= 0) {
            for (var i = 0; i < this.cart.length; i++) {
                if (this.cart[i].id === item.id) {
                    this.cart.splice(i, 1);
                    break;
                }
            }
        }
    }
},



filters: {
    currency: function(price) {
        return '$'.concat(price.toFixed(2));
        // fix decimal places

    }
}


}
</script>
<style scoped>
    /* Generic styling */

/* h2, h3, h4, h5, h6 {
    font-family: 'Montserrat', sans-serif;
} */

button:focus, input:focus {
    outline: none;
}

.btn {
    background-color: #2c3e50;
    border-radius: 2px;
    color: white;
    user-select: none;
    border: none;
    cursor: pointer;
    opacity: 1;
}

.btn:active {
    opacity: 0.8;
}

[v-cloak] {
    display: none !important;
}

.fade-enter-active {
    transition: opacity .5s
}
.fade-enter, .fade-leave-active {
    opacity: 0
}

/* Sections */





.main {
    display: flex;
    flex-direction: row;
    flex: 1;
    padding-bottom: 2rem;
}

.products {
    flex: 3;
}

.cart {
    flex: 2;
}

/* Header */

h1 {
    font-family: 'Luckiest Guy', cursive;
    font-size: 2.5rem;
    padding: 2rem 0 1rem;
    margin: 0;
    color: #FFAFAF;
    text-shadow: black 2px 1px 1px;
}

/* Products */

.product-list {
    margin-right: 5rem;
}

.product {
    padding: 1rem;
    border: 1px solid #E9E9E9;
    border-radius: 2px;
    overflow: auto;
    margin: 1rem 1rem 1rem 0;
    display: flex;
    flex-flow: row nowrap;
}

.product-box{
    margin-left: 20px;
}

.product-image {
    height: 200px;
    width: 200px;
    overflow: hidden;
    border: 1px solid #E9E9E9;
    border-radius: 2px;
}

.product-image > img {
    width: 100%;
    display: block;
}

.product-title {
    margin-top: 0;
}

.product .add-to-cart {
    padding: 0.5rem 1rem;
    font-size: 0.8rem;
}

#product-list-bottom {
    text-align: center;
    color: #AAAAAA;
    font-size: 0.85rem;
}

/* Cart */

.cart {
    margin-top: 1rem;
    margin-left: 1rem;
    padding-left: 1rem;
}

.cart .empty-cart {
    padding-top: 1rem;
}

.cart > h2 {
    margin-top: 0;
}

.cart ul {
    width: 100%;
    font-size: 0.9rem;
    border-top: 2px solid black;
    list-style: none;
    margin: 0;
    padding: 0;
}

.cart ul li {
    vertical-align: top;
    padding: 1rem 1rem 1rem 0;
}

.cart ul .cart-item {
    border-bottom: 1px solid #E9E9E9;
}

.cart ul .cart-item .item-title {

}

.cart ul .cart-item .item-price {
    font-weight: bold;
    padding-top: 0.5rem;
}

.cart ul .cart-item .item-qty {
    margin-right: 1rem;
}

.cart ul .cart-item:last-child {
    border-bottom: none;
}

.cart ul .cart-item button {
    margin-right: 3px;
}

</style>