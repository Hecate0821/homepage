
<template>
  <div class = "index" style="height: 100%;">
    <el-container>
      <el-header style="background-color: white; height: 60px; width: 100%">
        <img src="./assets/logo.png" style="height: 60px">
      </el-header>
      <el-main>
        <div style="height: 50px"></div>
        <el-row justify="center" padding = "100">
          <div style="height: 80px"></div>
          <el-col span = "6"><el-button type="primary" @click ="jump_super_user">I'm super-user</el-button></el-col>
        </el-row>
        <el-row justify="center">
          <div style="height: 80px"></div>
          <el-col span = "6"><el-button type="success" @click ="jump_admin">I'm administrator</el-button></el-col>
        </el-row>
        <el-row  justify="center">
          <div style="height: 80px"></div>
          <el-col span = "6"><el-button type="info" @click ="jump_staff">I'm library staff</el-button></el-col>
        </el-row>
        <el-row justify="center">
          <div style="height: 80px"></div>
          <el-col span = "6"><el-button type="warning" @click ="jump_patron">I'm patron</el-button></el-col>
        </el-row>
        <el-carousel :interval="4000" type="card" height="300px">
          <el-carousel-item v-for="item in imagebox" :key="item.id">
            <img :src="item.idView" class="image" style="height: 100%; width: 100%">
          </el-carousel-item>
        </el-carousel>
      </el-main>
      <el-footer style="background-color: white; height: 40px; width: 100%">
        <div style="display: flex; justify-content: center; align-items:center;">
          Novel Nook Class 4 Group D1
        </div>

      </el-footer>
    </el-container>
  </div>
</template>

<script>
export default {
  data() {
    return {

      imagebox: [
        {id: 0, idView: ('https://tse4-mm.cn.bing.net/th/id/OIP-C.EUGyegU3gRmen-Pct2Uy6AHaFI?pid=ImgDet&rs=1')},
        {id: 1, idView: ('https://ts1.cn.mm.bing.net/th/id/R-C.669dc1e23297fd9f0c0c6fd215240762?rik=%2bEOadGUpEdsXsg&riu=http%3a%2f%2fwww.waterlooassociation.org.uk%2fwp-content%2fuploads%2f2018%2f07%2fLondon-The_British_Library1997-Colin_St_John_Wilson.jpg&ehk=meK6duOQfmrDDmFFKpRImmHbQ1kiXM%2fhSW0mzxg3eK4%3d&risl=&pid=ImgRaw&r=0')},
        {id: 2, idView: ('https://tse3-mm.cn.bing.net/th/id/OIP-C.xmU8YKL-SZi2BDSog2bGTwHaCz?w=318&h=132&c=7&r=0&o=5&dpr=2&pid=1.7')},
        {id: 3, idView: ('https://tse1-mm.cn.bing.net/th/id/OIP-C.tRzlYPjCX7ePfO-u-RrlawHaE8?w=245&h=180&c=7&r=0&o=5&dpr=2&pid=1.7')},
        {id: 4, idView: ('https://tse2-mm.cn.bing.net/th/id/OIP-C.onFIutzPPw-XOprpUwVv9wHaE9?w=272&h=182&c=7&r=0&o=5&dpr=2&pid=1.7')},
        {id: 5, idView: ('https://tse4-mm.cn.bing.net/th/id/OIP-C.-M2AAchZQu0UCgoAqrn9UwHaEi?w=312&h=191&c=7&r=0&o=5&dpr=2&pid=1.7')},
        {id: 6, idView: ('https://tse3-mm.cn.bing.net/th/id/OIP-C.ZDe3wLcMBmfYLv33nEKEggHaEf?w=277&h=180&c=7&r=0&o=5&dpr=2&pid=1.7')},
        {id: 7, idView: ('https://tse2-mm.cn.bing.net/th/id/OIP-C.wRRrqHW1eoNubquaq9YGHgHaDa?w=347&h=160&c=7&r=0&o=5&dpr=2&pid=1.7')}

      ],

    }
  },
  methods: {
    jump_super_user() {
      window.location.href = "../super_user/login.html"
    },

    jump_admin() {
      window.location.href = "../admin/log.html"
    },

    jump_staff() {
      window.location.href = "../staff/login.html"
    },

    jump_patron() {
      window.location.href = "../patron/index.html"
    },


  },

  mounted() {

  }
}
</script>


<style>
html,body,#app,.el-container,index
{
  height: 100%;
  margin: 0;
  padding: 0;
}

.index{
  min-height:calc(100vh-60px);
/*  display:flex;
  flex-direction:column;
  align-items:center;*/
  justify-content:center;
  background-image:url('./assets/library.jpg');
  background-size:cover;
  background-position:center;
}

.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 200px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n+1) {
  background-color: #d3dce6;
}

</style>





