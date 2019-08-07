<template>
  <div>
    <div class="container payment_status">
      <div class="row top_color">
        <div class="col-sm-2 bg_grey"></div>
        <div class="col-sm-3 bg_orange"></div>
        <div class="col-sm-1 bg_darkblue"></div>
        <div class="col-sm-3 bg_yellow"></div>
        <div class="col-sm-2 bg_darkred"></div>
        <div class="col-sm-1 bg_blue"></div>
      </div>
      <h4 class="title">訂單資訊</h4>
      <div class="progress_bar">
        <div class="dot completed"></div>
        <div class="dash completed">
          <div class="step_content">Step1 選定支付方式</div>
        </div>
        <div class="dot completed"></div>
        <div class="dash">
          <div class="step_content">Step2 輸入信用卡資訊或取得支付代碼</div>
        </div>
        <div class="dot"></div>
      </div>
      <div class="payment_selection">
        <div class="pay_title">選擇付款方式</div>
        <div class="pay_btn selected_step"></div>
        <div class="pay_btn unselected_step"></div>
        <div class="pay_btn unselected_step"></div>
      </div>
    </div>
    <div class="container payment_detail"></div>
  </div>
</template>

<script>
export default {
  name: 'Payment',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

* {
  font-family: Microsoft JhengHei;
}

html, body {
  margin: 0;
  padding: 0;
}

.container {
  width: 100%;
  margin-right: auto;
  margin-left: auto;
}

.payment_status {
  height: 400px;
  background-color: #fff;
}

.payment_detail {
  height: 600px;
  background-color: #DEDEDE;
}

.top_color {
  height: 10px;
  display: flex;
  flex-wrap: wrap;
}
.top_color .bg_grey {
  background-color: #B3ABA6;
}
.top_color .bg_orange {
  background-color: #FF8F14;
}
.top_color .bg_darkblue {
  background-color: #173060;
}
.top_color .bg_yellow {
  background-color: #F4B459;
}
.top_color .bg_darkred {
  background-color: #B41F36;
}
.top_color .bg_blue {
  background-color: #62A1D2;
}

.title {
  padding-top: 20px;
  left: 50%;
  transform: translateX(-50%);
  position: absolute;
}

.progress_bar {
  display: flex;
  left: 50%;
  transform: translateX(-50%);
  position: absolute;
  margin-top: 70px;
}
.progress_bar .dot {
  height: 20px;
  width: 20px;
  border-radius: 50%;
  flex-direction: row;
  z-index: 99;
  background-color: #B3ABA6;
}
.progress_bar .dash {
  margin: 9px -5px;
  height: 3px;
  width: 350px;
  background-color: #B3ABA6;
  position: relative;
}
.progress_bar .dash .step_content {
  margin-top: 15px;
  left: 50%;
  transform: translateX(-50%);
  position: absolute;
  font-size: 12px;
  color: #B3ABA6;
}
.progress_bar .completed {
  background-color: #62A1D2;
  position: relative;
}
.progress_bar .completed .step_content {
  left: 50%;
  transform: translateX(-50%);
  font-size: 12px;
  color: #62A1D2;
  margin-top: 15px;
}

.payment_selection {
  padding-top: 140px;
  display: flex;
}
.payment_selection .pay_title {
  color: #62A1D2;
  margin-bottom: 20px;
  padding: 20px;
}
.payment_selection .pay_btn {
  height: 130px;
  width: 290px;
  border-radius: 10px;
  flex-direction: row;
  margin: 0px 30px 0px 0px;
}
.payment_selection .selected_step {
  background-color: #173060;
}
.payment_selection .unselected_step {
  border: 2px solid #62A1D2;
}
</style>
