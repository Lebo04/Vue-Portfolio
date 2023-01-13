<template>
  <div
  :style="{
      'background-color': `#E6BBAD`,
    }">
  <div class="social">
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
        </div>
      <div class="about">
        <h2 class="title">About Me</h2>
        <p>
          My name is Kelebogile Nobomvu I am 21 years of age. I matriculated in
          2019 with bachelors. Right now I am a web developer in training. I
          consider myself a forever student as I am eager to both build an
          academic foundation and a career at the same time.<br />
          I fell in love with coding at a time in my life I did not think that
          is even possible. I think that is the reason why I am so determined in
          seeing it through.<br />
          I am a very friendly but shy person at the same time. I love to listen
          to music to get me in the zone. I love helping another person where i
          can and I love eating.
        </p>
      </div>

  </div>
</template>
<script>
export default {};
</script>
<style scoped>
.social {
    display: flex;
    flex-direction: column;
    position: fixed;
    right: 2%;
    transform: translateY(40%);
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
    margin-top: 0rem;
    padding: 2rem;
  }
  
  .social a:hover {
    color: #111;
  }
.about .title {
    position: relative;
    text-align: center;
    font-size: 3rem;
    font-weight: 600;
    margin-bottom: 4rem;
    padding-bottom: 2rem;
  }
  
  .about .title::before {
    content: "";
    position: absolute;
    bottom: 0rem;
    left: 50%;
    width: 13rem;
    height: 0.2rem;
    background: #111;
    transform: translateX(-50%);
  }
  .about .title::after {
    position: absolute;
    left: 50%;
  }

  .about {
    padding-top: 3rem;
    margin-left: 5rem;
    margin-right: 5rem;
    height: 100vh;
  }
  
  .about p {
    text-align: center;
    font-size: 1.5rem;
    font-weight: 600;
  }

  @media screen and (max-width: 420px) {
    .social {
      right: 5%;
      transform: translateY(20%);
    }
    
    .social a {
      font-size: 1.5rem;
    }
  .about .title {
      font-size: 2rem;
      font-weight: 600;
      margin-bottom: 2rem;
      padding-bottom: 1rem;
    }
    
    .about .title::before {
      width: 7rem;
    }
  
    .about {
      padding-top: 1rem;
      margin-left: 3rem;
      margin-right: 3rem;
      height: 120vh;
    }
    
    .about p {
      font-size: 1rem;
      font-weight: 600;
    }
  }
  @media screen and (min-width: 421px) and (max-width: 720px)  {
    .social {
      right: 5%;
      transform: translateY(20%);
    }
    
    .social a {
      font-size: 1.5rem;
    }
  .about .title {
      font-size: 3rem;
      font-weight: 600;
      margin-bottom: 2rem;
      padding-bottom: 1rem;
    }
    
    .about .title::before {
      width: 13rem;
    }
  
    .about {
      padding-top: 1rem;
      margin-left: 3rem;
      margin-right: 3rem;
      height: 180vh;
    }
    
    .about p {
      font-size: 1.5rem;
      font-weight: 600;
    }
  }
  @media screen and (min-width: 721px) and (max-width: 1280px) {
    .social {
      right: 5%;
      transform: translateY(20%);
    }
    
    .social a {
      font-size: 3.5rem;
      padding: 3.5rem;
    }
  .about .title {
      font-size: 4rem;
      font-weight: 600;
      margin-bottom: 2rem;
      padding-bottom: 1rem;
    }
    
    .about .title::before {
      width: 14rem;
    }
  
    .about {
      padding-top: 4rem;
      margin-left: 3rem;
      margin-right: 3rem;
      height: 100vh;
    }
    
    .about p {
      font-size: 2rem;
      font-weight: 600;
    }
  }

</style>
