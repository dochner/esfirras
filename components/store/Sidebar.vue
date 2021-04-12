<template>
  <div>
    <v-sheet
      v-if="$vuetify.breakpoint.mdAndUp"
      height="300"
      :elevation="4"
      class="pa-8"
      tile
    >
      <h3>Filters</h3>
      <v-radio-group v-model="priceFilter" :mandatory="true">
        <v-radio
          v-for="(price, i) in prices"
          :key="i"
          :label="price"
          :value="i"
        />
      </v-radio-group>
    </v-sheet>
    <v-expansion-panels v-if="$vuetify.breakpoint.smAndDown">
      <v-expansion-panel>
        <v-expansion-panel-header expand-icon="fa-angle-down">
            Filters
        </v-expansion-panel-header>
        <v-expansion-panel-content>
            <v-radio-group v-model="priceFilter" :mandatory="true">
                <v-radio
                    v-for="(price, i) in prices"
                    :key="i"
                    :label="price"
                    :value="i"
                />
            </v-radio-group>
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>
  </div>
</template>

<script>
module.exports = {
  data() {
    return {
      prices: [
        'Any',
        'Under $25',
        '$25 to $100',
        '$100 to $500',
        'Over $500'
      ],
      priceFilter: 0,
      checkbox: true
    }
  }
}
</script>
