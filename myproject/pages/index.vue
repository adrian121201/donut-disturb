<template>
  <div>
 
    <div id="about-us-section" style="margin-bottom: 100px;">
  <v-container>
    <v-card class="mt-5 text-center elevation-0" color="transparent">
      <v-row align="center" class="mx-auto" style="max-width: 1000px;">
        <v-col cols="12" md="4">
          <v-img
            src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/3c097e07-ab69-4781-adcd-22c2d9af8902/dg0fjwu-83472f7f-265c-45a9-92b2-ad2bd97cc49a.png/v1/fit/w_828,h_828,q_70,strp/donut_girl_by_wabisabiwonders_dg0fjwu-414w-2x.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzNjMDk3ZTA3LWFiNjktNDc4MS1hZGNkLTIyYzJkOWFmODkwMlwvZGcwZmp3dS04MzQ3MmY3Zi0yNjVjLTQ1YTktOTJiMi1hZDJiZDk3Y2M0OWEucG5nIiwiaGVpZ2h0IjoiPD0xMjgwIiwid2lkdGgiOiI8PTEyODAifV1dLCJhdWQiOlsidXJuOnNlcnZpY2U6aW1hZ2Uud2F0ZXJtYXJrIl0sIndtayI6eyJwYXRoIjoiXC93bVwvM2MwOTdlMDctYWI2OS00NzgxLWFkY2QtMjJjMmQ5YWY4OTAyXC93YWJpc2FiaXdvbmRlcnMtNC5wbmciLCJvcGFjaXR5Ijo5NSwicHJvcG9ydGlvbnMiOjAuNDUsImdyYXZpdHkiOiJjZW50ZXIifX0._ay8vVZ7JQ3IX1YgHd1nGSNGRgxZnheJ1Y-KO2uFJyc"
            alt="About Us Image"
            height="300px"
            width="300px"
            style="border-radius: 50%;"
          ></v-img>
        </v-col>
        <v-col cols="12" md="8">
          <v-card-title style="font-family: 'Nunito'; font-weight: bold; color: #f5b60a; font-size: 40px;">About Us</v-card-title>
          <v-card-text style="color: black; max-width: 700px; text-align: justify; line-height: 28px; display: flex; flex-direction: column;">
            Savor the joy of delightful donuts at Donut Delight - your go-to destination for indulgent, mouth-watering treats. Our commitment to sweetness and unwavering dedication to quality have made us the top choice for discerning individuals who crave the perfect blend of flavor, texture, and satisfaction.
            With a heritage deeply rooted in baking excellence, our donuts are meticulously crafted to offer the ideal combination of taste and pleasure. Whether you're in pursuit of a classic glazed donut to satisfy your sweet tooth or exploring adventurous flavors to elevate your donut experience, our extensive collection has something to match your unique cravings.
            We firmly believe that the right donut can significantly elevate your mood and bring a touch of sweetness to your day. Our team of pastry experts is wholeheartedly committed to helping you discover that perfect donut that complements your taste buds and brings a smile to your face. At Donut Delight, we're not just a bakery - we're your trusted source for irresistible, delectable treats.
            Dive into our diverse range of donut offerings and treat yourself to a world of flavors like never before.
            <v-row>
              <v-btn text color="white" style="background-color: #3E2723; margin-top: 30px;  margin-left: 12px; border-radius: 20px;">See more</v-btn>
              <v-btn text color="white" style="background-color: #FF4081; margin-top: 30px; margin-left: 12px; border-radius: 20px;">Explore Menu</v-btn>
            </v-row>
          </v-card-text>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</div>





<div id="menu-section">
  <v-container>
    <v-row>
      <v-col v-for="(donut, index) in donuts" :key="index" cols="12" sm="6" md="4" lg="3">
        <v-card class="d-flex flex-column align-center">
          <v-card-title class="text-center" style="font-family: 'Nunito'; font-weight: bold; color: black;">
            {{ donut.title }}
          </v-card-title>
          <v-card-text>
            <p>{{ donut.description }}</p>
          </v-card-text>
          <v-img :src="donut.image"></v-img>
          <v-card-actions class="d-flex justify-center align-center">
            <v-btn color="white" text style="background-color: #f5b60a; border-radius: 20px; font-size: 12px;">Order Now</v-btn>
            <v-btn icon color="#3E2723">
              <v-icon>mdi-cart</v-icon>
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</div>




