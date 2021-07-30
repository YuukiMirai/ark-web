<template>
    <v-app>
        <v-navigation-drawer
                app
                v-model="isShowLeftBar"
        >
            <!-- -->
            <v-card
                    elevation="2"
            >
                <v-btn>
                    <v-icon>
                        fas fa-search
                    </v-icon>
                </v-btn>
                {{searchTitle}}
            </v-card>
        </v-navigation-drawer>

        <v-app-bar app>
            <!-- -->
            <v-btn
                    class="mx-2"
                    fab
                    dark
                    color="teal"
                    @click.stop="isShowLeftBar = !isShowLeftBar"
            >
                <v-icon dark>
                    mdi-format-list-bulleted-square
                </v-icon>
            </v-btn>
        </v-app-bar>

        <!-- 根据应用组件来调整你的内容 -->
        <v-main>

            <!-- 给应用提供合适的间距 -->
            <v-container fluid>

                <!-- 如果使用 vue-router -->
                <router-view></router-view>
            </v-container>
        </v-main>

        <v-footer app>
            <!-- -->
        </v-footer>
    </v-app>
</template>

<!--<link href="https://cdn.jsdelivr.net/npm/@mdi/font@5.x/css/materialdesignicons.min.css" rel="stylesheet">-->
<script>
  export default {
    name: "index",
    data() {
      return {
        isShowLeftBar: false, //是否显示左侧菜单
        overlayColor: "#949494", // 遮挡层颜色
        searchTitle: '全局搜索',
      }
    },
    methods: {}
  }
</script>

<style scoped>

</style>