<template>
  <div
    v-if="$q.screen.width >= 600"
    style="background-color: #8a8383; color: white; text-align: center"
  >
    Use Mobile Phone for better experience
  </div>
  <div class="settings-container">
    <p class="settings-title">Settings</p>
    <div class="card">
      <div class="circle col-1">AS</div>
      <div class="content col">
        <div class="content--title">Achmad Syarif</div>
        <div class="content--desc">Apple ID, ICloud+, Media & Purchases</div>
      </div>
      <div class="col-1">
        <q-icon name="arrow_forward_ios" flat color="blue-grey-13" />
      </div>
    </div>
    <div class="q-mt-md">
      <div class="card2">
        <div class="icon" style="background-color: orange">
          <q-icon name="flight" flat color="white" />
        </div>
        <div class="content">
          <div>Airplane Mode</div>
          <q-space />
          <q-toggle size="sm" v-model="value" color="green" />
        </div>
      </div>
      <div class="card2">
        <div class="icon" style="background-color: #035efc">
          <q-icon name="wifi" flat color="white" />
        </div>
        <div class="content">
          <div>Wi-Fi</div>
          <q-space />
          <q-icon name="arrow_forward_ios" flat color="blue-grey-13" />
        </div>
      </div>
      <div class="card2">
        <div class="icon" style="background-color: #035efc">
          <q-icon name="bluetooth" flat color="white" />
        </div>
        <div class="content">
          <div>Bluetooth</div>
          <q-space />
          <q-icon name="arrow_forward_ios" flat color="blue-grey-13" />
        </div>
      </div>
      <div class="card2">
        <div class="icon" style="background-color: #03fc7b">
          <q-icon name="signal_cellular_alt" flat color="white" />
        </div>
        <div class="content">
          <div>Cellular</div>
          <q-space />
          <q-icon name="arrow_forward_ios" flat color="blue-grey-13" />
        </div>
      </div>
      <div class="card2">
        <div class="icon" style="background-color: #03fc7b">
          <q-icon name="wifi_tethering" flat color="white" />
        </div>
        <div class="content">
          <div>Cellular</div>
          <q-space />
          <q-icon name="arrow_forward_ios" flat color="blue-grey-13" />
        </div>
      </div>
    </div>
    <div class="q-mt-md">
      <div class="card2">
        <div class="icon" style="background-color: #8a8383">
          <q-icon name="settings" flat color="white" />
        </div>
        <div class="content">
          <div>General</div>
          <q-space />
          <q-icon name="arrow_forward_ios" flat color="blue-grey-13" />
        </div>
      </div>
      <div class="card2">
        <div class="icon" style="background-color: #8a8383">
          <q-icon name="tune" flat color="white" />
        </div>
        <div class="content">
          <div>Control Center</div>
          <q-space />
          <q-icon name="arrow_forward_ios" flat color="blue-grey-13" />
        </div>
      </div>
      <div class="card2">
        <div class="icon" style="background-color: #ff0000">
          <q-icon name="fingerprint" flat color="white" />
        </div>
        <div class="content">
          <div>Touch ID & Passcode</div>
          <q-space />
          <q-icon name="arrow_forward_ios" flat color="blue-grey-13" />
        </div>
      </div>
      <div class="card2">
        <div class="icon" style="background-color: #03fc7b">
          <q-icon name="battery_low" flat color="white" />
        </div>
        <div class="content">
          <div>Battery</div>
          <q-space />
          <q-icon name="arrow_forward_ios" flat color="blue-grey-13" />
        </div>
      </div>
      <div class="card2">
        <div class="icon" style="background-color: #03fc7b">
          <q-icon name="wifi_tethering" flat color="white" />
        </div>
        <div class="content">
          <div>Cellular</div>
          <q-space />
          <q-icon name="arrow_forward_ios" flat color="blue-grey-13" />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const value = ref(true);

defineOptions({
  name: "IndexPage",
});
</script>
<style lang="scss">
.settings-container {
  background-color: black;
  height: 100vh;
  padding: 16px;
}

.settings-title {
  color: white;
  font-weight: 700;
  font-size: 30px;
}

.card {
  display: flex;
  align-items: center;
  gap: 10px;
  background-color: rgb(49, 49, 49);
  border-radius: 5px;
  padding: 5px 10px;
  .circle {
    width: 60px;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 60px;
    background-color: white;
    border-radius: 50%;
    font-size: 24px;
  }
  .content {
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: center;

    &--title {
      font-weight: 600;
      font-size: 16px;
    }
    &--desc {
      font-size: 10px;
    }
  }
}
.card2 {
  color: white;
  display: flex;
  align-items: center;
  gap: 10px;
  background-color: rgb(49, 49, 49);
  padding: 3px 10px;

  &:first-child {
    border-radius: 5px 5px 0 0;
  }
  &:last-child {
    border-radius: 0 0 5px 5px;
    padding-bottom: 4px;
  }
  &:not(:last-child) {
    .content {
      border-bottom: 1px solid rgb(83, 83, 83);
    }
  }

  .icon {
    padding: 2px 5px;
    border-radius: 5px;
  }
  .content {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 100%;
  }
}
</style>
