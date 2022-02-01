<template>
  <div class="post">
      <div class="leftText">
        <div style="text-align: left; padding-left: 4em;">
          <p>你的对手是</p>
          <p>神圣兽国游尾郡</p>
          <p>窝窝乡独行族妖侠</p>
          <p style="color: red;">魁拔</p>
        </div>
      </div>
      <div class="rightImg">
        <img src="../assets/KB/maimen.png" style="max-width: 100%;max-height: 100%;">
      </div>
  </div>
</template>

<script>
export default {
  name: 'post',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
p{
  font-size: 3em;
}
.post {
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 0.5em;
  width: 100vw;
  height: 100vh;
}
.leftText {
  color: white;
  flex: 1;
}

.rightImg {
  flex: 1;
}
</style>
