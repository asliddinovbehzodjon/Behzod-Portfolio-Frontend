<template>
<header>

    <div class="user">
        <img :src="me.image" alt="">
        <h3 class="name">Behzod asliddinov</h3>
        <p class="post">full stack web developer</p>
    </div>

    <nav class="navbar">
        <ul>
            <li><a href="#home">Asosiy sahifa</a></li>
            <li><a href="#about">Men haqimda</a></li>
            <li><a href="#education">Xizmatlar</a></li>
            <li><a href="#portfolio">Portfolio</a></li>
            <li><a href="#contact">Bog'lanish</a></li>
        </ul>
    </nav>

</header>

<!-- header section ends -->

<div id="menu" class="fas fa-bars"></div>


<!-- home section starts  -->

<section class="home" id="home">

    <h3>Salom!</h3>
    <h1>Men <span>Behzod asliddinov</span></h1>
    <p>
        Full Stack web dasturchiman ! Turli xil web dasturlar va telegram botlar yasash bilan shug'ullaman!
    </p>
    <a href="#about"><button class="btn">Men haqimda <i class="fas fa-user"></i></button></a>
     <div class="share">
        
        <a :href="link.phone" class="fa fa-mobile-phone" target="_blank"></a>
        <a :href="link.telegram" class="fab fa-telegram" target="_blank"></a>
        <a :href="link.facebook" class="fab fa-facebook-f" target="_blank"></a>
        <!-- <a href="#" class="fab fa-twitter"></a> -->
        <a :href="link.instagram" class="fab fa-instagram" target="_blank"></a>
        <a :href="link.linkedin" class="fab fa-linkedin" target="_blank"></a>
        <a :href="link.youtube" class="fab fa-youtube" target="_blank"></a>
        <a :href="link.github" class="fab fa-github" target="_blank"></a>
    </div>

</section>

<!-- home section ends -->

<!-- about section starts  -->

<section class="about" id="about">

    <h1 class="heading"> <span>Men</span> haqimda </h1>

    <div class="row">

        <div class="info">
            <h3> <span> Ismim : </span> {{me.name}} </h3>
            <h3> <span> Yoshim : </span> {{me.age}} </h3>
            <h3> <span> Ishlatadigan texnoligiyalarim : </span> {{me.technologies}} </h3>
            <h3> <span> Kasbim : </span> {{me.profession}} </h3>
            <h3> <span> Til : </span> {{me.language}} </h3>
            <a :href="me.cv" download target="_blank"><button class="btn"> CVni ko'rish <i class="fas fa-download"></i> </button></a>
        </div>

        <div class="counter">

            <div class="box">
                <span>1.5+</span>
                <h3>yillik tajriba</h3>
            </div>

            <div class="box">
                <span>15+</span>
                <h3>loyihalar</h3>
            </div>

            <div class="box">
                <span>30+</span>
                <h3>xursand mijozlar</h3>
            </div>

            <div class="box">
                <span>4+</span>
                <h3>mukofotlar</h3>
            </div>

        </div>

    </div>

</section>

<!-- about section ends -->

<!-- education section starts  -->

<section class="education" id="education">

    <h1 class="heading"> Mening <span>Xizmatlarim</span> </h1>

    <div class="box-container">

        <div class="box">
            <i class="fas fa-graduation-cap"></i>
            <span>Ta'lim</span>
            <h3>Python Foundation kursi</h3>
            <p>Foundation dasturlash kursi bu sizga qisqa muddatda dasturlash olaimiga kirishizga yordam beradi.
                Kurs davomiyligi 1 oy.Kursda dasturlash haqida tushuncha olasiz bu Python dasturlash tili orqali tushuntiriladi.</p>
        </div>

        <div class="box">
            <i class="fas fa-graduation-cap"></i>
            <span>Ta'lim</span>
            <h3>telegram bot kursi</h3>
            <p>Telegram bot dasturlash kursi bu sizga qisqa muddatda Telegram bot dasturchi bo'lishizga yordam beradi.
                Kurs davomiyligi 2 oy.Kursimiz 2 bosqichdan iborat.
                I.Python Beginner
                II.Backend:Telegram bot</p>
        </div>

        <div class="box">
            <i class="fas fa-graduation-cap"></i>
            <span>Ta'lim</span>
            <h3>Backend dasturlash kursi</h3>
            <p>Backend dasturlash kursi bu sizga qisqa muddatda Backend dasturchi bo'lishizga yordam beradi.
Kurs davomiyligi 4 oy.Kursimiz 3 bosqichdan iborat.
I.Python Beginner
II.Backend: Python OOP,Telegram bot
III.Django,Django Rest Framework</p>
        </div>

        <div class="box">
            <i class="fas fa-graduation-cap"></i>
            <span>Ta'lim</span>
            <h3>Full Stack web dasturlash kursi</h3>
            <p>FullStack Web dasturlash kursi
FullStack Web dasturlash kursi bu sizga qisqa muddatda Web dasturchi bo'lishizga yordam beradi.
Kurs davomiyligi 6 oy.Kursimiz 3 bosqichdan iborat.
I.Frontend Verstka: Html,Css,Bootstrap
II.Backend: Python,Telegram bot,Django,Django Rest Framework
III.Frontend Framewrok: Javascript,Vuejs</p>
        </div>

        <div class="box">
            <i class="fab fa-telegram"></i>
            <span>Telegram bot</span>
            <h3>Telegram bot yasash xizmati</h3>
            <p>istalgan turdagi telegram bot tayyorlash va uni serverga qo'yish.Arzon narxda va sifatli ko'rinishda</p>
        </div>

        <div class="box">
            <i class="fas fa-code"></i>
            <span>Web sayt</span>
            <h3>web sayt tayyorlash</h3>
            <p>Istalgan turdagi Web saytlar tayyorlash.Masalan: Internet magazin,Blog,Axborot beruvchi saytlar!</p>
        </div>

    </div>

