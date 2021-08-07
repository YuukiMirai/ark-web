<template>
    <v-app>
        <left-bar></left-bar>
        <!-- 根据应用组件来调整你的内容 -->
        <v-main>
            <!-- 给应用提供合适的间距 -->
            <v-container fluid>
                <!-- 如果使用 vue-router -->
                <router-view></router-view>
            </v-container>
            <v-container>
                <v-card @click="clickCard1">
                    <v-card-text>123</v-card-text>
                </v-card>

            </v-container>
            <v-container>
                <v-card>
                    <v-card-text>456</v-card-text>
                </v-card>

            </v-container>
        </v-main>

        <v-footer app>
            <!-- -->
        </v-footer>
    </v-app>
</template>

<script>
  import '@fortawesome/fontawesome-free/css/all.css';
  import leftBar from './leftAndTopBar'

  export default {
    components: {
      leftBar,
    },
    name: "index",
    data() {
      return {}
    },
    methods: {
      clickCard1() {

      }
    }
  }
</script>

