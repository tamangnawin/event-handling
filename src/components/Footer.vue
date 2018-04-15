<template>
    <footer>
        <div class="footerHeader" ></div>
        <div class="container">
            <div class="col-md-4 l" >
                <h3>About us</h3>
                <p>
                    Mero Bazaar is Asia’s fastest growing online marketplace, offering an unparalleled shopping experience in Pakistan, Bangladesh, Myanmar, Sri Lanka and Nepal. Mero Bazaar hosts a wide assortment of consumer electronics, fashion and beauty products, alongside a rapidly growing miscellany of general merchandise. Mero Bazaar privileges the personalization and security of the shoppers’ experience above all else. Excellent value-for-money, large assortment of original products, fast delivery and easy returns are Daraz signatures.
                </p>
            </div>
            
            <div class="col-md-4 l">
                <h3>Our Location </h3>
                <iframe src="https://www.google.com/maps/embed?pb=!1m10!1m8!1m3!1d7064.26494743033!2d83.4660464!3d27.713195799999998!3m2!1i1024!2i768!4f13.1!5e0!3m2!1sen!2snp!4v1523615589221" sytle="" frameborder="0" style="border:0" allowfullscreen></iframe>
            </div>


            <div class="col-md-4 l" >
                <h3>Contact Us</h3>
                <ul>
                    <li>Phone : 123 - 456 - 789</li>
                    <li>E-mail : shop@merobazaar.com</li>
                    <li>Fax : 123 - 456 - 789</li>
                </ul>
                
                <ul class="sm">
                    <li><a href="#" ><img src="https://www.facebook.com/images/fb_icon_325x325.png" class="img-responsive"></a></li>
                    <li><a href="#" ><img src="https://lh3.googleusercontent.com/00APBMVQh3yraN704gKCeM63KzeQ-zHUi5wK6E9TjRQ26McyqYBt-zy__4i8GXDAfeys=w300" class="img-responsive" ></a></li>
                    <li><a href="#" ><img src="http://playbookathlete.com/wp-content/uploads/2016/10/twitter-logo-4.png" class="img-responsive"  ></a></li>
                </ul>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
  
}
</script>

<style scoped>
    footer {
    background-color: rgba(44, 62, 80, 1.0);
    height: 310px;
    width: 100%;
    bottom: 0;
    font-weight: lighter;
    color: white;
    
}
    .footerHeader{
        width:100%;
        padding:1em;
        background-color:rgba(52, 73, 94,1.0);
        text-align:center;
        color:white;
        margin-bottom: 20px;
    }
    footer h3{
        font-weight:lighter;
    }
    footer ul{
        padding-left:5px;
        list-style:none;
    }
    footer p{
        text-align : justify;
        font-size : 12px;
    }
    footer iframe {
        width:100%;
        position:relative;
        height:170px;
    }
    .sm{
        list-style:none;
        overflow:auto;
    }
    .sm li {
        float: left;
        padding:5px;
    } 
    .sm li a img {
        width:32px;
        float: left;
    }

    .l {
        float: left;
    }
</style>
