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
        <address class="sidebar__text-seller">
          National Aeronautics and Space<br />Administration (NASA)<img
            class="sidebar__text-seller-icon"
            src="@/assets/img/planet.svg"
            alt=""
          />
          <br />
          Headquarters 300 E. Street SW, Suite 5R30
        </address>
        <p class="sidebar__meta"><span>Rating:</span> 5</p>
        <p class="sidebar__meta"><span>Reviews:</span> 308 042</p>
      </div>
      <div class="sidebar__copyright">
        <a href="#">Provided by Onpay.ru</a>
      </div>
    </aside>
    <main class="form">
      <section class="method">
        <div class="method__header">
          <h6 class="method__title">Payment method</h6>
          <a href="#">Payment limits</a>
        </div>
        <div class="radio-buttons">
          <button class="radio-buttons__item radio-buttons__item--active">
            E-money
          </button>
          <button class="radio-buttons__item">Mobile Payments</button>
          <button class="radio-buttons__item">Bank Cards</button>
          <button class="radio-buttons__item">Bank Transfers</button>
          <button class="radio-buttons__item">Terminals</button>
        </div>
        <div class="payment-methods">
          <button class="payment-methods__item">
            <div class="payment-methods__item-logo-container">
              <img src="@/assets/img/logos/qiwi.png" alt="" />
            </div>
            <h6 class="payment-methods__item-title">Qiwi Wallet</h6>
            <p class="payment-methods__item-info">Payment Fees 1.5%</p>
          </button>
          <button class="payment-methods__item">
            <div class="payment-methods__item-logo-container">
              <img src="@/assets/img/logos/skrill.png" alt="" />
            </div>
            <h6 class="payment-methods__item-title">Skrill</h6>
            <p class="payment-methods__item-info">Payment Fees 2.5%</p>
          </button>
          <button class="payment-methods__item">
            <div class="payment-methods__item-logo-container">
              <img src="@/assets/img/logos/payoneer.png" alt="" />
            </div>
            <h6 class="payment-methods__item-title">Payoneer</h6>
            <p class="payment-methods__item-info">Payment Fees 5%</p>
          </button>
          <button class="payment-methods__item">
            <div class="payment-methods__item-logo-container">
              <img src="@/assets/img/logos/payza.png" alt="" />
            </div>
            <h6 class="payment-methods__item-title">Payza</h6>
            <p class="payment-methods__item-info">Payment Fees 2.5%</p>
          </button>
          <button class="payment-methods__item payment-methods__item--active">
            <div class="payment-methods__item-logo-container">
              <img src="@/assets/img/logos/yandex.png" alt="" />
            </div>
            <h6 class="payment-methods__item-title">Yandex.Money</h6>
            <p class="payment-methods__item-info">Payment Fees 2.5%</p>
          </button>
          <button class="payment-methods__item">
            <div class="payment-methods__item-logo-container">
              <img src="@/assets/img/logos/paypal.png" alt="" />
            </div>
            <h6 class="payment-methods__item-title">PayPal</h6>
            <p class="payment-methods__item-info">Payment Fees 0.5%</p>
          </button>
        </div>
      </section>
    </main>
  </div>
</template>

<script>
export default {
  name: "Dashboard"
};
</script>

<style lang="scss" scoped>
// * Global
.dashboard {
  display: grid;
  grid-template-columns: 418px auto;
  min-height: 100vh;
}

// * Sidebar
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

.sidebar__text-seller-icon {
  vertical-align: bottom;
  margin: 0 4px;
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

  a {
    color: #fff;
  }
}

// * Main content
.form {
  color: $color-black;
  padding: 36px;
  width: 100%;
  max-width: 782px;
}

.method__header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}

.radio-buttons {
  margin-bottom: 14px;
}
</style>
