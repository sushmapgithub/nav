<template>
  <div>
    <v-row no-gutters align="center" justify="center" class="mt-5">
      <v-col cols="12" md="6">
        <v-card outlined>
          <v-card-subtitle>Search Component</v-card-subtitle>
          <v-col cols="12" md="8">
            <v-autocomplete
              label="Search"
              v-model="search"
              :items="dataList"
              outlined
              dense
              item-text="label"
              item-value="label"
            >
            </v-autocomplete>
          </v-col>
          <strong class="ml-5 mb-5">
            {{ this.search }}
          </strong>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>
<script>
import data from "@/mixins/data.json";

export default {
  data: () => ({
    search: "",
    dataList: [],
  }),
  mounted() {
    this.dataList = data.fields;
  },
  watch: {},
};
</script>