</section>

<!-- education section ends -->

<!-- portfolio section starts  -->

<section class="portfolio" id="portfolio">

    <h1 class="heading"> Mening <span>portfoliolarim</span> </h1>

    <div class="box-container">

      
      <div class="box" v-for="portfolio in portfolios" :key="portfolio.id">
        <img :src="portfolio.image" alt="">
        <div class="content">
            <h3 class="ptitle" style=" color:#f9ca24 ;
    font-size: 24px;">{{portfolio.name}}</h3>
            <a :href="portfolio.url" class="btn" target="_blank">Portfolioni ko'rish</a>
        </div></div>

      

    </div>
      <div class="center mt-3">
        <div class="pagination">
            <a @click="Orqaga()">Orqaga</a>
            <a v-if="currentpage_num">{{currentpage_num}} ta {{allpages}} dan</a>
            <a v-else>0 ta 0 dan</a>
            <a @click="Oldinga()">Oldinga</a>
        </div>
    </div>
</section>


<!-- portfolio section ends -->

<!-- contact section starts  -->

<section class="contact" id="contact">

    <h1 class="heading"> <span>Menga</span> bog'lanish </h1>

    <div class="row">

        <div class="content">

            <h3 class="title">Malumot:</h3>

            <div class="info">
                <h3> <i class="fas fa-envelope"></i> behzodme@gmail.com </h3>
                <h3> <i class="fas fa-phone"></i> +998 99 116-04-34 </h3>
                <h3> <i class="fas fa-phone"></i> +998 91 008-08-86 </h3>
                <h3> <i class="fas fa-map-marker-alt"></i>Toshkent,O'zbekiston </h3>
            </div>

        </div>

        <form @submit.prevent="SendMe">

            <input type="text" placeholder="Ismingiz" class="box" v-model="name" required>
            <input type="email" placeholder="Elektron pochta manzilingiz" class="box" v-model="email" required>
            
            <textarea name="" id="" cols="30" rows="10" class="box message" placeholder="Xabaringiz..." v-model="message" required></textarea>
            <button type="submit" class="btn"> Yuborish <i class="fas fa-paper-plane"></i> </button>

        </form>

    </div>

</section>

<!-- contact section ends -->

<!-- scroll top button  -->

<a href="#home" class="top">
    <!-- <img src="images/scroll-top-img.png" alt=""> -->
</a>
</template>

<script>
import { toast } from 'bulma-toast'
import axios from 'axios'
export default {
    name: 'Main',
    mounted(){
                 this.getme()
    },
    data(){
        return{
            url:'https://portfoliouz.pythonanywhere.com/api/v1',
            me:{
                name:'',
                age:'',
                technologies:'',
                profession:'',
                language:'',
                image:'',
                cv:''
            },
            link:{
                telegram:'',
                instagram:'',
                facebook:'',
                github:'',
                youtube:'',
                linkedin:'',
                phone:'',
            },
            currentpage_num:'',
            allpages:'',
            next:'',
            previous:'',
            portfolios:[],
            name:'',
            email:'',
            message:'',

        }
    },
    methods:{
       async SendMe(){
              await axios.post(`${this.url}/sendtelegram/${this.name}/${this.email}/${this.message}/`).then(res =>{
                toast({
                    pauseOnHover:true,
                    message:'Xabar yuborildi',
                    position:'bottom-right',
                    duration:2000,
                    dismissible:true,
                    type:'is-light',
                    extraClasses:'btoast'
                    
                })
                this.name=''
                this.email=''
                this.message=''

              })     
       } ,
       async Oldinga(){
            if (this.next) {
                   await  axios.get(this.next).then(res => {
                        this.portfolios = res.data.results,
                            this.next = res.data.next,
                            this.previous = res.data.previous,
                            this.allpages = res.data.all_pages,
                            this.currentpage_num = res.data.current_page_num
                    })
                } else {
                await axios.get(`${this.url}/portfolio/`).then(res => {
                this.portfolios = res.data.results,
                this.next = res.data.next,
                this.previous = res.data.previous,
                this.allpages = res.data.all_pages,
                this.currentpage_num = res.data.current_page_num
               
            })
                }
        },
        async Orqaga(){
            if (this.previous) {
                    await axios.get(this.previous).then(res => {
                        this.portfolios = res.data.results,
                            this.next = res.data.next,
                            this.previous = res.data.previous,
                            this.allpages = res.data.all_pages,
                            this.currentpage_num = res.data.current_page_num
                    })
                } else {
                await axios.get(`${this.url}/portfolio/`).then(res => {
                this.portfolios = res.data.results,
                this.next = res.data.next,
                this.previous = res.data.previous,
                this.allpages = res.data.all_pages,
                this.currentpage_num = res.data.current_page_num
               
            })
                }
        },

        async getme(){
            await axios.get(`${this.url}/me/`).then(res => {
                this.me = res.data[0]
               
            })
            await axios.get(`${this.url}/social/`).then(res => {
                this.link = res.data[0]
               
            })
            await axios.get(`${this.url}/portfolio/`).then(res => {
                this.portfolios = res.data.results,
                this.next = res.data.next,
                this.previous = res.data.previous,
                this.allpages = res.data.all_pages,
                this.currentpage_num = res.data.current_page_num
               
            })
            
        },
       
    }
}
</script>

<style scoped>
@import '../assets/css/style.css';


</style>
