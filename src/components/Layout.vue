<template>
  <div class="layout">
    <v-navigation-drawer
      v-model="drawer"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar fixed app>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-btn href="https://github.com/97cool-vikas" target="_blank">
      <v-icon>notranslate mdi mdi-github theme--light</v-icon>
      </v-btn>
      
      <v-btn href="https://wa.me/7697587695" target="_blank">
      <v-icon>notranslate mdi mdi-whatsapp theme--light</v-icon>
      </v-btn>
      <v-btn href="https://www.linkedin.com/in/vikas-nigam-886618188/" target="_blank">
      <v-icon>notranslate mdi mdi-linkedin theme--light</v-icon>
      </v-btn>
      <v-btn href="mailto:vikasnigam97@gmail.com">
      <v-icon>notranslate mdi mdi-gmail theme--light</v-icon>
      </v-btn>
    </v-app-bar>
    <v-footer app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      fixed: true,
      items: [
        {
          icon: "mdi-apps",
          title: "Home",
          to: "/",
        },
        {
          icon: "mdi-chart-bubble",
          title: "About",
          to: "/about",
        },
        {
          icon: "mdi-certificate",
          title: "Certification",
          to: "/certification",
        },
      ],
      title: "Hi, There! This is Vikas",
    };
  },
};
</script>