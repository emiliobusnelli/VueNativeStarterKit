<template>
  <nb-container>
    <nb-header>
      <text>Title<text>
    </nb-header>
    <nb-content>
      <nb-form>
        <nb-picker
          mode="dropdown"
          :iosIcon="getIosIcon()"
          placeholder="Select your SIM"
          placeholderStyle="{ color: '#bfc6ea' }"
          placeholderIconColor="#007aff"
          :selectedValue="selected"
          :onValueChange="onValueChange"
        >
          <item label="$6" value="key0" />
          <item label="$7" value="key1" />
          <item label="$8" value="key2" />
          <item label="$9" value="key3" />
          <item label="$10" value="key4" />
        </nb-picker>
      </nb-form>
    </nb-content>
  </nb-container>
</template>

<script>
import React from "react";
import { Picker, Icon } from "native-base";
export default {
  components: { Item: Picker.Item },
  data: function() {
    return {
      selected: ""
    };
  },
  methods: {
    onValueChange: function(value) {
      this.selected = value;
    },
    getIosIcon: function() {
      return <Icon name="ios-arrow-down-outline" />;
    }
  }
};
</script>