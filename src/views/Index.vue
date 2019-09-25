<template>
  <div class="wrapper">
    <parallax class="page-header header-filter" :style="headerStyle">
      <div class="md-layout">
        <div class="md-layout-item">
          <div class="image-wrapper">
            <div class="brand">
              <h1>Aikikai - Singapore Chapter</h1>
              <h3>Aikido practitioners</h3>
            </div>
          </div>
        </div>
      </div>
    </parallax>

    <div class="main main-raised">
      <!-- Keep this raised panel -->

      <!-- <div class="section section-basic"> -->
      <div class="section section-intro">
        <div class="container">
          <div class="title">
            <h2>About us</h2>
          </div>

          <!-- <basic-elements></basic-elements> -->
          <!-- TODO: Replace with about elements -->
        </div>
      </div>

      <!-- <div class="section section-basic"> -->
      <div class="section section-aikido">
        <div class="container">
          <div class="title">
            <h2>Aikido</h2>
          </div>

          <!-- <basic-elements></basic-elements> -->
          <!-- TODO: Replace with Aikido information -->
        </div>
      </div>

      <!-- <div class="section section-basic"> -->
      <div class="section section-dojo">
        <div class="container">
          <div class="title">
            <h2>Dojo</h2>
          </div>

          <!-- <basic-elements></basic-elements> -->
          <!-- TODO: Replace with dojo elements -->
        </div>
      </div>

      <!-- <div class="section section-navbars">
        <div class="container">
          <small-navigation></small-navigation>
        </div>
        <navigation></navigation>
      </div> 
      <div class="section section-tabs">
        <div class="container">
          <tabs></tabs>
        </div>
      </div>
      <div class="section section-white">
        <div class="container">
          <nav-pills></nav-pills>
        </div>
      </div>
      <div class="section section-notifications">
        <div class="container">
          <div class="title">
            <h3>Notifications</h3>
          </div>
        </div>
        <notifications></notifications>
      </div>
      <div class="section">
        <div class="container">
          <typography-images></typography-images>
        </div>
      </div>
      <div class="section section-javascript">
        <div class="container">
          <javascript-components></javascript-components>
        </div>
      </div>-->
    </div>
  </div>
</template>




<script>
import BasicElements from "./components/BasicElementsSection";
import Navigation from "./components/NavigationSection";
import SmallNavigation from "./components/SmallNavigationSection";
import Tabs from "./components/TabsSection";
import NavPills from "./components/NavPillsSection";
import Notifications from "./components/NotificationsSection";
import TypographyImages from "./components/TypographyImagesSection";
import JavascriptComponents from "./components/JavascriptComponentsSection";
import { LoginCard } from "@/components";

export default {
  components: {
    BasicElements,
    Navigation,
    SmallNavigation,
    Tabs,
    NavPills,
    Notifications,
    TypographyImages,
    JavascriptComponents,
    LoginCard
  },
  name: "index",
  bodyClass: "index-page",
  props: {
    image: {
      type: String,
      default: require("@/assets/img/aikido-bg-distort.png")
    }
  },
  data() {
    return {
      firstname: null,
      email: null,
      password: null,
      leafShow: false
    };
  },
  methods: {
    leafActive() {
      if (window.innerWidth < 768) {
        this.leafShow = false;
      } else {
        this.leafShow = true;
      }
    }
  },
  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.image})`
      };
    },
    signupImage() {
      return {
        backgroundImage: `url(${this.signup})`
      };
    }
  },
  mounted() {
    this.leafActive();
    window.addEventListener("resize", this.leafActive);
  },
  beforeDestroy() {
    window.removeEventListener("resize", this.leafActive);
  }
};
</script>
<style lang="scss">
.section-download {
  .md-button + .md-button {
    margin-left: 5px;
  }
}

@media all and (min-width: 991px) {
  .btn-container {
    display: flex;
  }
}
</style>

