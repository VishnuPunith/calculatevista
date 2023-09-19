<template>
  <div class="card">
   <el-dropdown>
          <el-button type="primary" class="font">
            Conversion Tool<i class="el-icon-arrow-down el-icon--right"></i>
          </el-button>
          
          <el-dropdown-menu slot="dropdown" class="drop">

            <el-dropdown-item v-for="x in arrayData" :key="x"><router-link :to="`x.links`" class="textd">{{x.titles}}</router-link></el-dropdown-item>
               </el-dropdown-menu>
        </el-dropdown>
  </div>
</template>

<script>
export default {
  name: 'DropDown',
  props: {
    arrayData: {
      type: Array,
      default: () => []
    },
    title: {
      type: String,
      default: ''
    }
  },
  data(){
    return{
        //  mydata:[
        //             {
        //                 links:"/cmtokm",
        //                 titles:"cmtokm"
        //             },
        //              {
        //                 links:"/cmtom",
        //                 titles:"cmtom"
        //             },
        //              {
        //                 links:"/AC_to_DC",
        //                 titles:"AC_to_DC"
        //             },
        //              {
        //                 links:"/inchtofeet",
        //                 titles:"inchtofeet"
        //             },
        //              {
        //                 links:"/sqtoac",
        //                 titles:"sqtoac"
        //             },
        //              {
        //                 links:"/decimaltofr",
        //                 titles:"decimaltofr"
        //             },
        //         ],
        //         phyData:[
        //             {
        //                 links:"/wavelength",
        //                 titles:"Wave Length Calculator"
        //             },
        //              {
        //                 links:"/cmtom",
        //                 titles:"cmtom"
        //             },
        //              {
        //                 links:"/AC_to_DC",
        //                 titles:"AC_to_DC"
        //             },
        //              {
        //                 links:"/inchtofeet",
        //                 titles:"inchtofeet"
        //             },
        //              {
        //                 links:"/sqtoac",
        //                 titles:"sqtoac"
        //             },
        //              {
        //                 links:"/decimaltofr",
        //                 titles:"decimaltofr"
        //             },
        //         ],
        //         chemistryData:[
        //             {
        //                 links:"/cmtokm",
        //                 titles:"cmtokm"
        //             },
        //              {
        //                 links:"/cmtom",
        //                 titles:"cmtom"
        //             },
        //              {
        //                 links:"/AC_to_DC",
        //                 titles:"AC_to_DC"
        //             },
        //              {
        //                 links:"/inchtofeet",
        //                 titles:"inchtofeet"
        //             },
        //              {
        //                 links:"/sqtoac",
        //                 titles:"sqtoac"
        //             },
        //              {
        //                 links:"/decimaltofr",
        //                 titles:"decimaltofr"
        //             },
        //         ]
    }
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');
body {
  background-color: rgb(234, 241, 241);
  font-family: 'Poppins', sans-serif;
}
.font {
  font-family: 'Poppins', sans-serif;
  font-weight: 500;
  background-color:black;
  border-radius: 12px;
}
.drop{
  border-radius: 12px;
}
.button {
  display: flex;
    gap: 22px;
    justify-content: center;
    padding: 49px;
}
.textd{
  text-decoration: none;
  color: black;
}
.el-dropdown {
  vertical-align: top;
}
.cm{
  text-decoration: none;
  color: aliceblue;
}
.el-dropdown + .el-dropdown {
  margin-left: 15px;
}
.el-icon-arrow-down {
  font-size: 12px;
}

</style>