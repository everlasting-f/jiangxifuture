<template>
  <v-container fluid>
    <v-card>
      <v-responsive width="100%" aspect-ratio="3" >
        <v-img
          :src="require('@/assets/home/news/5.jpg')"
          class="grey lighten-2 d-flex align-center"
          height="100%"
          aspect-ratio="3"
        >
          <v-row>
            <v-col cols="12" sm="6" offset-sm="3">
              <!-- <v-responsive aspect-ratio="16"> -->
              <v-text-field
                class="white"
                flat
                dense
                hide-details="auto"
                label="Search"
                prepend-inner-icon="mdi-magnify"
                solo-inverted
              ></v-text-field>
              <!-- </v-responsive> -->
            </v-col>
          </v-row>
        </v-img>
      </v-responsive>
    </v-card>
    <v-container>
      <v-row>
        <v-col cols="12" md="6">
          <v-breadcrumbs :items="items" light>
            <template v-slot:divider>
              <v-icon>mdi-chevron-right</v-icon>
            </template>
          </v-breadcrumbs>
        </v-col>
        <v-col cols="12" md="6">
          <v-toolbar dense flat class="d-flex justify-sm-space-between justify-md-end">
            <v-toolbar-title class="mr-md-5">
              <v-btn>
                <v-icon>mdi-email-newsletter</v-icon>集团新闻
              </v-btn>
            </v-toolbar-title>
            <v-toolbar-title>
              <v-btn>
                <v-icon>mdi-microphone-variant</v-icon>媒体报道
              </v-btn>
            </v-toolbar-title>
          </v-toolbar>
        </v-col>
      </v-row>
    </v-container>

    <v-divider></v-divider>

    <!-- 新闻列表组件 -->
    <newlist></newlist>

    <div class="d-flex justify-center align-center">
      <v-btn text>&lt; 上一页</v-btn>
      <v-responsive max-width="50" class="mx-5">
        <v-text-field outlined dense hide-details="auto"></v-text-field>
      </v-responsive>
      <span class="mr-5">/{{ 18 }}</span>
      <v-btn text>下一页 &gt;</v-btn>
    </div>
  </v-container>
</template>

<script>
import newlist from "./neslist-com";
export default {
  components: { newlist },
  data: () => ({
    items: [
      {
        text: "Dashboard",
        disabled: false,
        href: "news"
      },
      {
        text: "Link 1",
        disabled: false,
        href: "breadcrumbs_link_1"
      },
      {
        text: "Link 2",
        disabled: true,
        href: "breadcrumbs_link_2"
      }
    ]
    // toggleExclusive: undefined,
  })
};
</script>