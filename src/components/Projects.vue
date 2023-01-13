<template>
  <div
    :style="{
      'background-color': `#E6BBAD`,
    }"
  >
    <h2 class="title">Projects</h2>
    <div class="container-sm text-center">
      <div class="row">
        <div class="col-md-6 g-3" v-for="item in projects">
          <div class="card-container">
            <div class="front">
              <img :src="item.image" width="300" height="300" alt="" />
            </div>
            <div class="back">
              <h5>{{ item.name }}</h5>
              <p>{{ item.description }}</p>
              <a :href="item.site">netlify</a><br />
              <a :href="item.github"><i class="fa-brands fa-github"></i></a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      projects: [
        {
          name: "E-Commerce Website",
          image:
            "https://i.postimg.cc/8kWdtCYg/Screenshot-2022-11-01-115801.png",
          description: "Beauty salon where everyone is welcomed.",
          site: "https://leboparlour.netlify.app",
          github: "https://github.com/Lebo04/Beauty-Parlour.git",
        },
        {
          name: "Mobile Repair Shop",
          image:
            "https://i.postimg.cc/8cB6D78F/Screenshot-2022-11-04-123257.png",
          description:
            "People who care and will fix your mobile devices anytime.",
          site: "https://mobi-car.netlify.app",
          github: "https://github.com/Lebo04/Mobile.git",
        },
        {
          name: "Calculator",
          image:
            "https://i.postimg.cc/8cWqCVwf/Screenshot-2023-01-11-111428.png",
          description:
            "Simple calculator that makes simple calculations like addition, subtraction, multiplication and division.",
          site: "https://leboparlour.netlify.app",
          github: "https://github.com/Lebo04/Beauty-Parlour.git",
        },
        {
          name: "Point of sale",
          image:
            "https://i.postimg.cc/pVQrprCs/Screenshot-2023-01-11-130311.png",
          description: "Shoe shop that sells heels.",
          site: "https://kelebogile-pointofsale.netlify.app",
          github: "https://github.com/Lebo04/Shoes.git",
        },
        {
          name: "BMI",
          image:
            "https://i.postimg.cc/zf1NND1W/Screenshot-2023-01-11-163044.png",
          description: "Calculator that calculates your BMI.",
          site: "https://kelebogile-bmi.netlify.app",
          github: "https://github.com/Lebo04/BMI-calculator.git",
        },
        {
          name: "Portfolio",
          image:
            "https://i.postimg.cc/hPWRTPfY/Screenshot-2023-01-11-163227.png",
          description: "Digital Portfolio.",
          site: "https://kelebogile-portfolio.netlify.app",
          github: "https://github.com/Lebo04/Portfolio_.git",
        },
      ],
    };
  },
};
</script>
<style scoped>
a {
  font-size: 1.5rem;
  color: #111;
}
a:hover {
  font-size: 2.5rem;
}
.title {
  position: relative;
  text-align: center;
  font-size: 4rem;
  font-weight: 600;
  margin-bottom: 0.1rem;
  padding-top: 4rem;
  padding-bottom: 2rem;
}
.title::before {
  content: "";
  position: absolute;
  bottom: 0px;
  left: 50%;
  width: 18rem;
  height: 0.2rem;
  background: #111;
  transform: translateX(-50%);
}
.card-container,
.front,
.back {
  width: 20rem;
  height: 20rem;
}

.card-container {
  margin: 1rem;
  animation: in 1.5s ease-in;
}
@keyframes in {
    0% {
        transform: translateX(100vh) scale(0);
    }
    100% {
        transform: translateX(-10vh) scale(1);
    }
}


.front {
  padding: 1rem;
  font-size: 1rem;
  text-transform: uppercase;
  text-align: center;
}

.back {
  box-sizing: border-box;
  padding: 2rem;
  border-radius: 4px;
  box-sizing: 0 1rem 2rem rgb(0, 0, 0, 0.25);
  font-size: 5rem;
  text-transform: uppercase;
  text-align: center;
  background-color: rgba(245, 154, 169, 0.903);
}

.card-container .back {
  font-size: 1rem;
}

.card-container {
  position: relative;
}

.front,
.back {
  position: absolute;
  top: 0;
  left: 0;
  backface-visibility: hidden;
  overflow: hidden;
  transition: all 0.8s ease;
}

.back {
  transform: rotateY(180deg);
}

.card-container:hover .front {
  transform: rotateY(-180deg);
}

.card-container:hover .back {
  transform: rotateY(0deg);
}

.card-container {
  perspective: 30rem;
}

@media screen and (max-width: 300px) {
  a {
    font-size: 1.5rem;
    color: #111;
  }
  a:hover {
    font-size: 2.5rem;
  }
  .title {
    font-size: 2.5rem;
    margin-bottom: 0rem;
    padding-top: 2rem;
    padding-bottom: 1rem;
  }
  .title::before {
    width: 10rem;
  }
  .card-container,
  .front,
  .back {
    width: 15rem;
    height: 15rem;
  }
  
  .back {
    text-transform: lowercase;
  }
}
@media screen and (max-width: 720px) {
  a {
    font-size: 2rem;
    color: #111;
  }
  a:hover {
    font-size: 2.5rem;
  }
  .title {
    font-size: 3rem;
    margin-bottom: 0rem;
    padding-top: 2rem;
    padding-bottom: 1rem;
  }
  .title::before {
    width: 11rem;
  }
  .card-container,
  .front,
  .back {
    width: 14rem;
    height: 18rem;
    margin-left: 4rem;
  }
  
  .back {
    text-transform: uppercase;
  }
}
</style>
