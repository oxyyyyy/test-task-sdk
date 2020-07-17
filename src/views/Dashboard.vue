<template>
  <div class="dashboard">
    <aside class="sidebar">
      <div class="sidebar__fixed-content">
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
          <router-link to="/onpay">Provided by Onpay.ru</router-link>
        </div>
      </div>
    </aside>
    <main class="form">
      <section class="method">
        <div class="method__header">
          <h6 class="method__title">Payment method</h6>
          <router-link to="/payment-limits" class="hide-to-collapse"
            >Payment limits</router-link
          >
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
              <img src="@/assets/img/logos/qiwi.svg" alt="" />
            </div>
            <h6 class="payment-methods__item-title">Qiwi Wallet</h6>
            <p class="payment-methods__item-info">Payment Fees 1.5%</p>
          </button>
          <button class="payment-methods__item">
            <div class="payment-methods__item-logo-container">
              <img src="@/assets/img/logos/skrill.svg" alt="" />
            </div>
            <h6 class="payment-methods__item-title">Skrill</h6>
            <p class="payment-methods__item-info">Payment Fees 2.5%</p>
          </button>
          <button class="payment-methods__item">
            <div class="payment-methods__item-logo-container">
              <img src="@/assets/img/logos/payoneer.svg" alt="" />
            </div>
            <h6 class="payment-methods__item-title">Payoneer</h6>
            <p class="payment-methods__item-info">Payment Fees 5%</p>
          </button>
          <button class="payment-methods__item">
            <div class="payment-methods__item-logo-container">
              <img src="@/assets/img/logos/payza.svg" alt="" />
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
              <img src="@/assets/img/logos/paypal.svg" alt="" />
            </div>
            <h6 class="payment-methods__item-title">PayPal</h6>
            <p class="payment-methods__item-info">Payment Fees 0.5%</p>
          </button>
        </div>
      </section>
      <section class="payment">
        <h6 class="payment__title">Payment</h6>
        <div
          class="input-group input-group--with-hint input-group--mobile-layout"
        >
          <label for="amount" class="label">Amount with commission</label>
          <div class="input-currency">
            <input
              id="amount"
              type="text"
              class="input"
              disabled
              value="43408.75"
            />
            <span class="input-currency__type">USD</span>
          </div>
          <p class="input-group__hint">
            <span class="input-group__hint-mobile-hide"
              >payment system fees</span
            >
            2.5% (+$1058.75)
          </p>
        </div>
        <div class="input-group input-group--with-hint">
          <label for="email" class="label">Yandex.Money account</label>
          <input id="email" type="email" class="input" />
        </div>
        <div class="input-group input-group--with-hint">
          <label for="phone" class="label">Phone</label>
          <input id="phone" type="tel" class="input" value="+380" />
        </div>
        <div class="input-group">
          <label for="message" class="label">Message for seller</label>
          <textarea
            id="message"
            class="input input--textarea"
            placeholder="If you need additional services, please inform the seller about this"
          ></textarea>
        </div>
        <div class="input-group input-group--with-hint">
          <label for="captcha" class="label">Enter captcha</label>
          <div class="input-captcha">
            <input id="captcha" type="text" class="input" />
            <div class="input-captcha__code">
              <img src="@/assets/img/captcha.svg" alt="" />
            </div>
          </div>
        </div>
        <div class="input-group">
          <div></div>
          <p class="form-agreement">
            By clicking "Confirm payment" I realize that the seller is
            responsible for the quality of the product/services and accept the
            <router-link to="/terms" class="accent-link"
              >terms of the agreement</router-link
            >
          </p>
        </div>
        <div class="input-group input-group--jc-fs">
          <div></div>
          <button type="button" class="button-accent form__submit-btn">
            Confirm payment
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

  @media screen and (max-width: $bp-collapse) {
    grid-template-columns: auto;
  }
}

// * Sidebar
.sidebar {
  background: $gradient-sidebar;
  color: #fff;
}

.sidebar__fixed-content {
  position: fixed;
  width: 418px;
  max-width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 36px 28px 42px 28px;

  @media screen and (max-width: $bp-collapse) {
    position: static;
    width: auto;
  }
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
  padding-bottom: 60px;
  width: 100%;
  max-width: 782px;

  @media screen and (max-width: $bp-collapse) {
    padding: 18px 16px;
    padding-bottom: 70px;
    max-width: 100%;
  }
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

.method {
  margin-bottom: 50px;
}

.payment__title {
  margin-bottom: 24px;

  @media screen and (max-width: $bp-collapse) {
    margin-bottom: 20px;
  }
}

.form__submit-btn {
  @media screen and (max-width: $bp-collapse) {
    position: fixed;
    bottom: 16px;
    width: calc(100% - 32px);
    box-shadow: 0px 4px 12px rgba(41, 49, 235, 0.4);
  }
}
</style>
