<template>
  <div class="personal">
    <div class="leftText">
        <div style="text-align: left; margin-left: 3em;">
          <div style="margin: 1em; font-size: 2em;">{{ rname }}</div>
          <div style="margin: 1em;">{{ desc }}</div>
        </div>
    </div>
    <div class="rightImg" style="display:flex; justify-content:center; max-height: 300px;">
      <img :src="imgUrl" style="width: 100%;height: 100%; border-radius: 5px;">
    </div>
  </div>
</template>

<script>
export default {
  name: 'Personal',
  props: {
    rname: String,
    desc: String,
    imgUrl: String,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.personal {
  display: flex;
  margin: 1em;
  border-radius: 0.5em;
}
.leftText {
  color: white;
  flex: 3;
}

.rightImg {
  flex: 1;
}
</style>
