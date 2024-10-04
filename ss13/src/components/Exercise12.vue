<template>
  <div>
    <h1>B12</h1>
    <div>
      <v-container>
        <v-card>
          <v-card-title>
            Product List
            <v-spacer></v-spacer>
            <v-btn color="primary" outlined> Add New Item </v-btn>
          </v-card-title>

          <!-- Search Bar -->
          <v-text-field
            class="mx-4"
            label="Search"
            prepend-inner-icon="mdi-magnify"
            outlined
          ></v-text-field>

          <!-- Product Table -->
          <v-data-table
            :items="products"
            class="mx-4"
            disable-sort
            hide-default-footer
          >
            <template v-slot:headers>
              <tr>
                <th>
                  <v-checkbox></v-checkbox>
                </th>
                <th>Product Image</th>
                <th>Product</th>
                <th>Date</th>
                <th>Status</th>
                <th>Price</th>
                <th>Actions</th>
              </tr>
            </template>

            <template v-slot:item="{ item }">
              <tr>
                <td>
                  <v-checkbox></v-checkbox>
                </td>
                <td>
                  <v-avatar>
                    <img :src="item.image" alt="Product Image" />
                  </v-avatar>
                </td>
                <td>
                  <div>{{ item.name }}</div>
                  <small>{{ item.category }}</small>
                </td>
                <td>{{ item.date }}</td>
                <td>
                  <v-chip
                    :color="item.status === 'Instock' ? 'green' : 'red'"
                    text-color="white"
                    small
                  >
                    {{ item.status }}
                  </v-chip>
                </td>
                <td>${{ item.price }}</td>
                <td>
                  <v-icon small class="mr-2" color="primary">mdi-pencil</v-icon>
                  <v-icon small color="red">mdi-delete</v-icon>
                </td>
              </tr>
            </template>
          </v-data-table>

          <!-- Pagination and Items Per Page -->
          <v-card-actions class="px-4">
            <v-select
              :items="itemsPerPageOptions"
              label="Items per page"
              outlined
            ></v-select>
            <v-spacer></v-spacer>
            <v-pagination :length="totalPages" v-model="page" />
          </v-card-actions>
        </v-card>
      </v-container>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      products: [
        {
          image:
            "https://th.bing.com/th/id/OIP.20aUpvI7tI6v_RRPgwBx0QHaE8?rs=1&pid=ImgDetMain",
          name: "Curology Face wash",
          category: "Beauty",
          date: "Thu, Jan 12 2023",
          status: "Instock",
          price: 275,
        },
        {
          image:
            "https://th.bing.com/th/id/OIP.20aUpvI7tI6v_RRPgwBx0QHaE8?rs=1&pid=ImgDetMain",
          name: "Body Lotion",
          category: "Beauty",
          date: "Thu, Jan 20 2023",
          status: "Out of Stock",
          price: 89,
        },
        {
          image:
            "https://th.bing.com/th/id/OIP.20aUpvI7tI6v_RRPgwBx0QHaE8?rs=1&pid=ImgDetMain",
          name: "Smart Watch",
          category: "Electronics",
          date: "Fri, Feb 15 2024",
          status: "Instock",
          price: 125,
        },
        {
          image:
            "https://th.bing.com/th/id/OIP.20aUpvI7tI6v_RRPgwBx0QHaE8?rs=1&pid=ImgDetMain",
          name: "Camera",
          category: "Electronics",
          date: "Fri, March 30 2024",
          status: "Instock",
          price: 200,
        },
        {
          image:
            "https://th.bing.com/th/id/OIP.20aUpvI7tI6v_RRPgwBx0QHaE8?rs=1&pid=ImgDetMain",
          name: "Games",
          category: "Electronics",
          date: "Sat, March 30 2024",
          status: "Out of Stock",
          price: 100,
        },
      ],
      itemsPerPageOptions: [5, 10, 15],
      page: 1,
      totalPages: 7,
    };
  },
};
</script>

<style scoped>
.v-avatar img {
  width: 50px;
  height: 50px;
}
</style>
