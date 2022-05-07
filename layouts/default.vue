<template>
  <div class='app'>
    <link href='https://unpkg.com/boxicons@2.1.2/css/boxicons.min.css' rel='stylesheet'>

    <vs-navbar shadow square center-collapsed v-model="active">
      <template #left>
        <!-- <vs-button @click="activeSidebar = !activeSidebar" flat icon>
          <i class="mdi mdi-sword-cross"></i>
        </vs-button> -->
      </template>

      <!-- <vs-navbar-item :active="active == 'guide'" id="guide">
          pirooz jenabi
        </vs-navbar-item> -->

      <template #right>
        <vs-button 
        gradient
        style="min-width: 100px"
        animation-type="scale"
        >
          Hire me
        <template #animate >
          <i class='bx bx-mail-send' ></i>
        </template>

        </vs-button>
        <vs-button>Developer Tools</vs-button>
        <vs-button>Blog</vs-button>
      </template>
    </vs-navbar>
    <vs-sidebar 
    absolute 
    v-model="active" 
    :open.sync="activeSidebar" 
    reduce
    hover-expand
    >
      <template #logo>
        <!-- ...img logo -->
      </template>
      <vs-sidebar-item id="home">
        <template #icon>
          <i class="bx bx-home"></i>
        </template>
        Home
      </vs-sidebar-item>
      <vs-sidebar-item id="market">
        <template #icon>
          <i class="bx bx-grid-alt"></i>
        </template>
        Blog
      </vs-sidebar-item>
      <vs-sidebar-item id="Music">
        <template #icon>
          <i class="bx bx-code-alt"></i>
        </template>
        Short Codes
      </vs-sidebar-item>
      <!-- <vs-sidebar-group>
        <template #header>
          <vs-sidebar-item arrow>
            <template #icon>
              <i class="bx bx-group"></i>
            </template>
            Social media
          </vs-sidebar-item>
        </template>

        <vs-sidebar-item id="Instagram">
          <template #icon>
            <i class="bx bxl-instagram"></i>
          </template>
          Instagram
        </vs-sidebar-item>
        <vs-sidebar-item id="twitter">
          <template #icon>
            <i class="bx bxl-twitter"></i>
          </template>
          Twitter
        </vs-sidebar-item>
        <vs-sidebar-item id="Facebook">
          <template #icon>
            <i class="bx bxl-facebook"></i>
          </template>
          Facebook
        </vs-sidebar-item>
      </vs-sidebar-group> -->

      <vs-sidebar-item id="donate">
        <template #icon>
          <i class="bx bxs-donate-heart"></i>
        </template>
        Tools
      </vs-sidebar-item>

      <template #footer>
        <vs-row justify="space-between">
          <vs-avatar>
            <img src="/avatars/avatar-5.png" alt="" />
          </vs-avatar>

          <vs-avatar badge-color="danger" badge-position="top-right">
            <i class="bx bx-bell"></i>

            <template #badge> 28 </template>
          </vs-avatar>
        </vs-row>
      </template>
    </vs-sidebar>


    <Nuxt />
  </div>
</template>
<script>
export default {
  data:function (){
    return {
      active: "home",
      activeSidebar: true,
    }
  }
};
</script>
<style>
.app {
  width: 100%;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
