<template>
  <v-app-bar style="height: 56px; background-color: rgb(241, 236, 236)">
    <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
    <v-app-bar-title>
      <img height="auto" width="140px" src="../assets/logo.png" />
    </v-app-bar-title>
    <v-spacer></v-spacer>
    <!-- Filtro Aqui Encima-->
    <Input_filter />
    <v-spacer></v-spacer>
    <v-btn icon="mdi-theme-light-dark"></v-btn>
    <v-btn style="height: 40px; width: 10px; font-size: 20px">
      <v-badge color="rgb(244, 16, 0)" dot
        ><v-icon icon="mdi-bell-outline"></v-icon></v-badge
    ></v-btn>
    <!-- Componente Do Perfil de Usúario  -->
    <ProfileButtom />
  </v-app-bar>
  <v-card>
    <v-navigation-drawer
      style="height: 100%; background-color: rgb(229, 231, 231); width: 228px"
      floating
      permanent
      v-model="drawer"
    >
      <v-list density="compact" style="padding: 0px; margin: auto" nav>
        <v-list-item
          prepend-icon="mdi-chart-bar"
          value="dashboard"
          title="Dashboard"
        >
        </v-list-item>
        <v-list-item
          prepend-icon="mdi-phone-plus-outline"
          value="atendimento"
          title="Atendimento"
        ></v-list-item>
        <v-list-item
          prepend-icon="mdi-domain"
          value="empresas"
          title="Empresas"
        ></v-list-item>
        <v-list-item
          prepend-icon="mdi-account-multiple-outline"
          value="clientes"
          title="Clientes"
        ></v-list-item>
        <v-list-item
          prepend-icon="mdi-ticket-outline "
          value="tickets"
          title="Tickets"
        ></v-list-item>
        <v-list-item
          prepend-icon="mdi-newspaper-variant-multiple-outline"
          value="campanhas"
          title="Campanhas"
        ></v-list-item>
        <v-list-item
          prepend-icon="mdi-application-outline"
          value="quadros"
          title="Quadros"
        ></v-list-item>
        <v-list-item
          prepend-icon="mdi-chat-processing-outline"
          value="chat"
          title="Chat interno"
        ></v-list-item>
        <v-list-item
          prepend-icon="mdi-cog-outline"
          title="Configurações"
          value="config"
          append-icon="mdi-chevron-down"
        ></v-list-item>
        <v-list-item
          prepend-icon="mdi-note-text-outline"
          title="Relatórios"
          value="relat"
          append-icon="mdi-chevron-down"
        ></v-list-item>
      </v-list>
      <div
        style="
        top: 75px;
          display: flex;
          flex-direction: column;
          align-items: center;
          position: relative;
          bottom: 0;
          right: 0;
          padding: 20px;
        "
      >
        <p>powered by</p>
        <img src="../assets/logonpx.png" class="img_logonpx" alt="" />
      </div>
    </v-navigation-drawer>
  </v-card>
</template>

<script setup>
const drawer = ref(false);
</script>

<style scoped>

 .v-list-item__prepend , .v-list-item__spacer  {


width: 12px;
}

.img_logonpx {
  width: 120px;
  height: auto;
  justify-content: end;
}

.v-list .v-list-item--nav:not(:only-child) {
  margin-bottom: 0px;
}

.v-list-item--rounded {
  border-radius: 0px;
}
.v-list-item--nav {
  padding-inline-start: 8px;
  padding-inline-end: 18px;
}

.v-list-item--active:focus {
  color: orangered;
  background-color: white;
}

.v-list-item--variant-text:focus {
  background-color: white;
  color: orangered;
  border-left: 4px solid orangered;
}

.v-theme--light {
  --v-activated-opacity: 0;
}
</style>
