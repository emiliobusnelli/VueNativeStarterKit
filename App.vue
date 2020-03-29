<template>
  <app-navigator>
  </app-navigator>
</template>

<script>
import {
  createAppContainer,
  createBottomTabNavigator,
  createMaterialTopTabNavigator,
  createStackNavigator,
} from "vue-native-router";


import Vue from "vue-native-core";
import { VueNativeBase } from "native-base";

// registering all native-base components to the global scope of the Vue
Vue.use(VueNativeBase);


import DeckScreen from "./screens/Deck.vue";
import DetailsScreen from "./screens/Details.vue";
import PriceScreen from "./screens/Price.vue";




const IOSTabs = createBottomTabNavigator(
  {
    Home: DeckScreen,
    Price: PriceScreen,
    Details: DetailsScreen,
    
  }
);
const AndroidTabs = createMaterialTopTabNavigator(
  {
    Home: DeckScreen,
    Price: PriceScreen,
    Details: DetailsScreen,
    
  }
);
const StackNavigator = createStackNavigator(
  {
    IOSTabs,
    AndroidTabs
  }
);
const AppNavigator = createAppContainer(StackNavigator);
export default {
  components: { AppNavigator },
}
</script>