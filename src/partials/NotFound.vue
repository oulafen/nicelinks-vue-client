<template>
  <div class="error-404">
    <div class="error-404-body">
      <el-card>
        <div class="error-404-body-title">
          <span class="left-four">4</span>
          <span class="zero center-zero"><span class="screen-reader-text">0</span></span>
          <span class="right-four">4</span>
        </div>
        <p class="error-404-body-message">YOU&nbsp;&nbsp;LOOK&nbsp;&nbsp;LOST</p>
        <div class="error-404-btns">
          <el-button @click="onGoHomeClick" :plain="true" size="large" type="info">
          返回首页
          </el-button>
          <el-button @click="onBackPageClick" :plain="true" size="large" ttype="info">返回上一页
          </el-button>
        </div>
      </el-card>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Error404',

  methods: {
    onBackPageClick () {
      this.$router.go(-1)
    },
    onGoHomeClick () {
      this.$router.push('/')
    }
  }
}
</script>

<style type="text/css" lang="scss">
.screen-reader-text {
  position: absolute;
  top: -9999em;
  left: -9999em;
}
.zero {
  display: inline-block;
  position: relative;
  vertical-align: middle;
  width: 120px;
  height: 120px;
  border-radius: 999px;
}
.zero:before,
.zero:after {
  border-radius: 0%;
  content:"";
  position: absolute;
  top: 0; left: 0;
  width: inherit; height: inherit;
  border-radius: 999px;
  box-shadow: inset 30px 0 0 rgba(209, 242, 165, 0.4),
    inset 0 30px 0 rgba(239, 250, 180, 0.4),
    inset -30px 0 0 rgba(255, 196, 140, 0.4),
    inset 0 -30px 0 rgba(245, 105, 145, 0.4);
  animation: shadowsdancing 4s infinite;
}

@keyframes shadowsdancing {
  0% {
    box-shadow: inset 30px 0 0 rgba(209, 242, 165, 0.4),
        inset 0 30px 0 rgba(239, 250, 180, 0.4),
        inset -30px 0 0 rgba(255, 196, 140, 0.4),
        inset 0 -30px 0 rgba(245, 105, 145, 0.4);
  }
  25% {
    box-shadow: inset 30px 0 0 rgba(245, 105, 145, 0.4),
        inset 0 30px 0 rgba(209, 242, 165, 0.4),
        inset -30px 0 0 rgba(239, 250, 180, 0.4),
        inset 0 -30px 0 rgba(255, 196, 140, 0.4);
  }
  50% {
     box-shadow: inset 30px 0 0 rgba(255, 196, 140, 0.4),
        inset 0 30px 0 rgba(245, 105, 145, 0.4),
        inset -30px 0 0 rgba(209, 242, 165, 0.4),
        inset 0 -30px 0 rgba(239, 250, 180, 0.4);
  }
  75% {
   box-shadow: inset 30px 0 0 rgba(239, 250, 180, 0.4),
        inset 0 30px 0 rgba(255, 196, 140, 0.4),
        inset -30px 0 0 rgba(245, 105, 145, 0.4),
        inset 0 -30px 0 rgba(209, 242, 165, 0.4);
  }
  100% {
    box-shadow: inset 30px 0 0 rgba(209, 242, 165, 0.4),
        inset 0 30px 0 rgba(239, 250, 180, 0.4),
        inset -30px 0 0 rgba(255, 196, 140, 0.4),
        inset 0 -30px 0 rgba(245, 105, 145, 0.4);
  }
}
@keyframes colordancing {
  0% {
    color: #D1F2A5;
  }
  25% {
    color: #F56991;
  }
  50% {
    color: #FFC48C;
  }
  75% {
    color: #EFFAB4;
  }
  100% {
    color: #D1F2A5;
  }
}
@keyframes colordancing2 {
  0% {
    color: #FFC48C;
  }
  25% {
    color: #EFFAB4;
  }
  50% {
    color: #D1F2A5;
  }
  75% {
    color: #F56991;
  }
  100% {
    color: #FFC48C;
  }
}


@keyframes error-404-animation {
  0% {
    transform: rotateZ(0deg);
  }
  20% {
    transform: rotateZ(60deg);
  }
  40% {
    transform: rotateZ(10deg);
  }
  60% {
    transform: rotateZ(-50deg);
  }
  80% {
    transform: rotateZ(20deg);
  }
  100% {
    transform: rotateZ(0deg);
  }
}

@keyframes left-four-animation {
  0% {
    transform: translateX(0);
    color: #D1F2A5;
  }
  20% {
    transform: translateX(0);
    color: #F56991;
  }
  40% {
    transform: translateX(0);
    color: #FFC48C;
  }
  60% {
    transform: translateX(-50px);
    color: #F56991;
  }
  80% {
    transform: translateX(-20px);
    color: #D1F2A5;
  }
  100% {
    transform: translateX(0);
    color: #FFC48C;
  }
}
@keyframes right-four-animation {
  0% {
    transform: translateX(0);
    color: #FFC48C;
  }
  20% {
    transform: translateX(60px);
    color: #EFFAB4;
  }
  40% {
    transform: translateX(40px);
    color: #D1F2A5;
  }
  60% {
    transform: translateX(0px);
    color: #F56991;
  }
  80% {
    transform: translateX(10px);
    color: #FFC48C;
  }
  100% {
    transform: translateX(0);
    color: #D1F2A5;
  }
}

.error-404{
  width: 100%;
  height: 100%;
  background-color: #000;
  .error-404-body {
    width: 96%;
    max-width: 600px;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    padding: 20px 0;
    .error-404-body-title{
      text-align: center;
      font-size: 7rem;
      font-weight: 700;
      color: #FFC48C;
      height: 13rem;
      line-height: 13rem;
      .center-zero{
        display: inline-block;
        animation: error-404-animation 3s ease 0s infinite alternate;
        margin: 0 -2rem;
      }
      .left-four{
        margin: 0;
        display: inline-block;
        animation: left-four-animation 3s ease 0s infinite alternate;
      }
      .right-four{
        margin: 0;
        display: inline-block;
        animation: right-four-animation 3s ease 0s infinite alternate;
      }
    }
    .error-404-body-message {
      display: block;
      text-align: center;
      font-size: 1rem;
      font-weight: 500;
      letter-spacing: 12px;
      color: #dddde2;
    }
  }
}

@media (max-width:375px) {
  .el-card__body{
    padding: 10px 0;
  }
  .error-404-body{
    background-color: #000;
    .error-404-body-title{
      height: 12rem;
      font-size: 6rem;
    }
  }
}
</style>
