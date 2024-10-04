<template>
  <div>
    <div>
      <!-- First Template -->
      <v-container>
        <v-row>
          <v-tabs v-model="activeTab" background-color="primary" dark>
            <v-tab>
              Item Cart <br />
              <small>Product Summary</small>
            </v-tab>
            <v-tab>
              Billing <br />
              <small>Billing Information</small>
            </v-tab>
            <v-tab>
              Payment <br />
              <small>Add & Update Card</small>
            </v-tab>
          </v-tabs>
        </v-row>

        <v-card class="mt-3">
          <v-card-title>
            <v-row>
              <v-col>Product</v-col>
              <v-col>Price</v-col>
              <v-col>Quantity</v-col>
              <v-col>Total</v-col>
            </v-row>
          </v-card-title>

          <v-divider></v-divider>

          <v-card-text>
            <v-row>
              <v-col>
                <v-img
                  src="https://th.bing.com/th/id/OIP.Ra3M-XJEDbBxJlSgKMNtSwHaHa?rs=1&pid=ImgDetMain"
                  height="80"
                  contain
                ></v-img>
                <div>Cute Soft Teddybear</div>
                <small>size: 8 | Color: Dark Red</small>
              </v-col>
              <v-col>
                <div>$200</div>
                <s>$175</s>
              </v-col>
              <v-col>
                <v-btn icon>
                  <v-icon>mdi-minus</v-icon>
                </v-btn>
                1
                <v-btn icon>
                  <v-icon>mdi-plus</v-icon>
                </v-btn>
              </v-col>
              <v-col>$200</v-col>
            </v-row>
          </v-card-text>

          <v-divider></v-divider>

          <v-card-text>
            <div class="text-h6">Order Summary</div>
            <v-row>
              <v-col>Sub Total</v-col>
              <v-col>$200</v-col>
            </v-row>
            <v-row>
              <v-col>Discount 5%</v-col>
              <v-col class="red--text">- $10</v-col>
            </v-row>
            <v-row>
              <v-col>Shipping Charges</v-col>
              <v-col>-</v-col>
            </v-row>
            <v-divider></v-divider>
            <v-row>
              <v-col>Total</v-col>
              <v-col>$190</v-col>
            </v-row>
          </v-card-text>

          <v-card-actions>
            <v-btn outlined color="red">Continue Shopping</v-btn>
            <v-spacer></v-spacer>
            <v-btn color="orange">CheckOut</v-btn>
          </v-card-actions>
        </v-card>
      </v-container>

      <!-- Second Template -->
    </div>
    <div>
      <div>
        <template>
          <v-container>
            <v-row>
              <v-col cols="12" md="6">
                <v-carousel hide-delimiters height="400">
                  <v-carousel-item v-for="(item, i) in images" :key="i">
                    <v-img :src="item" alt="Product Image"></v-img>
                  </v-carousel-item>
                </v-carousel>
              </v-col>

              <v-col cols="12" md="6">
                <v-card>
                  <v-card-title class="text-h5"
                    >Cute Soft Teddybear</v-card-title
                  >
                  <v-card-subtitle class="text-subtitle-1">
                    <span class="green--text">In Stock</span> | kids
                  </v-card-subtitle>
                  <v-card-text>
                    <div><s>$175</s> <span class="text-h5">$200</span></div>
                    <v-rating value="3" color="amber" dense readonly></v-rating>
                    <small>(236 reviews)</small>
                    <p>Description goes here...</p>
                    <div>Colors</div>
                    <v-btn
                      icon
                      v-for="color in colors"
                      :key="color"
                      :style="{ backgroundColor: color }"
                    >
                      <v-icon color="white">mdi-check</v-icon>
                    </v-btn>
                    <div>Quantity</div>
                    <v-btn icon>
                      <v-icon>mdi-minus</v-icon>
                    </v-btn>
                    1
                    <v-btn icon>
                      <v-icon>mdi-plus</v-icon>
                    </v-btn>
                  </v-card-text>
                  <v-card-actions>
                    <v-btn color="orange">Buy Now</v-btn>
                    <v-btn color="primary">Add To Cart</v-btn>
                  </v-card-actions>
                  <v-card-text>
                    <small>Dispatched in 2-3 weeks</small>
                    <v-btn text>Why the longer time for delivery?</v-btn>
                  </v-card-text>
                </v-card>
              </v-col>
            </v-row>
          </v-container>
        </template>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeTab: 0, // Tab state for switching between tabs
      images: [
        "https://via.placeholder.com/400x300.png?text=Product+Image+1",
        "https://via.placeholder.com/400x300.png?text=Product+Image+2",
        "https://via.placeholder.com/400x300.png?text=Product+Image+3",
      ],
      colors: ["#ffeb3b", "#ff5722", "#e91e63", "#03a9f4"],
    };
  },
};
</script>

<style scoped>
.v-card-text {
  padding-left: 0;
  padding-right: 0;
}
.v-carousel-item {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