<div id="opportunities-section" style="margin-top: 40px; margin-bottom: 40px;">
  <v-container fluid>
    <v-row>
      <v-col cols="12" class="p-0">
  
        <div style="position: relative;">
   
          <v-img
            src="https://img.freepik.com/free-photo/delicious-glazed-doughnuts-arrangement_23-2150674104.jpg?t=st=1701151874~exp=1701155474~hmac=bd37eecad4f4a4306cd85213857f46beb9ee38e352908691a6a641d934888fa6&w=2000"
            alt="Long Picture"
            class="d-flex align-center"
            style="height: 250px; position: relative;"
          >
      
            <div style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; background-color: rgba(0, 0, 0, 0.4);"></div>

            <v-row class="fill-height ma-0" align="center" justify="center">
              <v-col cols="12" class="text-center">
                <v-card color="transparent" class="white--text elevation-0">
                  <v-card-text style="color: white; font-family: 'Nunito'; font-size: 30px; font-weight: bold;">
                    We don't just sell donuts
                  </v-card-text>
                  <v-card-subtitle style="color: white; font-family: 'Nunito'; font-size: 17px;">
                    We offer business opportunities too!
                  </v-card-subtitle>
                </v-card>
              </v-col>
            </v-row>

            <v-row class="fill-height ma-0" align="center" justify="center">
              <v-col cols="12" class="text-center">
                <v-btn
                  outlined
                  text
                  style="border-color: white; 
                  border-width: 2px;
                  color: white; 
                  background-color: rgba(0, 0, 0, 0.1);"
                >
                  Check Opportunities
                </v-btn>
              </v-col>
            </v-row>
          </v-img>
        </div>
      </v-col>
    </v-row>
  </v-container>
</div>



