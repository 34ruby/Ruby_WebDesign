<template>
  <nav>
    <v-app-bar color="#23262C" dark app class="line" height="90px">
        <v-chip class="ma-2" color="grey darken-1" pill>DashBoard 
            <v-icon right small color="cyan">fas fa-chevron-circle-down</v-icon>
        </v-chip>
        <v-chip class="ma-2" color="grey darken-1" pill>Reports
            <v-icon right small color="cyan">fas fa-file-alt</v-icon>
        </v-chip>
        <v-chip class="ma-2" color="grey darken-1" pill>Stock Ageing
            <v-icon right small color="cyan">fas fa-chart-line</v-icon>
        </v-chip>
        <v-spacer></v-spacer>
        <v-text-field filled dense rounded label="Search" prepend-inner-icon="fas fa-search" class="mt-6 mr-2" sm="2"></v-text-field>
        <v-btn fab color="cyan" elevation="0" class="mr-2">
            <v-icon color="white">fas fa-user-check</v-icon>
        </v-btn>
        <v-btn fab color="orange" elevation="0">
            <v-icon color="white">fas fa-bars</v-icon>
        </v-btn>
    </v-app-bar>
    <v-navigation-drawer v-model="drawer" dark app mini-variant mini-variant-width="122" color="#23262d">
        <v-list>
            <v-list-item-group v-model="selectedItem" >
                <v-list-item class="mb-4">
                    <v-list-item-content align="center">
                        <v-icon align="center" x-large>fas fa-tv</v-icon>
                    </v-list-item-content>
                </v-list-item>
            </v-list-item-group>

            <v-list-item-group v-model="selectItem">
                <v-list-item v-for="(item, i) in items" :key="i">
                    <v-list-item-content align="center">
                        <v-icon v-text="item.icon" class="mb-3" align="center"></v-icon>
                        <v-list-item-subtitle v-text="item.text" align="center" class="caption"></v-list-item-subtitle>
                    </v-list-item-content>
                </v-list-item>
            </v-list-item-group>
        </v-list>
    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
    data: () => ({
        drawer: null,
        selectedItem: 0,
        items: [
            {text: 'DASHBOARD', icon: 'fas fa-tachometer-alt'},
            {text: 'REPORTS', icon: 'fas fa-file-alt'},
            {text: 'STOCK AGEING', icon: 'fas fa-chart-line'},
            {text: 'DEVICE SALES', icon: 'fas fa fa-tablet'},
            {text: 'USER REPORT', icon: 'fas fa-user-tag'},
            {text: 'SETTINGS', icon: 'fas fa-cogs'},
        ]
    })
}
</script>

<style>

</style>