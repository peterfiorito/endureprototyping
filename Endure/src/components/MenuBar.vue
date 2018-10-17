<template>
  <div class="menu-bar">
    <div class="menu-bar__logo" @click="showMenu">
      <em class="fas fa-bars menu-bar__logo--menu"/>
      <span>LOGO</span>
    </div>
    <div class="menu-bar__logo--menu-alt" v-if="toggle">
      <span>HOME</span>
      <span>JOBS</span>
      <span>ABOUT</span>
      <span>DEPARTMENTS</span>
      <span>CONTACT</span>
    </div>
    <div class="menu-bar__options">
      <button class="menu-bar__button"
      @click="setActive('HOME')"
      :class="{'menu-bar__button-active': active == 'HOME'}">
        <span>HOME</span>
      </button>
      <button class="menu-bar__button"
      @click="setActive('JOBS')"
      :class="{'menu-bar__button-active': active == 'JOBS'}">
        <span>JOBS</span>
      </button>
      <button class="menu-bar__button"
      @click="setActive('ABOUT')"
      :class="{'menu-bar__button-active': active == 'ABOUT'}">
        <span>ABOUT</span>
      </button>
      <button class="menu-bar__button"
      @click="setActive('DEPARTMENTS')"
      :class="{'menu-bar__button-active': active == 'DEPARTMENTS'}">
        <span>DEPARTMENTS</span>
      </button>
      <button class="menu-bar__button"
      @click="setActive('CONTACT')"
      :class="{'menu-bar__button-active': active == 'CONTACT'}">
        <span>CONTACT</span>
      </button>
    </div>
    <div class="menu-bar__search">
      <input class="menu-bar__input" placeholder="SEARCH FOR JOBS BY KEYWORD" />
      <em class="fa fa-search menu-bar__icon" />
    </div>
    <div class="menu-bar__notifications">
      <div class="menu-bar__number--envelope">
        <em class="fa fa-suitcase" />
        <span class="menu-bar__number">1</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MenuBar',
  data () {
    return {
      active: 'HOME',
      toggle: false
    }
  },
  methods: {
    setActive (activeTab) {
      this.active = activeTab
    },
    showMenu () {
      this.toggle === false ? this.toggle = true : this.toggle = false
    }
  }
}
</script>

<style scoped>
.menu-bar{
  position: sticky;
  margin-top: 0;
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  background-color: black;
  color: white;
}
.menu-bar__logo{
  margin-top: auto;
  margin-bottom: auto;
  line-height: 1.5em;
  font-size: 16px;
}
.menu-bar__options{
  font-weight: bold;
  padding: 8px;
  display: none;
}
.menu-bar__button{
  background-color: transparent;
  border: none;
  color: white;
  font-size: 15px;
  padding: 5px;
  font-weight: bold;
}
.menu-bar__button:focus{
  outline: none;
}
.menu-bar__button-active{
  border-bottom: white solid 3px;
}
.menu-bar__search{
  display: flex;
  margin-top: auto;
  margin-bottom: auto;
  height: 2em;
  position: relative;
}
.menu-bar__input{
  padding: 10px;
  min-width: 250px;
}
.menu-bar__icon{
  position: absolute;
  top: 10px;
  font-size: 14px;
  right: 8px;
  color: #9e9e9e;
}
.menu-bar__notifications{
  display: flex;
  margin-top: auto;
  margin-bottom: auto;
}
.menu-bar__number{
  font-size: 12px;
  top: 0px;
  right: -10px;
  font-weight: 900;
  position: absolute;
}
.menu-bar__number--envelope{
  position: relative;
}
.menu-bar__logo--menu-alt{
  background-color: black;
  position: absolute;
  top: 32px;
  padding: 10px;
  width: 100%;
  justify-content: space-around;
  display: flex;
}
@media screen and (min-width: 760px){
  .menu-bar__options{
    display: flex;
  }
  .menu-bar__logo--menu{
    display: none;
  }
}
</style>
