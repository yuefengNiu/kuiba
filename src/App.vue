<template>
  <div>
    <div class="post" style="margin: 2.5em;">
      <Post></Post>
    </div>
    <div style="margin: 2em;" v-for="(item, index) in list" :key="index">
      <Personal :rname="item.rname" :desc="item.desc" :imgUrl="item.imgUrl"></Personal>
    </div>
  </div>
</template>

<script>
import Post from '@/components/Post';
import Personal from '@/components/Personal';

export default {
  name: 'Main',
  components: {
    Post,
    Personal,
  },
  data() {
    return {
      list: [
        {rname: "奇衡三", desc:"基斯卡人，魁拔十二妖之一，最大的兴趣就是迷麟。在探索四代魁拔迷麟身体上奥秘时，奇衡三让士兵给迷麟施加各种刺激，包括用重兵器痛击、用冷水冲击、用矛刺，最后用石头压在迷麟身上，迷麟承受不了巨大的压力，挤出“奇衡三”三个字向其求助，忽然之间，出现了庞大威猛的脉兽，“奇衡三”就此成为魁拔召唤脉兽的口号。和幽弥狂镇守元泱界粼妖祭坛。临死前见到了第六代魁拔的魁拔状态后说出“魁拔？魁拔！魁拔...”，最后受光势打击死去。", imgUrl: require('./assets/KB/qihengsan.jpeg')},
        {rname: "幽弥狂", desc:"雾妖，魁拔十二妖之一，灵山军夜袭小队队长。他还是神圣联军夜战分队小队长的时候，他带领的五名妖侠在暗杀魁拔的战斗中献上了年轻宝贵的生命，但神圣联军却因为他们都是没有纹耀的白身妖侠，拒绝承认他们的联军士兵身份，也就不能被称作“对抗魁拔的一员”而死。幽弥狂不再争辩，只身一人潜入魁拔的营地，在埋葬五个兄弟的地方立了一块木板，在上面写了已逝兄弟的名字和“魁拔的敌人”几个字，并挂上了自己的纹耀。他在墓前默默站了五天五夜。第五夜的下半夜，幽弥狂离开坟墓，向魁拔的营帐走去，他冲进了魁拔的大帐里，却被魁拔一手抓住了他的头!幽弥狂就这样被魁拔抓着头，说出了五个普通的名字，讲述了五位无纹耀战士的生平故事，讲述的语调平静却略带伤感。魁拔听完之后，推开被按在他手掌下的幽弥狂：“大家听好了，白落提、丰和、英宋、桓泽金、广秀，这五个人将因为誓死捍卫故乡、抵抗魁拔而被所有灵山军官兵记住，并视为死敌!”然后只身带着幽弥狂闯入联军营地，杀了驳回幽弥狂申请的联军军官，之后幽弥狂加入灵山军夜袭小队，最后与奇衡三一同受光势打击阵亡。", imgUrl: require("./assets/KB/youmikuang.jpeg")},
        {rname: "海问香", desc:"粼妖，魁拔十二妖之一，魁拔南部战区梅龙尼卡航线护卫部队独立先锋。在自己的家乡的入口万诗之海，看到第四代魁拔的舰队来到她的家乡，遭受重创的舰队本可以在万诗之海布阵与紧追不舍的对手进行决战，第四代魁拔却因为石壁上的情诗深受感动，没有在粼妖的圣地排兵布阵并将其作为战场，而是将船头反向朝强大的敌人而去，年轻的海问香很受感动独自一人追随第四代魁拔。迷麟的舰队离开后，自己也离开星移之海，不远万里跋涉追寻魁拔的足迹，并终于在第三魁拔帝国大厦将倾之时加入灵山军。", imgUrl: require("./assets/KB/haiwenxiang.jpeg")},
        {rname: "远浪", desc:"粼妖，“曲境一号舰”舰长，联军海军上将兼神圣联军涡流岛战区司令官。明明做着最危险的事，却还一副慵懒事不关己的态度。远浪一直喝的是航海饮料，而眼罩的秘密是为了适应到达深海过程中的强光与黑暗的交替，情诗是从一个海盗哥哥那里得到过关暗语。这个从一开始都在懒散的命令着其他人的舰长，其实才是最睿智最有能力的领导者。最后蛮吉大战海问香的时候变身魁拔，远浪成为第一个知道蛮吉身份而且还活着的人。”我的小鱼你醒了，还认识早晨吗？”", imgUrl: require("./assets/KB/yuanlang.png")},
        {rname: "迷麟", desc:"地界未知生物，第四代魁拔。记忆里最早的事情是打雷和闪电，幼年时期被爪云王子发现并一起生活。魁拔1058年，天界神族集中全部兵力向第四代魁拔发起总攻击，魁拔召唤出脉兽和他的部下们一起与天神展开殊死一战，因抵挡不住天神的火力，魁拔在他生命的最后时刻用战器冲天槊打开曲曲之境，将他剩余的十二名部下传送到到距第六代魁拔诞生前20年的时空，这十二人因穿越“曲曲之境”容貌不再衰变，一直保持着穿越时的年龄。冲天槊化作地界涡流岛上巨大的石柱，他的部下守护在那里等待着新一代魁拔的诞生。", imgUrl: require("./assets/KB/milin.jpeg")},
      ],
    };
  }
};
var s=0,x=0;
window.onscroll = function() {
  s=document.documentElement.scrollTop;
    setTimeout(function (){
        x=document.documentElement.scrollTop;
    },1)
    if(s>=x){
      var scrollTop = document.documentElement.scrollTop || document.body.scrollTop;
      if (scrollTop >= 300 && scrollTop < 350) {
        window.scrollTo({ top: document.documentElement.clientHeight, behavior: "smooth" })
      }
    }
    // else{}

  
}
</script>

<style>
</style>
