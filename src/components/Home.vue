<template>
  <div
    :style="{
      'background-image': `url(https://i.postimg.cc/fLKVt5xW/home.jpg)`,
      'background-size': 'cover',
    }"
  >
    <section class="social">
      <a href="https://www.instagram.com/lebonobomvu"
        ><i class="fa fa-instagram"></i
      ></a>
      <a href="https://www.facebook.com/kilebogile.lebza"
        ><i class="fa fa-facebook"></i
      ></a>
      <a href="https://www.twitter.com/kelebogile_04"
        ><i class="fa fa-twitter"></i
      ></a>
      <a href="https://www.youtube.com"><i class="fa fa-youtube"></i></a>
      <a href="https://www.linkedin.com/in/kelebogile-nobomvu-a6389717a"
        ><i class="fa fa-linkedin"></i
      ></a>
      <a href="https://github.com/Lebo04"><i class="fa fa-github"></i></a>
    </section>

    <section class="home" id="home">
      <img
        src="https://i.postimg.cc/L8Syk8Py/IMG-20221203-WA0016-removebg-preview.png"
        width=""
        alt=""
      />
      <div class="home-cont" v-for="item in CV">
        <div class="texty pop">Hi, my name is</div>
        <div class="texty pop delay-1">Kelebogile Nobomvu</div>
        <div class="texty pop delay-2">
          And I'm a <span>Web Developer </span>in training.
        </div>
        <a :href="item.cv">Hire me</a>
      </div>
    </section>
  </div>
</template>
<script>
export default {
  data() {
    return {
      CV : [
        {
          cv : "../assets/CV_2023011209104117.pdf"
        }
      ]
    }
  },
};
</script>
<style scoped>
img {
  width: 35rem;
}
.social {
  display: flex;
  flex-direction: column;
  position: fixed;
  right: 2%;
}

.social a {
  display: block;
  text-align: center;
  transition: all 0.3s ease;
  color: rgba(251, 84, 112, 0.903);
  font-size: 2rem;
  width: 3rem;
  height: 3rem;
  border-radius: 50%;
  margin-top: 1.5rem;
  padding: 1.7rem;
}

.social a:hover {
  color: #111;
}

.home {
  display: flex;
  height: 42.2rem;
  justify-content: center;
  align-items: center;
}

.home .home-cont {
  margin: auto 0 auto 4rem;
}

.home .home-cont .texty {
  font-size: 4rem;
  font-weight: 600;
  color: #111;
}

.home .home-cont .delay-1 {
  font-size: 3rem;
  font-weight: 600;
}

.home .home-cont .delay-2 {
  font-size: 2rem;
  font-weight: 600;
  margin-top: 5rem 0;
}

.home .home-cont .texty span {
  color: crimson;
  font-size: 3rem;
}

.home .home-cont a {
  display: inline-block;
  background: #111;
  font-size: 1rem;
  padding: 0.5rem 0.5rem;
  margin-top: 1rem;
  border-radius: 0.5rem;
  border: 0.3rem solid #111;
  transition: all 0.3s ease;
}

.home .home-cont a:hover {
  color: crimson;
}

section {
  padding: 5rem;
  padding-bottom: 3rem;
}

.texty {
  animation-duration: 0.5s;
  animation-name: anime;
  animation-delay: 0.5s;
  animation-fill-mode: backwards;
}

@keyframes anime {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
.texty .pop {
  animation-name: animate-pop;
  animation-timing-function: cubic-bezier(0.26, 0.53, 0.74, 1.48);
}

@keyframes animate-pop {
  0% {
    opacity: 0;
    transform: scale(0.5, 0.5);
  }

  100% {
    opacity: 1;
    transform: scale(1, 1);
  }
}

.delay-1 {
  animation-delay: 0.6s;
}

.delay-2 {
  animation-delay: 0.7s;
}

@media screen and (min-width: 421px) and (max-width: 720px) {
  img {
    width: 15rem;
    margin-left: 0rem;
  }
  .social {
    right: 0.01%;
  }
  
  .social a {
    font-size: 1.5rem;
    width: 3rem;
    height: 4rem;
    margin-top: 0rem;
    padding: 1.5rem;
  }
  
  .home {
    height: 35rem;
    margin-left: 5rem;
    justify-content: right;
  }
  .home .home-cont {
    margin: 0rem;
  }
  
  .home .home-cont .texty {
    font-size: 2rem;
    font-weight: 600;
  }
  
  .home .home-cont .delay-1 {
    font-size:2rem;
    font-weight: 600;
  }
  
  .home .home-cont .delay-2 {
    font-size: 2rem;
    font-weight: 600;
    margin-top: 2rem 0;
  }
  
  .home .home-cont .texty span {
    font-size: 2rem;
  }
  
  section {
    padding: 5rem;
    padding-bottom: 3rem;
  }
}


@media screen and (max-width: 420px) {
  img {
    width: 15rem;
  }
  .social {
    left: 55%;
  }
  
  .social a {
    font-size: 1.3rem;
    width: 2rem;
    height: 2rem;
    margin-top: 1rem;
    padding: 1rem;
  }
  
  .home {
    flex-direction: column;
    height: 60rem;
    margin-left: 0rem;
  }
  
  .home .home-cont .texty {
    font-size: 2rem;
    font-weight: 600;
  }
  
  .home .home-cont .delay-1 {
    font-size: 2rem;
    font-weight: 600;
  }
  
  .home .home-cont .delay-2 {
    font-size: 2rem;
    font-weight: 600;
    margin-top: 2rem 0;
  }
  
  .home .home-cont .texty span {
    font-size: 2rem;
  }
  
  section {
    padding: 5rem;
    padding-bottom: 3rem;
  }
}
@media screen and (min-width: 721px) and (max-width: 1092px) {
  img {
    width: 50rem;
  }
  .social {
    right: 1%;
  }
  
  .social a {
    font-size: 3rem;
    width: 2rem;
    height: 2rem;
    margin-top: 1rem;
    padding: 4rem;
  }
  
  .home {
    height: 60rem;
    margin-left: 0rem;
  }
  
  .home .home-cont .texty {
    font-size: 4rem;
    font-weight: 600;
  }
  
  .home .home-cont .delay-1 {
    font-size: 4rem;
    font-weight: 600;
  }
  
  .home .home-cont .delay-2 {
    font-size: 4rem;
    font-weight: 600;
    margin-top: 2rem 0;
  }
  
  .home .home-cont .texty span {
    font-size: 4rem;
  }
  
  section {
    padding: 5rem;
    padding-bottom: 3rem;
  }
}

</style>
