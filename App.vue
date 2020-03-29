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


import HomeScreen from "./screens/Home.vue";
import DetailsScreen from "./screens/Details.vue";
import AboutScreen from "./screens/About.vue";




const IOSTabs = createBottomTabNavigator(
  {
    Home: HomeScreen,
    About: AboutScreen,
    Details: DetailsScreen,
    
  }
);
const AndroidTabs = createMaterialTopTabNavigator(
  {
    Home: HomeScreen,
    About: AboutScreen,
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