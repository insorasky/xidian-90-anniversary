<template>
  <div id="app">
    <el-row>
      <el-col :span="24">
        <el-card shadow="hover">
          <div class="top">
            <div class="text">
              <p>西安电子科技大学</p>
              <p>90周年校庆</p>
            </div>
          </div>
        </el-card>
      </el-col>
    </el-row>
    <el-row :gutter="20" class="row">
      <el-col :span="12">
        <el-card shadow="hover" @click.native="showHistory">
          <img src="./assets/history.jpg" alt="西电校史" class="card-img"/>
          <div style="padding: 14px;">
            <span>西电校史</span>
          </div>
        </el-card>
      </el-col>
      <el-col :span="12">
        <el-card shadow="hover" @click.native="showSong">
          <img src="./assets/song.jpg" alt="西电校歌" class="card-img"/>
          <div style="padding: 14px;">
            <span>西电校歌</span>
          </div>
        </el-card>
      </el-col>
    </el-row>
    <el-row :gutter="20" class="row">
      <el-col :span="12">
        <el-card shadow="hover" @click.native="showCampus">
          <img src="./assets/campus.png" alt="西电校园" class="card-img"/>
          <div style="padding: 14px;">
            <span>西电校园</span>
          </div>
        </el-card>
      </el-col>
      <el-col :span="12">
        <el-card shadow="hover" @click.native="showSpirit">
          <img src="./assets/spirit.jpeg" alt="西电精神" class="card-img"/>
          <div style="padding: 14px;">
            <span>西电精神</span>
          </div>
        </el-card>
      </el-col>
    </el-row>
    <el-row class="row">
      <p>1232352563426 某某某</p>
    </el-row>
    <el-dialog title="西电校史" :visible.sync="history" width="60%">
      <el-row :gutter="20" type="flex" align="middle" justify="center">
        <el-col span="18" style="font-size: 22px">
          <p>西安电子科技大学的历史是与中国革命史紧紧相连在一起的。 在中国革命发展的每一个时期， 她都是党中央、中央军委的“千里眼”和“顺风耳”，红色的电波传遍了大江南北。她为革命争夺取全国的胜利建立了不朽的功勋。</p>
          <p>西安电子科技大学的历史是中国电子高等教育史的重要组成部分。战争年代，她自强不息，坚韧不拔，在长征途中，在敌后根据地，处处都留下了她创办现代工程教育的足迹。和平时期，她打破了西方对我国的技术封锁，不屈不挠，创建了我国电子与信息技术领域一批新的学科和专业，为建国后我国自主建设电子与信息学科门类院校积累了丰富的办学经验，进行了必要的人才储备，在中国电子高等教育史上谱写了辉煌篇章。</p>
        </el-col>
        <el-col span="6">
          <img src="./assets/history_map.jpeg" style="max-width: 100%" alt="map"/>
        </el-col>
      </el-row>
    </el-dialog>
    <el-dialog title="西电校歌" :visible.sync="song" width="60%" @close="closeSong">
      <el-row :gutter="20" type="flex" align="middle">
        <el-col span="24" style="font-size: 22px">
          <video src="./assets/song.mp4" style="max-width: 80%; display: block; margin: 0 auto; max-height: 500px" controls="controls" id="song"/>
          <p style="text-align: center; font-size: 30px">西电校歌——《与共和国同行》</p>
          <p>星星之火，照耀着我们，照耀着我们的忠诚。红色电波，辉煌着我们，我们的传统。肩负使命，千锤百炼，我们和共和国，我们和共和国同行。团结勤奋，求实创新，厚德求真，力学笃行。我们是光荣的西电科大人。向着太阳拥抱光明，向着太阳拥抱光明，永远向着太阳。</p>
          <p>艰苦奋斗，传承着我们，传承着我们的校风。英才摇篮，奋发着我们，我们的豪情。开拓创新，走向未来，我们和共和国，我们和共和国同行。绿色校园，百年树人，时代青年，勇攀高峰。我们是新世纪西电科大人。祖国强盛民族复兴，祖国强盛民族复兴，铸造祖国强盛。</p>
        </el-col>
      </el-row>
    </el-dialog>
    <el-dialog title="西电校园" :visible.sync="campus" width="60%">
      <el-row :gutter="20" type="flex" align="middle">
        <el-col span="16" style="font-size: 18px">
          <p>西电是分为两个校区的，南校区和北校区，北校区的建筑大都年代较早，可以一窥当时西电的建筑分格与历史。南校区地处长安，属于新校区，建筑风格新颖独特，可以一窥这个学校的当代与未来。 </p>
          <p>进入北校区，首先映入眼帘的就是著名的主楼，如下图，就是最上边红旗飘飘，左右红色大字是西电的校训，主楼是一座历史悠久的建筑，一楼大厅里就可以看到建筑风格大气优美。主楼的前边是一个雕塑，雕塑寓意在电子科技科技领域中，持续专注与创新的西电作风。同时前边还是一个浅浅的水池，蓝天白云下，倒映着在水池里的雕塑、主楼和天空，显得格外的和谐宁静，仅仅诉说着西电的故事。西电新校区的标志性建筑较多，主要包含观光塔、题字雕塑等。如下图的西电新校区的观光塔，图是一张二次元作品哈，但是大家可以看到这个塔的独特风格，高耸而立，观光塔顶部，远远望去，附近长安的景色尽收眼底，体验美妙。如下图所示是毛泽东主席给西电的题词，西电是一所建立在长征路上的高校，所以具有很深厚的红色背景。这个雕塑在西电南校区东门刚进入便可看到，背景是一个不大的广场，但却宏伟大气，两旁的柱子上镌刻着西电的历史，雕塑上红色大字引人注目。</p>
        </el-col>
        <el-col span="8">
          <img src="./assets/campus1.jpg" alt="campus1" style="width: 100%"/>
          <img src="./assets/campus2.jpeg" alt="campus2" style="width: 100%"/>
        </el-col>
      </el-row>
    </el-dialog>
    <el-dialog title="西电精神" :visible.sync="spirit" width="60%">
      <el-row :gutter="20" type="flex" align="middle">
        <el-col span="16" style="font-size: 20px">
          <p>西电精神永传承，不忘初心跟党走</p>
          <p>办学宗旨：全心全意为人民服务</p>
          <p>办学理念：大师、大爱、大为、大气</p>
          <p>西电精神：艰苦奋斗、自强不息，求真务实、爱国为民</p>
          <p>西电校训：厚德 求真 砺学 笃行</p>
          <p>西电校风：团结 勤奋 求实 创新</p>
          <p>治学风范：崇尚学术、追求卓越</p>
          <p>西电风尚：团结、和谐、包容、进取</p>
        </el-col>
        <el-col span="8">
          <img src="./assets/spirit1.jpeg" alt="spirit1" style="width: 100%"/>
        </el-col>
      </el-row>
    </el-dialog>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {

  },
  data(){
    return {
      history: false,
      song: false,
      campus: false,
      spirit: false,
    }
  },
  methods: {
    showHistory(){
      this.history = true
    },
    showSong(){
      this.song = true
    },
    showCampus(){
      this.campus = true
    },
    showSpirit(){
      this.spirit = true
    },
    closeSong(){
      document.getElementById('song').pause()
    }
  },
  mounted() {
    document.title = "西安电子科技大学90周年校庆"
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  width: 1000px;
  display: block;
  margin: 0 auto;
}
.top{
  background: url("assets/cover.jpg") no-repeat;
  display: block;
  height: 250px;
  margin: 0 auto;
  text-align: right;
  color: #DD0000;
  font-size: 50px;
  line-height: 10px;
}
.text{
  display: block;
  width: 600px;
  margin: auto;
  padding-top: 1px;
}
.card-img{
  width: 100%;
  height: 300px;
}
.row{
  margin: 20px;
}
</style>
