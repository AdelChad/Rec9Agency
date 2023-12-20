<template>
  <div class="content">
    <div v-for="service in services" :key="service" class="service">

        <p class="paragraph">{{service.text}}</p>
        <img :src="service.img" class="illustration">

    </div>
  </div>
</template>

<script>
export default{
  data() {
      return {
          services:[
              {
                  text: "Text Text Text Text Text Text Text Text Text Text Text Text Text Text Text Text Text Text Text",
                  
              },
              {
                  text: "Text Text Text Text Text Text Text Text Text Text Text Text Text Text Text Text Text Text Text",
                 
              },
              {
                  text: "Text Text Text Text Text Text Text Text Text Text Text Text Text Text Text Text Text Text Text",
              },
          ]
      }
  },
}
</script>

<style lang="scss" scoped>
.content{
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  position: absolute;
  display: flex;
  flex-direction: column;
  gap: 50px;
}

.service{
  opacity: 0;
  align-items:center;
  display: flex;
  border: solid;
  width: fit-content;
  height: fit-content;
  border-image: #222222;
  border-image-slice: 1;
  border-width: 2px;
  border-radius: 15px;

  &:nth-child(even){
      animation: fadeInRight 1000ms forwards;
  }
  &:nth-child(odd){
      animation: fadeInLeft 1000ms forwards;
  }

  @for $i from 1 through 4 {
      &:nth-child(#{$i}) {
        animation-delay: #{$i * 300}ms;
        animation-duration: 1000ms;
      }
  }
}


@keyframes fadeInLeft {
  from{
      opacity: 0;
      transform: translateX(-100%);
  }
  to{
      opacity: 1;
      transform: translateX(-25%);
  }
}

@keyframes fadeInRight {
  from{
      opacity: 0;
      transform: translateX(100%);
  }
  to{
      opacity: 1;
      transform: translateX(25%);
  }
}

.paragraph{
  margin-left: 2vw;
  font-size: 1.2vw;
  width: 35vw;
  color: rgb(0, 0, 0);
}

.illustration{
  margin-top: 1vw;
  margin-bottom: 1vw;
  margin-right: 2vw;
  margin-left: 2vw;
  width: 10vw;
}
</style>