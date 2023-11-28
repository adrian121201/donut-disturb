<template>
  <v-app dark style="background-color: #FAFAFA;" >
    <v-app-bar :clipped-left="clipped" fixed app style="background-color: #3E2723;" class="elevation-0">
      <v-toolbar-title>
        <v-row align="center">
          <v-col cols="auto">
            <v-btn text @click.prevent="handleNavigation('#home-section')">
             <span style="color: #f5b60a; font-family: 'Lilita One', sans-serif; font-size: 6vh; font-weight: bold;">DONUT DISTURB</span>
            </v-btn>
          </v-col>
          <v-col cols="auto">
            <v-img
              @click.prevent="handleNavigation('#home-section')"
              src="https://webstockreview.net/images/clipart-design-donut-15.png"
              alt="Donut Logo"
              width="46"
              height="46"
              style="margin-left: 5px; cursor: pointer;"
            ></v-img>
          </v-col>
        </v-row>
      </v-toolbar-title>
      <v-spacer />

     

      <v-btn text class="hidden-sm-and-down" style="color: white; font-family: 'Nunito'; font-weight: bold;" @click="scrollToSection('#about-us-section')">
        About Us
      </v-btn>

      <v-btn text class="hidden-sm-and-down" style="color: white; font-family: 'Nunito'; font-weight: bold;"  @click="scrollToSection('#menu-section')">
        Menu
      </v-btn>

      <v-btn text class="hidden-sm-and-down" style="color: white; font-family: 'Nunito'; font-weight: bold;" @click.prevent="handleNavigation('#opportunities-section')">
        Opportunities
      </v-btn>

      <v-btn text class="hidden-sm-and-down" style="color: white; font-family: 'Nunito'; font-weight: bold;" @click.prevent="handleNavigation('#reviews-section')">
        Reviews
      </v-btn>

      <v-btn text class="hidden-sm-and-down" style="color: white; font-family: 'Nunito'; font-weight: bold;" @click="scrollToSection('#contact-us-section')">
        Contact Us
      </v-btn>


      <v-btn icon class="hidden-sm-and-down">
        <v-icon color="white" size="24">mdi-facebook</v-icon>
      </v-btn>
      <v-btn icon class="hidden-sm-and-down">
        <v-icon color="white" size="24">mdi-twitter</v-icon>
      </v-btn>
      <v-btn icon class="hidden-sm-and-down">
        <v-icon color="white" size="24">mdi-instagram</v-icon>
      </v-btn>

      <v-btn icon class="hidden-md-and-up" @click.stop="drawer = !drawer">
        <v-icon color="white">mdi-menu</v-icon>
      </v-btn>
    </v-app-bar>
    
    <v-navigation-drawer v-model="drawer" app temporary class="elevation-0">
      <v-list-item-group>
        <v-list-item @click="scrollToSection('#about-us-section')">
          <v-list-item-title>About Us</v-list-item-title>
        </v-list-item>
        <v-list-item @click="scrollToSection('#menu-section')">
          <v-list-item-title>Menu</v-list-item-title>
        </v-list-item>
        <v-list-item @click.prevent="handleNavigation('#opportunities-section')">
          <v-list-item-title>Opportunities</v-list-item-title>
        </v-list-item>
        <v-list-item @click.prevent="handleNavigation('#reviews-section')">
          <v-list-item-title>Reviews</v-list-item-title>
        </v-list-item>
        <v-list-item @click="scrollToSection('#contact-us-section')">
          <v-list-item-title>Order</v-list-item-title>
        </v-list-item>
      </v-list-item-group>
    </v-navigation-drawer>

    
    <div style="width: 100%; margin-top: 50px;">
    <v-carousel cycle hide-delimiters height="300" :interval="5000">
      <v-carousel-item v-for="(item, index) in items" :key="index">
        <img :src="item.image" alt="Carousel Image" style="width: 100%; height: 100%;">
      </v-carousel-item>
    </v-carousel>
  </div>

    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>

     

    <v-footer
    color="#FF4081"
    height="auto"
  >
    <v-container>
      <v-row>
        <v-col cols="12" md="6">
      
          <v-img
            src="https://webstockreview.net/images/clipart-design-donut-15.png"
            alt="Donut Logo"
            width="120"
            height="120"
            color="white"
          ></v-img>
          <div class="white--text">
            <p style="color: white; font-family: 'Nunito'; font-size: 3vh;">Connect with us:</p>
            <v-btn icon color="white">
              <v-icon >mdi-facebook</v-icon>
            </v-btn>
            <v-btn icon color="white">
              <v-icon>mdi-twitter</v-icon>
            </v-btn>
            <v-btn icon color="white">
              <v-icon>mdi-instagram</v-icon>
            </v-btn>
          </div>
        </v-col>

        <v-col cols="12" md="6">
      
          <v-row>
          <v-col cols="12" md="6">
          <h3 style="color: white; font-family: 'Nunito'; font-size: 4vh;">Quick Links</h3>
          <v-list dense style="background-color: transparent;">
            <v-list-item v-for="link in footerLinks" :key="link.title" >
              <a @click.prevent="handleNavigation(link.link)" style="color: white; font-family: 'Nunito'; font-weight: bold; text-decoration: none; cursor: pointer;">
                {{ link.title }}
              </a>
            </v-list-item>
          </v-list>
        </v-col>
            <v-col cols="12" md="6">
              <h3 style="color: white; font-family: 'Nunito'; font-size: 4vh;">Contact Us</h3>
              <p class="white--text">Dolores, San Fernando Pampanga</p>
              <p class="white--text">donutdisturb21@gmail.com</p>
              <p class="white--text">+639534203251</p>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </v-footer>

   
  </v-app>



  
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      footerLinks: [
        { title: 'About', link: '#about-us-section' },
        { title: 'Menu', link: '#menu-section' },
        { title: 'Opportunities', link: '#opportunities-section' },
        { title: 'Reviews', link: '#reviews-section' },
        { title: 'Contact', link: '#contact-us-section' },
      ],
      items: [
        {
          image:'https://bearcreekdonuts.com/wp-content/uploads/2021/03/home4.jpg',
        },
        {
          image:'https://bearcreekdonuts.com/wp-content/uploads/2021/03/home2.jpg',
        },
       
      ],
    };
  },
  methods: {
    doSomething() {
    
    },
    handleNavigation(sectionId) {
      if (sectionId === '#home-section') {
        location.reload();
      } else {
        this.scrollToSection(sectionId);
      }
    },
    scrollToSection(sectionId) {
      const section = document.querySelector(sectionId);
      if (section) {
        window.scrollTo({
          top: section.offsetTop,
          behavior: 'smooth',
        });
      }
    },
  },
};
</script>