<div id="reviews-section">
  <v-container>
    <v-row>
      <v-col
        v-for="(item, index) in twitterItems"
        :key="index"
        cols="12"
        sm="4"
      >
        <v-card
          class="mx-auto"
          color="white" 
          dark
          max-width="400"
        >
          <v-card-title style="color: black;">
            <span style="font-family: 'Nunito'; font-weight: bold; color: #f5b60a;">Reviews</span>
          </v-card-title>

     
          <v-list-item>
            <v-list-item-avatar color="grey darken-3">
              <v-img
                class="elevation-6"
                alt=""
                :src="item.picture"
              ></v-img>
            </v-list-item-avatar>

            <v-list-item-content>
              <v-list-item-title style="color: black;">{{ item.name }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>

          <v-card-text class="text-h7 font-weight-bold" style="color: #616161;"> 
            "{{ item.text }}"
          </v-card-text>

    
          <v-rating
            v-model="item.rating"
            background-color="transparent"
            color="yellow"
            dense
            half-increments
            readonly
            style="margin-left: 10px;"
          ></v-rating>

          <v-card-actions>
            <v-row
              align="center"
              justify="space-between"
              class="w-100"
            >
              <v-col>
                <v-icon class="mr-1" style="color: black;">mdi-Like</v-icon>
                <span class="subheading" style="color: black;">{{ item.shares }}</span>
              </v-col>
              <!-- You can add more actions here if needed -->
            </v-row>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</div>


<div id="contact-us-section" style="margin-top: 50px; margin-bottom: 50px;">
  <v-container>
 
    <v-row>
      <v-col cols="12" md="6">
        <v-img
          src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/3c097e07-ab69-4781-adcd-22c2d9af8902/dg9an4m-8ac3b048-491e-4580-8e6c-99e08b748532.png/v1/fit/w_828,h_828,q_70,strp/cute_waitress_by_wabisabiwonders_dg9an4m-414w-2x.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzNjMDk3ZTA3LWFiNjktNDc4MS1hZGNkLTIyYzJkOWFmODkwMlwvZGc5YW40bS04YWMzYjA0OC00OTFlLTQ1ODAtOGU2Yy05OWUwOGI3NDg1MzIucG5nIiwiaGVpZ2h0IjoiPD0xMjgwIiwid2lkdGgiOiI8PTEyODAifV1dLCJhdWQiOlsidXJuOnNlcnZpY2U6aW1hZ2Uud2F0ZXJtYXJrIl0sIndtayI6eyJwYXRoIjoiXC93bVwvM2MwOTdlMDctYWI2OS00NzgxLWFkY2QtMjJjMmQ5YWY4OTAyXC93YWJpc2FiaXdvbmRlcnMtNC5wbmciLCJvcGFjaXR5Ijo5NSwicHJvcG9ydGlvbnMiOjAuNDUsImdyYXZpdHkiOiJjZW50ZXIifX0.QA4-2JMFg5CuFXnBCwQppPAolojJBR-hJMlWFsNdUYU"
          alt="Contact Image"
          height="450px"
          width="450px"
          style="border-radius: 50%;"
        ></v-img>
      </v-col>

      <v-col cols="12" md="6">
        <v-card class="elevation-3 pa-6">
          <h1 style="font-family: 'Nunito'; color: #f5b60a;">Contact Us</h1>
          <v-form>
       
            <v-row>
              <v-col cols="12" md="6">
                <v-text-field  label="First Name" ></v-text-field>
              </v-col>
              <v-col cols="12" md="6">
                <v-text-field  label="Last Name" ></v-text-field>
              </v-col>
            </v-row>
            
       
            <v-row>
              <v-col cols="12" md="6">
                <v-text-field  label="Email"></v-text-field>
              </v-col>
              <v-col cols="12" md="6">
                <v-text-field  label="Phone Number"></v-text-field>
              </v-col>
            </v-row>

         
            <v-row>
              <v-col cols="12">
                <v-textarea label="Message"></v-textarea>
              </v-col>
            </v-row>
            
            <v-btn class="elevation-0" color="#f5b60a" style="color: white; border-radius: 20px;">Submit</v-btn>
            <v-btn class="elevation-0" color="#f5b60a" style="color: white; border-radius: 20px;">Clear</v-btn>
          </v-form>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</div>




  </div>
</template>



<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      donuts: [
        {
          title: "Classic Glazed",
          description: "Experience the classic glazed donut with a perfect blend of sweetness.",
          image: 'https://img.freepik.com/premium-photo/balushahi-sweet-food-served-white-golden-plate-moody-background_466689-25281.jpg?w=826',
        },
        {
          title: "Star Fluffy",
          description: "Experience the classic glazed donut with a perfect blend of sweetness.",
          image: 'https://d2rdhxfof4qmbb.cloudfront.net/wp-content/uploads/20180905143956/Faschingskrapfen.jpg',
        },
        {
          title: "Rose Filling",
          description: "Experience the classic glazed donut with a perfect blend of sweetness.",
          image: 'https://d2rdhxfof4qmbb.cloudfront.net/wp-content/uploads/20180903195350/Berliners.jpg',
        },
        {
          title: "Moon",
          description: "Experience the classic glazed donut with a perfect blend of sweetness.",
          image: 'https://d2rdhxfof4qmbb.cloudfront.net/wp-content/uploads/20180905144005/Fritule.jpg',
        },
        {
          title: "Crown Feeling",
          description: "Experience the classic glazed donut with a perfect blend of sweetness.",
          image: 'https://d2rdhxfof4qmbb.cloudfront.net/wp-content/uploads/20180905144036/Zeppole.jpg',
        },
        {
          title: "Dark Glaze",
          description: "Experience the classic glazed donut with a perfect blend of sweetness.",
          image: 'https://d2rdhxfof4qmbb.cloudfront.net/wp-content/uploads/20180717130400/Loukoumades-1024x684.jpg',
        },
        {
          title: "Classic Noble",
          description: "Experience the classic glazed donut with a perfect blend of sweetness.",
          image: 'https://images6.alphacoders.com/799/799212.jpg',
        },
        {
          title: "Classic",
          description: "Experience the classic glazed donut with a perfect blend of sweetness.",
          image: 'https://www.wallpaperflare.com/static/833/738/401/donuts-chocolate-glaze-photo-wallpaper-preview.jpg',
        },
      ],
      twitterItems: [

        { 
        text: "Absolutely loved the donuts! They were incredibly fresh and flavorful. I can't get enough of them! Highly recommend trying them out!",
        picture: 'https://www.billboard.com/wp-content/uploads/2022/05/nayeon-twice-2022-press-billboard-1548.png',
        name: 'Nayeon', 
        rating: 5,
        
        },
        { 
        text: "These donuts are divine! The variety of flavors is impressive, and they simply melt in your mouth. You won't be disappointed!",
        picture: 'https://6.soompi.io/wp-content/uploads/image/20230728152120_Jihyo-2.jpg?s=900x600&e=t',
        name: 'Jihyo', 
        rating: 5,
    
        },
        { 
        text: "Amazing donuts! The texture and taste are outstanding. Each bite feels like a little piece of heaven. Can't wait to visit again!", 
        picture: 'https://qph.cf2.quoracdn.net/main-qimg-a6b8a6bf79bc0780cf1cc7f4ca5c0e77-lq', 
        name: 'Momo', 
        rating: 5,
       
        },
        { 
        text: "I'm in love with these donuts! The flavors are simply amazing, and they're always so fresh and scrumptious!",
        picture: 'https://image-cdn.hypb.st/https%3A%2F%2Fhypebeast.com%2Fwp-content%2Fblogs.dir%2F6%2Ffiles%2F2022%2F10%2Fgucci-newjeans-hanni-brand-ambassdaor-announcement-tw.jpg?w=960&cbr=1&q=90&fit=max',
        name: 'Hanni', 
        rating: 5,
       
        },
        { 
        text: "I'm obsessed with these donuts! The freshness and flavors are top-notch. A must-try for any donut enthusiast!",
        picture: 'https://image.kpopmap.com/2023/06/NewJeans-MinJi-W-Korea.jpg',
        name: 'Minji', 
        rating: 5,
     
        },
        { 
        text: "These donuts are pure bliss! The flavors are so rich and delightful. You won't regret indulging in these heavenly treats!",
        picture: 'https://assets.puzzlefactory.com/puzzle/520/361/original.jpg', 
        name: 'Haerin', 
        rating: 5,
      
        },
        
      ],
    };
  },
};
</script>


