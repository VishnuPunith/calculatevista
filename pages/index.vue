<template>
  <body>
  <div>
    <div class="container">
    <nav class="side">
      <div class="button">
        <el-dropdown>
          <el-button type="primary" class="font">
            Conversion Tool<i class="el-icon-arrow-down el-icon--right"></i>
          </el-button>
          <el-dropdown-menu slot="dropdown" class="drop">
            <el-dropdown-item><router-link to="/cmtokm" class="textd">M to Km</router-link></el-dropdown-item>
            <el-dropdown-item><router-link to="/cmtom" class="textd">Convert Cm to M</router-link></el-dropdown-item>
            <el-dropdown-item><router-link to="/AC_to_DC" class="textd">AC to DC Converter</router-link></el-dropdown-item>
            <el-dropdown-item><router-link to="/inchtofeet" class="textd">Inch to Feet</router-link></el-dropdown-item>
            <el-dropdown-item><router-link to="/sqtoac" class="textd"> Square Meter to Acre</router-link></el-dropdown-item>
            <el-dropdown-item><router-link to="/decimaltofr" class="textd"> Decimal to Friction</router-link></el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
        <el-dropdown>
          <el-button type="primary" class="font">
            Physics Calculator<i class="el-icon-arrow-down el-icon--right"></i>
          </el-button>
          <el-dropdown-menu slot="dropdown" class="drop">
            <el-dropdown-item><router-link to="/wavelength" class="textd">Wave Length Calculator</router-link></el-dropdown-item>
            <el-dropdown-item><router-link to="/work" class="textd">Work Calculator</router-link></el-dropdown-item>
            <el-dropdown-item>Total Work Calculator</el-dropdown-item>
            <el-dropdown-item>Pressure Calculator</el-dropdown-item>
            <el-dropdown-item>Power Calculator</el-dropdown-item>
            <el-dropdown-item>Ohms Law Calculator</el-dropdown-item>
            <el-dropdown-item>Mass Calculator</el-dropdown-item>
            <el-dropdown-item>Kinetic Energy Calculator</el-dropdown-item>
            <el-dropdown-item>Gravity Calculator</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
        <el-dropdown>
          <el-button type="primary" class="font">
          Basic Calculator<i class="el-icon-arrow-down el-icon--right"></i>
          </el-button>
          <el-dropdown-menu slot="dropdown" class="drop">
            <el-dropdown-item>Addition Calculator</el-dropdown-item>
            <el-dropdown-item>Subtraction Calculator</el-dropdown-item>
            <el-dropdown-item>Multiplication Calculator</el-dropdown-item>
            <el-dropdown-item>Division Calculator</el-dropdown-item>
            <el-dropdown-item>Sqaure Root Calculator</el-dropdown-item>
            <el-dropdown-item>Percentage Calculator</el-dropdown-item>
            <el-dropdown-item>Profit Calculator</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
        <el-dropdown>
          <el-button type="primary" class="font">
            Math Calculator<i class="el-icon-arrow-down el-icon--right"></i>
          </el-button>
          <el-dropdown-menu slot="dropdown" class="drop">
            <el-dropdown-item>Algebra Calculator</el-dropdown-item>
            <el-dropdown-item>Area Calculator</el-dropdown-item>
            <el-dropdown-item>Trigonometry Calculator</el-dropdown-item>
            <el-dropdown-item>Variable Calculator</el-dropdown-item>
            <el-dropdown-item>Volume Calculator</el-dropdown-item>
            <el-dropdown-item>Triangle Calculator</el-dropdown-item>
            <el-dropdown-item>Surface Area Calculator</el-dropdown-item>
            <el-dropdown-item>Statitics Calculator</el-dropdown-item>
            <el-dropdown-item>Simple Intrest Calculator</el-dropdown-item>
            <el-dropdown-item>Rectangle Calculator</el-dropdown-item>
            <el-dropdown-item>Phythagoream Theorem Calculator</el-dropdown-item>
            <el-dropdown-item>Matrix Calculator</el-dropdown-item>
            <el-dropdown-item>LCM Calculator</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
        <el-dropdown>
          <el-button type="primary" class="font">
            Chemistry Calculator<i class="el-icon-arrow-down el-icon--right"></i>
          </el-button>
          <el-dropdown-menu slot="dropdown" class="drop">
            <el-dropdown-item>Molar Volume Calculator</el-dropdown-item>
            <el-dropdown-item>Chemical Equation Calculator</el-dropdown-item>
            <el-dropdown-item>Chemical Reaction Calculator</el-dropdown-item>
            <el-dropdown-item>Boiling Point Calculator</el-dropdown-item>
            <el-dropdown-item>Nernst Equation Calculator</el-dropdown-item>
            <el-dropdown-item>Ph Calculator</el-dropdown-item>
            <el-dropdown-item>Vapor Pressure Calculator</el-dropdown-item>
            <el-dropdown-item>Molecular Calculator</el-dropdown-item>

          </el-dropdown-menu>
        </el-dropdown>
        <el-row>
          <el-button type="primary" round class="font"><router-link to="/onlinecalc" class="cm"> Online Calculator</router-link></el-button>
        </el-row>
      </div>
    </nav>
    <nuxt />
  </div>
  </div>
</body>
</template>

<script>
export default {
};
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