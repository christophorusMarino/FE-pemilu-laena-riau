<template>
  <div>
    <v-card flat>
      <v-tabs grow v-model="currentTab">
        <v-tab href="#DPR_RI"> Ir. H. MOHAMAD IDRIS LAENA, M.H </v-tab>
        <v-tab href="#DPRD_KOTA"> Drs. M. JAMIL LAENA </v-tab>

        <v-tabs-items v-model="currentTab">
          <v-tab-item value="DPR_RI">
            <load-data-tabulasi-dpr-ri :layer="currentTab" />
          </v-tab-item>
          <v-tab-item value="DPRD_KOTA">
            <load-data-tabulasi-dprd-kota />
          </v-tab-item>
        </v-tabs-items>
      </v-tabs>
    </v-card>
  </div>
</template>
  
  <script>
import LoadDataTabulasiDprdKota from "./DprdKota/load-data-tabulasi-dprd-kota.vue";
import loadDataTabulasiDprRi from "./DprRi/load-data-tabulasi-dpr-ri.vue";

export default {
  components: {
    loadDataTabulasiDprRi,
    LoadDataTabulasiDprdKota,
  },
  data: () => ({
    currentTab: "DPR_RI",
  }),
};
</script>