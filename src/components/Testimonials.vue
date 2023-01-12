<template>
  <div
    :style="{
      'background-color': `#E6BBAD`,
    }"
  >
    <h2 class="title">Testimonials</h2>
    <div class="container-sm text-center">
      <div class="row">
        <div class="col-md-6 g-3" v-for="item in testimonials" :key="item">
          <div class="card-container">
            <div class="front">
              <img :src="item.image" width="300" height="300" alt="" />
              <h5>{{ item.name }}</h5>
              <p>{{ item.relation }}</p>
            </div>
            <div class="back">
              <p>{{ item.message }}</p>
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
      testimonials: [
        {
          name: "Candice Amon",
          image: "https://i.postimg.cc/s2WxDtdF/candice-2022.jpg",
          relation: "Life Choices Academy, Facilitator",
          message: `Stays true to what she holds dear to her heart. She remains
    firm and supports whole heartedly what she believes in.
    Strives to do her best at all times and does not give up 
    easily.`,
        },
        {
          name: "Sibabalwe Mafestile",
          image: "https://i.postimg.cc/L58mfW78/1667466094491-720.jpg",
          relation: "Life Choices Academy, Colleague",
          message: `Kelebogile is a grounded individual who adapts to
    environmental changes, works hard on completing her tasks and
    developing her skills`,
        },
        {
          name: "Buhle Qampi",
          image: "https://i.postimg.cc/cJhjYJNf/buhle.jpg",
          relation: "Life Choices Academy, Colleague",
          message: `Kelebogile is an exceptional coder, her code is always neat
    and coherent. Her developer skills are necessary for any
    workplace`,
        },
        {
          name: "Uzukhanye Dywili",
          image: "https://i.postimg.cc/65sXBy6Q/img-20220625-wa0031.jpg",
          relation: "Life Choices Academy, Colleague",
          message: `Kelebogile, I thank GOD for blessing me with you in my life.
    A selfless, humble, smart and beautiful person`,
        },
        {
          name: "Chrisaner Matthys",
          image: "https://i.postimg.cc/gkyfdsBM/20221020-144016.jpg",
          relation: "Life Choices Academy, Colleague",
          message: `Kelebogile is a determined individual. he executes given
    tasks diligently as shes's passionate about what she does. I
    believe she will be a asset to any organization`,
        },
        {
          name: "Masizole Shabane",
          image: "https://i.postimg.cc/cL45WS3H/screenshot-20221103-143935.jpg",
          relation: "Life Choices Academy, Colleague",
          message: `A wonderful colleague to work beside. Kind in her approach
    and open to engage. Always there lend a helping hand when
    called upon and even offers to help when she can see that a
    certain task is a handful. Slow to act on emotions and
    impulses in order to maintain a healthy work environment for
    everyone around her. Thoughtful and considerate in her
    actions words`,
        },
      ],
    };
  },
};
</script>
<style scoped>
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
  width: 21rem;
  height: 21rem;
}

.card-container {
  margin: 5rem;
}

.front {
  box-sizing: border-box;
  padding: 2rem;
  border-radius: 4px;
  box-sizing: 0 1rem 2rem rgb(0, 0, 0, 0.25);
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
  .title {
    font-size: 2.5rem;
    margin-bottom: 0rem;
    padding-top: 2rem;
    padding-bottom: 1rem;
  }
  .title::before {
    width: 14rem;
  }
  .card-container,
  .front,
  .back {
    width: 17rem;
    height: 21rem;
  }

  .card-container {
    margin: 0rem;
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
    font-size: 0.8rem;
  }
}
</style>
