<template>
    <div class="outer-cont">
        <div class="img-cont">
            <img :src="product.url" :alt="product.name" id="productImg" />
        </div>
        <div class="product-desc">
            
            <p id="name"><strong> {{product.name}} </strong></p>
            <p id="category">Category: {{product.category}}</p>
            <p id="price"><b>Price : ${{ product.price }}</b></p>
            <p id="rating"><b>Rating : {{ product.rating }}</b></p>
            <p id="reformulated"><b>{{ product.reformulated? '** REFORMULATED **': '' }}</b></p>

        </div>
    </div>
</template>

<script>

export default{
    name: 'MakeupComp',
    props: ['product'],

}
</script>

<style scoped>
.outer-cont{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    background-color:rgb(232, 232, 243);
    justify-content: center;
    align-items: center;
    min-width: 450px;
    margin: 30px 0;
    border:6px inset rgb(187, 179, 179);
    border-radius: 15px;
}
.img-cont{
        width: 240px;
        height: 280px;
        ;
        /* margin: 0 auto; */
        
    }
.product-desc{
    text-align: center;
    max-width: 200px;
    margin: 10px;
}
#productImg{
    width: 210px;
    height: 240px;
    margin:20px;
    
    align-items: left;
    border-radius: 5px;
    
}

#price{
    font-size: 16px;
    
}
#name{
    color:rgb(112, 69, 110);
   font-size: larger;
   font-style: oblique;
}
#category,#rating{
    font-size:12px;
    color: grey;
    
}
#reformulated{
    color: green;
    font-size:14px;
}
</style>
