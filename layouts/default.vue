<template>
  <div>
    <el-container>
      <el-col :span="4" style="background: black;">
        <MainMenu/>
      </el-col>
      <el-col :span="20">
        <el-header>
          <div style="padding-left:20px">
            <span v-on:click="collapseSidebar()">
              <i class="fas fa-bars"></i>
            </span>
            <h2><span class='el-icon-folder-opened'> MaxonErp</span></h2>
            <h5>Software Bisnis</h5>
          </div>           
        </el-header>

        <el-row>
            <el-col :span="24" style="padding-left:20px;background: white;
    border: 1px solid gray;">
              <nuxt />
            </el-col>
        </el-row>
      </el-col>
    </el-container>
  </div>
</template>

<script>
  import MainMenu from '~/components/Menu.vue'
  export default {
    components:{
      MainMenu
    },
    methods: {
      selected(){
          console.log('DialogItem.selected')
      },
      handleClose(){
          console.log('DialogItem.handleClose')
      },
      selectItem(){
          console.log('DialogItem.selectItem')
      },


    }
  };
</script>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
.el-header {
    color: white;
    background-color: #000000;
    border-bottom: #f56c6c 2px solid;
}
.el-menu-item a {
    color: white;
    text-decoration: none;
}
.el-container {
  min-height: 900px;
}
</style>
