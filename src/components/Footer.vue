<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-box">
        <router-link to="/" class="footer-logo logo">
          <img src="../assets/images/logo.png" alt="logo">
        </router-link>
        <div class="footer-nav">
          <ul>
            <li>Ресторанам</li>
            <li>Курьерам</li>
            <li>Пресс-центр</li>
            <li>Контакты</li>
          </ul>
        </div>
        <div class="footer-socials">
          <img src="../assets/images/inst.png" alt="inst">
          <img src="../assets/images/facebook.png" alt="facebook">
          <img src="../assets/images/VK.png" alt="VK">
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {

}
</script>

<style scoped>
.footer{
  min-height: 156px;
  padding: 60px;
}
.footer-box{
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 100%;
  gap: 36px;
  flex-wrap: wrap;
}
.footer-nav{
  flex-grow: 1;
}
.footer-nav ul{
  display: flex;
  align-items: center;
  list-style: none;
  padding: 0;
  margin: 0;
  gap: 15px;
  flex-wrap: wrap;
}
.footer-nav ul li{
  color: #595959;
  font-size: 18px;
  font-weight: 400;
}
.footer-socials{
  display: flex;
  align-items: center;
  justify-content: flex-end;
  gap: 21px;
}
</style>