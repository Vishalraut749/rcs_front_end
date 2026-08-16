<script setup>
const summaryCards = [
  {
    title: 'Total Claims',
    value: 125,
    description: 'All submitted claims',
  },
  {
    title: 'Pending Claims',
    value: 32,
    description: 'Claims awaiting review',
  },
  {
    title: 'Approved Claims',
    value: 78,
    description: 'Successfully approved',
  },
  {
    title: 'Rejected Claims',
    value: 15,
    description: 'Claims rejected',
  },
]
</script>

<template>
  <div class="dashboard">
    <div class="dashboard-content">

      <!-- Header -->
      <div class="dashboard-header">
        <div>
          <h1 class="text-h4 font-weight-bold">Dashboard</h1>
          <p class="text-body-1 text-medium-emphasis">
            Welcome to Rapid Claim System
          </p>
        </div>

        <v-btn
          color="primary"
          prepend-icon="mdi-plus"
        >
          New Claim
        </v-btn>
      </div>

      <!-- Cards -->
      <v-row class="mt-6">
        <v-col cols="12" sm="6" md="3" v-for="card in summaryCards" :key="card.title">
          <v-card class="summary-card">
            <v-card-text>
              <div class="card-label">{{ card.title }}</div>
              <div class="card-value">{{ card.value }}</div>
              <div class="card-description">{{ card.description }}</div>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>

      <!-- Recent Claims -->
      <v-card class="claims-card mt-6">

        <v-card-title class="claims-header">
          <div>
            <div class="text-h6 font-weight-bold">
              Recent Claims
            </div>

            <div class="text-body-2 text-medium-emphasis">
              Latest claim activity
            </div>
          </div>

          <v-btn
            variant="text"
            color="primary"
          >
            View All
          </v-btn>
        </v-card-title>

        <v-divider />

        <v-table>
          <thead>
            <tr>
              <th>Claim ID</th>
              <th>Customer</th>
              <th>Amount</th>
              <th>Status</th>
            </tr>
          </thead>

          <tbody>
            <tr>
              <td>CLM-1001</td>
              <td>Rahul Patil</td>
              <td>₹25,000</td>
              <td>
                <v-chip color="warning" variant="tonal" size="small">
                  Pending
                </v-chip>
              </td>
            </tr>

            <tr>
              <td>CLM-1002</td>
              <td>Priya Sharma</td>
              <td>₹45,000</td>
              <td>
                <v-chip color="success" variant="tonal" size="small">
                  Approved
                </v-chip>
              </td>
            </tr>

            <tr>
              <td>CLM-1003</td>
              <td>Amit Kumar</td>
              <td>₹18,500</td>
              <td>
                <v-chip color="error" variant="tonal" size="small">
                  Rejected
                </v-chip>
              </td>
            </tr>
          </tbody>
        </v-table>

      </v-card>

    </div>
  </div>
</template>

<style scoped>

.dashboard {
  width: 100%;
  min-height: 100vh;
  padding: 40px;
  box-sizing: border-box;
}

.dashboard-content {
  width: 100%;
  max-width: none;
}

.dashboard-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.summary-card {
  width: 100%;
  min-height: 140px;
  border-radius: 12px;
}

.card-label {
  font-size: 14px;
  color: #6b7280;
}

.card-value {
  font-size: 30px;
  font-weight: 700;
  margin-top: 8px;
}

.card-description {
  font-size: 13px;
  color: #9ca3af;
  margin-top: 8px;
}

.claims-card {
  width: 100%;
  border-radius: 12px;
  overflow: hidden;
  margin-top: 24px;
}

.claims-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 24px;
}

</style>