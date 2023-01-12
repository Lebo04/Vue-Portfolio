<template>
  <div
    :style="{
      'background-color': `#E6BBAD`,
    }"
  >
    <h2 class="title">My skills and Education</h2>

    <div class="resume">
      <div class="skills">
        <div class="skills-cont">
          <div class="colu lefty">
            <div class="texty">My creative skills & experiences.</div>
            <p>
              I have done coding for the past year now. I would not say that I
              am experienced in coding but at the moment I have knowledge of
              HTML, CSS, Bootstrap, a bit of JavaScript and MySQL. I love coding
              and I am willing to learn more about it.
            </p>
          </div>
          <div class="colu righty" v-for="item in skills" :key="item">
            <div class="bars">
              <div class="info">
                <span>{{ item.name }}</span>
                <span>{{ item.rate }}</span>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="education">
        <div class="timeline">
          <div class="containery lefty" v-for="item in education1">
            <div class="content">
              <h2>{{ item.year }}</h2>
              <img :src="item.image" width="100" alt="" />
              <p>
                {{ item.place }}
              </p>
            </div>
          </div>
          <div class="containery righty" v-for="item in education2">
            <div class="content">
              <h2>{{ item.year }}</h2>
              <!-- <img :src="item.image" width="150" alt="" /> -->
              <p>
                {{ item.place }}
              </p>
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
      skills: [
        {
          name: "HTML",
          rate: "80%",
        },
        {
          name: "CSS",
          rate: "70%",
        },
        {
          name: "JavaScript",
          rate: "50%",
        },
        {
          name: "Bootstrap",
          rate: "60%",
        },
        {
          name: "MySQL",
          rate: "10%",
        },
        {
          name: "Vuejs",
          rate: "10%",
        },
      ],
      education1: [
        {
          image: "https://i.postimg.cc/sDmvMWSP/Logo-Life-Choices.jpg",
          year: "2022",
          place: `Finished the Technical Support Learnership I was doing. At the
                moment I am doing a Web Development course based in Lansdown.`,
        },
        {
          image: "https://i.postimg.cc/VkJHJjT2/th.jpg",
          year: "2021",
          place: `Late August I got an IT Technical Support Learnership from a
                company called Praesignis based in johannesburg. The Learnership
                was based in Elsies River.`,
        },
        {
          image: "https://i.postimg.cc/Fz2Gc6wq/th.jpg",
          year: "2019",
          place: `I finished my matric with a bachelors degree.`,
        },
        {
          image: "https://i.postimg.cc/C5NkMQSk/South-African-Air-Force.png",
          year: "2017 - 2018",
          place: `I was involved in an Air Force program which is based in
                Milnerton, Cape Town. Graduated and got my certification.`,
        },
        {
          image: "https://i.postimg.cc/Fz2Gc6wq/th.jpg",
          year: "2015",
          place: `Started grade 8 at the Centre of Science and Technology (COSAT
                High School) which is based at the heart of Khayelitsha in
                ILithe Park.`,
        },
      ],
    };
  },
};
</script>
<style scoped>
.resume {
  display: flex;
}
.title {
  padding-top: 3rem;
}
.title {
  position: relative;
  text-align: center;
  font-size: 3rem;
  font-weight: 600;
  margin-bottom: 2rem;
  padding-bottom: 2rem;
}
.title::before {
  content: "";
  position: absolute;
  bottom: 0px;
  left: 50%;
  width: 30rem;
  height: 0.2rem;
  background: #111;
  transform: translateX(-50%);
}
.title::after {
  position: absolute;
  left: 50%;
}
.skills-cont .colu {
  width: calc(50% - 2rem);
}
.skills-cont .lefty .texty {
  font-size: 2.3rem;
  font-weight: 600;
  margin-bottom: 1rem;
}
.skills-cont .lefty p {
  text-align: justify;
}
.skills-cont .lefty a {
  display: inline-block;
  background: crimson;
  color: #fff;
  font-size: 18px;
  font-weight: 500;
  padding: 8px 16px;
  margin-top: 20px;
  border-radius: 6px;
  border: 2px solid crimson;
  transition: all 0.3s ease;
}
.skills-cont .lefty a:hover {
  color: crimson;
  background: none;
}
.skills-cont .righty .info {
  display: flex;
  margin-bottom: 0.1rem;
  align-items: center;
  justify-content: space-between;
}
.skills-cont .righty span {
  font-weight: 600;
  font-size: 1.2rem;
  padding: 1rem;
}

.skills {
  margin-left: 2rem;
}

.timeline {
  padding-top: 1rem;
  padding-bottom: 3rem;
  position: relative;
}

.timeline::after {
  content: "";
  position: absolute;
  width: 0.5rem;
  background-color: #111;
  top: 0;
  bottom: 0;
  left: 50%;
  margin-left: -0.01rem;
  margin-top: 2rem;
}

.content {
  text-align: center;
}

.containery {
  padding: 1rem 2rem;
  position: relative;
  background-color: inherit;
  width: 50%;
}

.containery::after {
  content: "";
  position: absolute;
  width: 1.5rem;
  height: 1.5rem;
  right: -1rem;
  background-color: white;
  border: 0.2rem solid crimson;
  top: 0.9rem;
  border-radius: 50%;
  z-index: 1;
}

.lefty {
  left: 0;
}

.content {
  padding: 1rem 2rem;
  background-color: white;
  position: relative;
  border-radius: 1rem;
}

@media screen and (max-width: 300px) {
  .resume {
    flex-direction: column;
  }
  .title {
    padding-top: 1rem;
  }
  .title {
    font-size: 2.2rem;
    font-weight: 600;
    margin-bottom: 2rem;
    padding-bottom: 2rem;
  }
  .title::before {
    width: 13rem;
  }
  .skills-cont .colu {
    width: calc(90% - 1rem);
  }
  .skills-cont .lefty .texty {
    font-size: 1.5rem;
    font-weight: 600;
    margin-bottom: 0.5rem;
  }
  .skills-cont .lefty a {
    display: inline-block;
    background: crimson;
    color: #fff;
    font-size: 18px;
    font-weight: 500;
    padding: 8px 16px;
    margin-top: 20px;
    border-radius: 6px;
    border: 2px solid crimson;
    transition: all 0.3s ease;
  }
  .skills-cont .lefty a:hover {
    color: crimson;
    background: none;
  }
  .skills-cont .righty .info {
    margin-bottom: 0rem;
  }
  .skills-cont .righty span {
    font-weight: 500;
    font-size: 1.2rem;
    padding: 0.2rem;
  }
  .skills-cont .righty i {
    padding-right: 2rem;
    font-size: 4rem;
  }
  
  .skills {
    margin-left: 1.5rem;
  }
  
  .timeline {
    padding-top: 3rem;
    padding-bottom: 2rem;
    position: relative;
  }
  
  .timeline::after {
    content: "";
    position: absolute;
    width: 0.3rem;
    left: 80.5%;
    margin-left: -0.01rem;
    margin-top: 5rem;
  }
  
  .containery {
    padding: 1rem 1rem;
    width: 80%;
  }
  
  .content {
    padding: 2rem 1rem;
  }
}
</style>
