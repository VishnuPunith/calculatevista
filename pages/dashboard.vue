<template>
  <div class="card">
    <div class="drop">
    <DropDown :arrayData='mydata'/>
   <DropDown :arrayData='phyData' />
   <DropDown  :arrayData='chemistryData'/>
   <DropDown />
   <DropDown />
    </div>

  </div>
</template>

<script>
export default {
  name: 'dashboard',
  props: {
    title: {
      type: String,
      default: ''
    }
  },
  data(){
    return{
         mydata:[
                    {
                        links:"/cmtokm",
                        titles:"cmtokm"
                    },
                     {
                        links:"/cmtom",
                        titles:"cmtom"
                    },
                     {
                        links:"/AC_to_DC",
                        titles:"AC_to_DC"
                    },
                     {
                        links:"/inchtofeet",
                        titles:"inchtofeet"
                    },
                     {
                        links:"/sqtoac",
                        titles:"sqtoac"
                    },
                     {
                        links:"/decimaltofr",
                        titles:"decimaltofr"
                    },
                ],
                phyData:[
                    {
                        links:"/wavelength",
                        titles:"Wave Length Calculator"
                    },
                     {
                        links:"/cmtom",
                        titles:"cmtom"
                    },
                     {
                        links:"/AC_to_DC",
                        titles:"AC_to_DC"
                    },
                     {
                        links:"/inchtofeet",
                        titles:"inchtofeet"
                    },
                     {
                        links:"/sqtoac",
                        titles:"sqtoac"
                    },
                     {
                        links:"/decimaltofr",
                        titles:"decimaltofr"
                    },
                ],
                chemistryData:[
                    {
                        links:"/cmtokm",
                        titles:"cmtokm"
                    },
                     {
                        links:"/cmtom",
                        titles:"cmtom"
                    },
                     {
                        links:"/AC_to_DC",
                        titles:"AC_to_DC"
                    },
                     {
                        links:"/inchtofeet",
                        titles:"inchtofeet"
                    },
                     {
                        links:"/sqtoac",
                        titles:"sqtoac"
                    },
                     {
                        links:"/decimaltofr",
                        titles:"decimaltofr"
                    },
                ]
    }
  }
}
</script>

<style scoped>
.drop{
    display: flex;
    justify-content: space-around;
}

</style>