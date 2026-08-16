<script setup>
</script>

<template>
  <v-app>

    <v-app-bar elevation="4" color="primary" dark class="pa-0">
      <v-app-bar-title class="pa-4">Rapid Claim System</v-app-bar-title>
      <div class="flex-grow-1 top-menu-bar">
      <v-btn
        spaced="end"
        color="#FFFFFF"
        class="text-decoration-none"
        to="/"
        variant="text"
      >
        Dashboard
      </v-btn>

      <v-btn
      spaced="end"
        color="#FFFFFF"
        class="text-decoration-none"
        to="/claims"
        variant="text"
      >
        Claim Inbox
      </v-btn>

      <v-btn
      spaced="end"
        color="#FFFFFF"
        class="text-decoration-none"
        to="/payments"
        variant="text"
      >
        Payments
      </v-btn>

      <v-btn
      spaced="end"
        color="#FFFFFF"
        class="text-decoration-none"
        to="/customers"
        variant="text"
      >
        Customers
      </v-btn>

      <v-btn
        spaced="end"
        color="#FFFFFF"
        class="text-decoration-none"
        to="/reports"
        variant="text"
      >
        Reports
      </v-btn>
      <v-btn
        spaced="end"
        color="#FFFFFF"
        class="text-decoration-none"
        to="/reports"
        variant="text"
      >
        Allocate Claims
      </v-btn>
      <v-btn
        spaced="end"
        color="#FFFFFF"
        class="text-decoration-none"
        to="/reports"
        variant="text"
      >
        Reuest Hub
      </v-btn>
      </div>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>

  </v-app>
</template>

<style scoped>

.text-decoration-none{
  padding: 10px;
}
.top-menu-bar{
  display: flex;
    justify-content: center;
    align-items: center;
    padding-right: 10px;
    gap: 10px;
    color: white;
}
</style>
