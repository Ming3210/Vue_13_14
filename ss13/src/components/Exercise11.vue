<template>
  <div>
    <h1>B11</h1>
    <div>
      <v-container>
        <v-row>
          <!-- Filters Sidebar -->
          <v-col cols="3">
            <v-card class="pa-4">
              <!-- Gender Filter -->
              <v-expansion-panels>
                <v-expansion-panel>
                  <v-expansion-panel-header>Gender</v-expansion-panel-header>
                  <v-expansion-panel-content>
                    <v-checkbox label="All"></v-checkbox>
                  </v-expansion-panel-content>
                </v-expansion-panel>

                <!-- Categories Filter -->
                <v-expansion-panel>
                  <v-expansion-panel-header
                    >Categories</v-expansion-panel-header
                  >
                  <v-expansion-panel-content>
                    <v-checkbox label="Kitchen"></v-checkbox>
                    <v-checkbox label="Electronics"></v-checkbox>
                  </v-expansion-panel-content>
                </v-expansion-panel>

                <!-- Price Filter -->
                <v-expansion-panel>
                  <v-expansion-panel-header>Price</v-expansion-panel-header>
                  <v-expansion-panel-content>
                    <v-radio-group>
                      <v-radio label="$10 - $50"></v-radio>
                      <v-radio label="$50 - $100"></v-radio>
                      <v-radio label="$100 - $150"></v-radio>
                      <v-radio label="$150 - $200"></v-radio>
                      <v-radio label="Over $200"></v-radio>
                    </v-radio-group>
                  </v-expansion-panel-content>
                </v-expansion-panel>

                <!-- Rating Filter -->
                <v-expansion-panel>
                  <v-expansion-panel-header>Rating</v-expansion-panel-header>
                  <v-expansion-panel-content>
                    <v-rating length="5"></v-rating>
                  </v-expansion-panel-content>
                </v-expansion-panel>
              </v-expansion-panels>

              <!-- Reset Button -->
              <v-btn block color="primary" class="mt-4">Reset Filters</v-btn>
            </v-card>
          </v-col>

          <!-- Product Grid -->
          <v-col cols="9">
            <v-row>
              <!-- Product Card 1 -->
              <v-col cols="12" md="4">
                <v-card>
                  <v-img
                    src="https://th.bing.com/th/id/OIP.3Df1JLR5k7iNChSTuqy7RQHaE9?rs=1&pid=ImgDetMain"
                    height="200px"
                  ></v-img>
                  <v-card-title>MacBook Air Pro</v-card-title>
                  <v-card-subtitle>
                    <span class="line-through">$12</span>
                    <span class="ml-2">$15</span>
                  </v-card-subtitle>
                  <v-card-actions>
                    <v-rating value="4" readonly dense></v-rating>
                    <v-spacer></v-spacer>
                    <v-btn icon>
                      <v-icon>mdi-cart</v-icon>
                    </v-btn>
                  </v-card-actions>
                </v-card>
              </v-col>

              <!-- Product Card 2 -->
              <v-col cols="12" md="4">
                <v-card>
                  <v-img
                    src="https://th.bing.com/th/id/OIP.3Df1JLR5k7iNChSTuqy7RQHaE9?rs=1&pid=ImgDetMain"
                    height="200px"
                  ></v-img>
                  <v-card-title>Red Velvet Dress</v-card-title>
                  <v-card-subtitle>
                    <span class="line-through">$14.59</span>
                    <span class="ml-2">$16</span>
                  </v-card-subtitle>
                  <v-card-actions>
                    <v-rating value="4" readonly dense></v-rating>
                    <v-spacer></v-spacer>
                    <v-btn icon>
                      <v-icon>mdi-cart</v-icon>
                    </v-btn>
                  </v-card-actions>
                </v-card>
              </v-col>

              <!-- Product Card 3 -->
              <v-col cols="12" md="4">
                <v-card>
                  <v-img
                    src="https://th.bing.com/th/id/OIP.3Df1JLR5k7iNChSTuqy7RQHaE9?rs=1&pid=ImgDetMain"
                    height="200px"
                  ></v-img>
                  <v-card-title>Boat Headphone</v-card-title>
                  <v-card-subtitle>
                    <span class="line-through">$29</span>
                    <span class="ml-2">$36</span>
                  </v-card-subtitle>
                  <v-card-actions>
                    <v-rating value="4.5" readonly dense></v-rating>
                    <v-spacer></v-spacer>
                    <v-btn icon>
                      <v-icon>mdi-cart</v-icon>
                    </v-btn>
                  </v-card-actions>
                </v-card>
              </v-col>

              <!-- Product Card 4 -->
              <v-col cols="12" md="4">
                <v-card>
                  <v-img
                    src="https://th.bing.com/th/id/OIP.3Df1JLR5k7iNChSTuqy7RQHaE9?rs=1&pid=ImgDetMain"
                    height="200px"
                  ></v-img>
                  <v-card-title>The Psychology of Money</v-card-title>
                  <v-card-subtitle>
                    <span class="line-through">$49</span>
                    <span class="ml-2">$85</span>
                  </v-card-subtitle>
                  <v-card-actions>
                    <v-rating value="5" readonly dense></v-rating>
                    <v-spacer></v-spacer>
                    <v-btn icon>
                      <v-icon>mdi-cart</v-icon>
                    </v-btn>
                  </v-card-actions>
                </v-card>
              </v-col>

              <!-- Product Card 5 -->
              <v-col cols="12" md="4">
                <v-card>
                  <v-img
                    src="https://th.bing.com/th/id/OIP.3Df1JLR5k7iNChSTuqy7RQHaE9?rs=1&pid=ImgDetMain"
                    height="200px"
                  ></v-img>
                  <v-card-title>Psalms Book for Growth</v-card-title>
                  <v-card-subtitle>
                    <span class="line-through">$81</span>
                    <span class="ml-2">$89</span>
                  </v-card-subtitle>
                  <v-card-actions>
                    <v-rating value="3" readonly dense></v-rating>
                    <v-spacer></v-spacer>
                    <v-btn icon>
                      <v-icon>mdi-cart</v-icon>
                    </v-btn>
                  </v-card-actions>
                </v-card>
              </v-col>

              <!-- Product Card 6 -->
              <v-col cols="12" md="4">
                <v-card>
                  <v-img
                    src="https://th.bing.com/th/id/OIP.3Df1JLR5k7iNChSTuqy7RQHaE9?rs=1&pid=ImgDetMain"
                    height="200px"
                  ></v-img>
                  <v-card-title>Gaming Console</v-card-title>
                  <v-card-subtitle>
                    <span class="line-through">$86</span>
                    <span class="ml-2">$99</span>
                  </v-card-subtitle>
                  <v-card-actions>
                    <v-rating value="2" readonly dense></v-rating>
                    <v-spacer></v-spacer>
                    <v-btn icon>
                      <v-icon>mdi-cart</v-icon>
                    </v-btn>
                  </v-card-actions>
                </v-card>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style scoped>
.line-through {
  text-decoration: line-through;
}
</style>
