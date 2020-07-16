<template>
  <div class="dashboard">
    <aside class="sidebar">
      <div class="sidebar__content">
        <h6 class="sidebar__title-buyer">You are buying</h6>
        <p class="sidebar__text-buyer">
          Flight in space /Jupiter Area<br /><span
            >From IO to GANIMED, J29, 2048, G5/42</span
          ><br />
          Spaceship "Queen of the Sun"
        </p>
        <p class="sidebar__amount">42350.00 USD</p>
        <p class="sidebar__amount-hint">
          Amount to pay without the payment system commission
        </p>
        <h6 class="sidebar__title-seller">Seller</h6>
        <p class="sidebar__text-seller">
          National Aeronautics and Space<br />Administration (NASA)<br />
          Headquarters 300 E. Street SW, Suite 5R30
        </p>
        <p class="sidebar__meta"><span>Rating:</span> 5</p>
        <p class="sidebar__meta"><span>Reviews:</span> 308 042</p>
      </div>
      <div class="sidebar__copyright">
        <p>Provided by Onpay.ru</p>
      </div>
    </aside>
    <main class="form"></main>
  </div>
</template>

<script>
export default {
  name: "Dashboard"
};
</script>

<style lang="scss" scoped>
.dashboard {
  display: grid;
  grid-template-columns: 418px auto;
  min-height: 100vh;
}

.sidebar {
  padding: 36px 28px 42px 28px;
  background: $gradient-sidebar;
  color: #fff;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.sidebar__content {
  margin-bottom: 30px;
}

.sidebar__title-buyer {
  margin-bottom: 24px;
}

.sidebar__text-buyer {
  font-weight: 400;
  font-size: 18px;
  line-height: 27px;
  margin-bottom: 16px;

  span {
    font-weight: 600;
  }
}

.sidebar__amount {
  font-size: 34px;
  line-height: 44px;
}

.sidebar__amount-hint {
  font-size: 16px;
  line-height: 20px;
  color: $color-white-mutted;
  margin-bottom: 40px;
}

.sidebar__title-seller {
  margin-bottom: 10px;
}

.sidebar__text-seller {
  font-weight: 600;
  font-size: 17px;
  line-height: 26px;
  margin-bottom: 3px;
}

.sidebar__meta {
  font-size: 16px;
  line-height: 20px;

  span {
    color: $color-white-mutted;
  }
}

.sidebar__copyright {
  font-weight: 700;
  font-size: 18px;
  line-height: 27px;
}
</style>
