<template>
  <div>
    <h1>B10</h1>
    <div>
      <v-container>
        <v-title> Item </v-title>
        <v-card>
          <v-table density="compact">
            <thead>
              <tr>
                <th class="text-left">Name</th>
                <th class="text-left">Project Name</th>
                <th class="text-left">Post</th>
                <th class="text-left">Status</th>
                <th class="text-left">Budget</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="item in desserts" :key="item.name">
                <td>{{ item.name }}</td>
                <td>{{ item.projectName }}</td>
                <td>{{ item.post }}</td>
                <td v-if="item.status == `Active`">
                  <v-btn color="secondary" variant="tonal">Active</v-btn>
                </td>
                <td v-if="item.status == `Pending`">
                  <v-btn color="warning" variant="tonal">Pending</v-btn>
                </td>
                <td v-if="item.status == `Complete`">
                  <v-btn color="primary" variant="tonal">Complete</v-btn>
                </td>
                <td v-if="item.status == `Cancel`">
                  <v-btn color="danger" variant="tonal">Cancel</v-btn>
                </td>
                <td>{{ item.budget }}</td>
              </tr>
            </tbody>
          </v-table>
        </v-card>
        <div class="menu">
          <v-menu>
            <template v-slot:activator="{ props }">
              <v-btn v-bind="props"> 5 ↑↑ </v-btn>
            </template>
            <v-list>
              <v-list-item
                v-for="(item, index) in items"
                :key="index"
                :value="index"
              >
                <v-list-item-title>{{ item.title }}</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-menu>
          <span>1-5 of 10</span>
        </div>
      </v-container>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      items: [
        { title: "Click Me" },
        { title: "Click Me" },
        { title: "Click Me" },
        { title: "Click Me 2" },
      ],
      desserts: [
        {
          name: "Sunil Joshi",
          projectName: "Elite Admin",
          post: "Web Designer",
          status: "Active",
          budget: "$3.9",
        },
        {
          name: "Sunil Joshi",
          projectName: "Elite Admin",
          post: "Web Designer",
          status: "Pending",
          budget: "$3.9",
        },
        {
          name: "Sunil Joshi",
          projectName: "Elite Admin",
          post: "Web Designer",
          status: "Complete",
          budget: "$3.9",
        },
        {
          name: "Sunil Joshi",
          projectName: "Elite Admin",
          post: "Web Designer",
          status: "Active",
          budget: "$3.9",
        },
        {
          name: "Sunil Joshi",
          projectName: "Elite Admin",
          post: "Web Designer",
          status: "Cancel",
          budget: "$3.9",
        },
      ],
    };
  },
};
</script>

<style>
.v-btn {
  border-radius: 999px;
  height: 60% !important;
}
.menu {
  text-align: end !important;
}
</style>
