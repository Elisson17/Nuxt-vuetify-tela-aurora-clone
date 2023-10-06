<template>
  <v-main class="d-flex align-center justify-center" style="height: auto">
    <v-table style="border-radius: 10px; margin-top: 2%; width: 69%">
      <thead>
        <th
          colspan="3"
          style="padding: 8px; background-color: rgb(229, 226, 226)"
        >
          <h2 style="text-align: left; margin: 0; color: orangered">
            Empresas <v-icon icon="mdi-plus-circle-outline"></v-icon>
          </h2>
        </th>
        <tr>
          <th class="text-left">
            <strong> Empresas</strong>
          </th>
          <th class="text-left">
            <strong> Código Externo</strong>
          </th>
          <th class="text-left">
            <strong>Ações</strong>
          </th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="p in 8"
          :key="p"
          :style="{
            backgroundColor: p % 2 === 0 ? 'rgb(213, 230, 246)' : 'white',
            borderRadius: '10px',
          }"
        >
          <td style="font-size: 13px">Empresas lorem ipsum</td>
          <td style="font-size: 13px">#00000</td>
          <td>
            <v-icon icon="mdi-note-edit-outline"></v-icon
            ><v-icon icon="mdi-trash-can-outline"></v-icon>
          </td>
        </tr>
      </tbody>
    </v-table>
  </v-main>
  <v-pagination size="32px" :length="3"> </v-pagination>
</template>

<script setup></script>

<style lang="css">
.v-pagination__item {
  background-color: rgb(234, 233, 233);
  border-radius: 6px;
 
}
.v-pagination__item--is-active {
  background-color: orangered;
  color: white;
  border-radius: 6px;
}
.mdi-chevron-left::before {
    content: "Anterior";
    font-size: 10.4px;
    font-family: 'Times New Roman';
    
}
.mdi-chevron-right::before {
    content: "Próximo";
    font-size: 10.4px;
    font-family: 'Times New Roman';

}

.v-pagination__prev {
  margin: 0.3rem;
 margin-right: 15px;
}
.v-pagination__next{

  margin: 0.3rem;
 margin-left: 15px;
}
</style>
