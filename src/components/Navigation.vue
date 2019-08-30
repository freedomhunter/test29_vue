<template>
    <div id="navigation">
        <div id="mySidenav" class="sidenav">
            <a href="javascript:void(0)" class="closebtn" v-on:click="close">&times;</a>
            <div class="menuBtn">
              <a href="#">About</a>
              <a href="#">Services</a>
              <a href="#">Clients</a>
              <a href="#">Contact</a>
            </div>
        </div>
        <span style="font-size:30px;cursor:pointer;color:white" v-on:click="open">&#9776;</span>
    </div>
</template>

<script>
export default {
    name: 'Navigation',
    methods:{
        open: function openNav() {
            document.getElementById("mySidenav").style.width = "100%";
        },
        close: function closeNav() {
            document.getElementById("mySidenav").style.width = "0";
        }
    }
}

</script>

<style scoped>
.menuBtn {
  width: 80%;
  margin: auto;
  display: flex;
  height: 100vh;
}
.menuBtn a{
  flex: 2;
  height: fit-content;
  margin: auto;
  border-radius: 20px;
  padding: 5% !important;
  margin-left: 2%;
  background-color: black;
  box-shadow: 0px 10px 20px black;;
  margin-right: 2%;
}

.sidenav {
  height: 100%;
  width: 0;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  background-color: #111;
  overflow-x: hidden;
  transition: 0.5s;
  text-align:center;
}

.sidenav a {
  padding: 8px 8px 8px 32px;
  text-decoration: none;
  font-size: 25px;
  color: #fff;
  display: block;
  transition: 0.3s;

}

.sidenav a:hover{
  color: #f1f1f1;
}

.sidenav .closebtn {
  position: absolute;
  top: 0;
  right: 25px;
  font-size: 36px;
  margin-left: 50px;
}

@media screen and (max-height: 450px) {
  .sidenav {padding-top: 15px;}
  .sidenav a {font-size: 18px;}
}
</style>