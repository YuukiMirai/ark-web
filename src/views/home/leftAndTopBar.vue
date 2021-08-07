<template>
    <div>
        <v-navigation-drawer
                app
                v-model="isShowLeftBar"
                class="left-bar"
        >
            <!-- -->
            <v-card
                    elevation="2"
            >
                <v-btn
                        class="menu-left"
                        block
                        @click="turnToSearch"
                >
                    <v-icon
                            class="search-icon"
                    >
                        fas fa-search
                    </v-icon>
                    <span class="search-text">
                    {{searchTitle}}
                    </span>
                </v-btn>
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
        <!--        <v-footer app>-->
        <!--            &lt;!&ndash; &ndash;&gt;-->
        <!--        </v-footer>-->
    </div>

</template>

<script>
  export default {
    name: "leftBar",
    data() {
      return {
        isShowLeftBar: true, //是否显示左侧菜单
        overlayColor: "#949494", // 遮挡层颜色
        searchTitle: '全局搜索',
      }
    },
    methods: {
      turnToSearch() {

        console.log('111');
        //跳转
        this.$router.push({
          //跳转路由
          path: '/search'
        })
      }
    }
  }
</script>

<style scoped>
    .left-bar {
        padding: 8px;
    }


    .menu-left {
        background-color: #FFF;
    }

    .menu-left .search-text {
        font-size: 14px;
        color: rgba(0, 0, 0, .87);
        padding-left: 0px;
        padding-right: 100px;
    }

    .menu-left .search-icon {
        padding-right: 20px;
        padding-left: 0;
        font-size: 20px;
    }
</style>