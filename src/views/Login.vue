<template lang="pug">
    div.md-layout
        div.md-layout-item
            img.bg(src="../assets/bg.svg" width="70%")
            h3.title  Login with
            div.login-item-wrapper
              //- div.login-item
              //-   a(href="http://www.github.com" target="_blank")
              //-     img(src="../assets/github.svg")
              //-     h4.login-item-title  Github
              div.login-item(v-for="item in loginItems" :key="item.key")
                a(href="https://www.github.com" target="_blank")
                  img(:src="item.img")
                  h4.login-item-title Github

</template>

<script>
// let imgPath = "/img/github.svg";
export default {
  data() {
    return {
      loginItems: [
        {
          name: "Github",
          img: require("../assets/github.svg")
        },
        // {
        //   name: "Github",
        //   img: require("../assets/github.svg")
        // },
        // {
        //   name: "Github",
        //   img: require("../assets/github.svg")
        // }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.bg {
  margin-top: -3%;
}
.monitor {
  position: absolute;
  margin-left: auto;
  margin-right: auto;
  left: 0;
  right: 0;
  z-index: 10;
}
.lock {
  position: absolute;
  margin-left: auto;
  margin-right: auto;
  left: 0;
  right: 0;
  top: 50%;
  z-index: 20;
}
.title {
  color: white;
  font-size: 40px;
  position: absolute;
  margin-left: auto;
  margin-right: auto;
  top: 10%;
  left: 0;
  right: 0;
  z-index: 100;
}
.login-item-wrapper {
  position: absolute;
  margin-left: auto;
  margin-right: auto;
  top: 25%;
  left: 0;
  right: 0;
  z-index: 100;
  width: 50%;
  height: 30%;

  .login-item {
    display: inline-block;
    margin: 5%;
  }
  .login-item-title {
    // margin-top: -2%;
    color: white;
  }
  a:hover {
    color: black;
  }
}
</style>