<p align="center">
  <a href="https://ve-selectlist.lineitsolutions.com" target="_blank">
    <img src="https://raw.githubusercontent.com/logaretm/vee-validate/main/logo.png" width="200" title="Go to website">
  </a>
</p>

## Features

- **List Data:** List Array Of Data in Dropdown Wirt Filtering.
- **Flag API:** You Can Only Return Data With Countries & iso & ve-selectlist put all images with iso from flag api.
- **Value Tracking:** You Can return to users name and send any value to api like id easy...
- **With Image:** You Can return to users name and image easly...
- **Multiselect:** You Can multiselect Uploaded Soon...

## Getting Started

### Installation

```sh
# Install with yarn
yarn add ve-selectlist

# Install with npm
npm install ve-selectlist --save
```

### Usage

```sh
# in your file.vue add component & stylesheet
import VueSelectList from 've-selectlist';
import "ve-selectlist/dist/VueSelectList.css"
```

### Basic Select

```vue
<script setup>
import VueSelectList from 've-selectlist';
import 've-selectlist/dist/VueSelectList.css';
</script>

<template>
  <div class="ve_select">
    <VueSelectList
      :data="users"
      optionText="user_name"
      title="Select User"
      @update="onCategriesUpdate"
    />
  </div>
</template>

<script>
export default {
  components: {
    VueSelectList,
  },
  data() {
    return {
      users: [
        {
          id: 1,
          company_id: 1,
          user_name: 'Ahmed Waleed',
        },
        {
          id: 2,
          company_id: 1,
          user_name: 'Ahmed Lotfy',
        },
        {
          id: 3,
          company_id: 1,
          user_name: 'Ahmed Fakhry',
        },
      ],
      category_id: '',
    };
  },
  methods: {
    onCategriesUpdate(opject) {
      this.category_id = opject.id;
    },
  },
};
</script>
```
