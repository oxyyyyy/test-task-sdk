<template>
  <div class="dashboard">
    <div
      class="amount-to-pay-preview"
      :class="{ 'amount-to-pay-preview--hide': isActiveAmountToPay }"
      @click="isActiveAmountToPay = !isActiveAmountToPay"
    >
      <span class="amount-to-pay-preview__label">Amount to pay</span>
      <span class="amount-to-pay-preview__value">42350.00 USD</span>
      <div class="sidebar__mobile-icon show-to-collapse"></div>
    </div>
    <aside class="sidebar">
      <div
        class="sidebar__fixed-content"
        @click="isActiveAmountToPay = !isActiveAmountToPay"
        :class="{
          'sidebar__fixed-content--show': isActiveAmountToPay,
          alwaysShow: windowWidth >= 836,
          'alwaysShow--flex': windowWidth >= 836
        }"
      >
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
          <h6 class="sidebar__title-seller hide-to-collapse">Seller</h6>
          <address class="sidebar__text-seller hide-to-collapse">
            National Aeronautics and Space<br />Administration (NASA)<img
              class="sidebar__text-seller-icon"
              src="@/assets/img/planet.svg"
              alt=""
            />
            <br />
            Headquarters 300 E. Street SW, Suite 5R30
          </address>
          <p class="sidebar__meta hide-to-collapse"><span>Rating:</span> 5</p>
          <p class="sidebar__meta hide-to-collapse">
            <span>Reviews:</span> 308 042
          </p>
        </div>
        <div class="sidebar__copyright hide-to-collapse">
          <router-link to="/onpay">Provided by Onpay.ru</router-link>
        </div>
        <div class="sidebar__mobile-icon show-to-collapse"></div>
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
        <div class="radio-buttons hide-to-collapse">
          <button class="radio-buttons__item radio-buttons__item--active">
            E-money
          </button>
          <button class="radio-buttons__item">Mobile Payments</button>
          <button class="radio-buttons__item">Bank Cards</button>
          <button class="radio-buttons__item">Bank Transfers</button>
          <button class="radio-buttons__item">Terminals</button>
        </div>
        <div
          class="payment-methods"
          :class="{ 'payment-methods--active': isActiveSelect }"
        >
          <button
            class="payment-methods__mobile-select show-to-collapse show-to-collapse--flex"
            @click="isActiveSelect = !isActiveSelect"
            role="button"
            aria-labelledby="dropdown-label"
            tabindex="0"
          >
            <span>Yandex.Money</span>
            <svg
              class="payment-methods__mobile-select-icon"
              width="10"
              height="8"
              viewBox="0 0 10 8"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M8.49779 0.879578L10 2.34941L5 7.24162L0 2.34941L1.50221 0.879578L5 4.30197L8.49779 0.879578Z"
                fill="#B3B3B3"
              />
            </svg>
          </button>
          <div
            class="payment-methods__mobile-select-list"
            :class="{
              alwaysShow: windowWidth >= 836,
              'alwaysShow--grid': windowWidth >= 836
            }"
            v-show="isActiveSelect"
            :aria-expanded="isActiveSelect"
            role="list"
          >
            <button class="payment-methods__item">
              <div
                class="payment-methods__item-logo-container hide-to-collapse"
              >
                <img src="@/assets/img/logos/qiwi.svg" alt="" />
              </div>
              <h6 class="payment-methods__item-title">Qiwi Wallet</h6>
              <p class="payment-methods__item-info hide-to-collapse">
                Payment Fees 1.5%
              </p>
            </button>
            <button class="payment-methods__item">
              <div
                class="payment-methods__item-logo-container hide-to-collapse"
              >
                <img src="@/assets/img/logos/skrill.svg" alt="" />
              </div>
              <h6 class="payment-methods__item-title">Skrill</h6>
              <p class="payment-methods__item-info hide-to-collapse">
                Payment Fees 2.5%
              </p>
            </button>
            <button class="payment-methods__item">
              <div
                class="payment-methods__item-logo-container hide-to-collapse"
              >
                <img src="@/assets/img/logos/payoneer.svg" alt="" />
              </div>
              <h6 class="payment-methods__item-title">Payoneer</h6>
              <p class="payment-methods__item-info hide-to-collapse">
                Payment Fees 5%
              </p>
            </button>
            <button class="payment-methods__item">
              <div
                class="payment-methods__item-logo-container hide-to-collapse"
              >
                <img src="@/assets/img/logos/payza.svg" alt="" />
              </div>
              <h6 class="payment-methods__item-title">Payza</h6>
              <p class="payment-methods__item-info hide-to-collapse">
                Payment Fees 2.5%
              </p>
            </button>
            <button class="payment-methods__item payment-methods__item--active">
              <div
                class="payment-methods__item-logo-container hide-to-collapse"
              >
                <img src="@/assets/img/logos/yandex.png" alt="" />
              </div>
              <h6 class="payment-methods__item-title">Yandex.Money</h6>
              <p class="payment-methods__item-info hide-to-collapse">
                Payment Fees 2.5%
              </p>
            </button>
            <button class="payment-methods__item">
              <div
                class="payment-methods__item-logo-container hide-to-collapse"
              >
                <img src="@/assets/img/logos/paypal.svg" alt="" />
              </div>
              <h6 class="payment-methods__item-title">PayPal</h6>
              <p class="payment-methods__item-info hide-to-collapse">
                Payment Fees 0.5%
              </p>
            </button>
          </div>
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
  name: "Dashboard",
  data() {
    return {
      isActiveSelect: false,
      windowWidth: window.innerWidth,
      isActiveAmountToPay: false
    };
  },
  created() {
    window.addEventListener("resize", this.handleResize);
    this.handleResize();
  },
  destroyed() {
    window.removeEventListener("resize", this.handleResize);
  },
  methods: {
    handleResize() {
      this.windowWidth = window.innerWidth;
    }
  }
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
.amount-to-pay-preview {
  background: linear-gradient(0deg, #2f37f4, #2f37f4);
  padding: 16px;
  color: #fff;
  display: none;
  justify-content: space-between;
  align-items: center;
  position: relative;
  cursor: pointer;
  margin-bottom: 2px;
  visibility: visible;
  transition: opacity 0.3s ease, transform 0.3s ease;

  @media screen and (max-width: $bp-collapse) {
    display: flex;
  }
}

.amount-to-pay-preview--hide {
  transform: translateY(-5%);
  opacity: 0;
  visibility: hidden;
}

.amount-to-pay-preview__label {
  font-size: 18px;
  line-height: 27px;
}

.amount-to-pay-preview__value {
  font-size: 16px;
  line-height: 24px;
}

.sidebar {
  color: #fff;

  @media screen and (max-width: $bp-collapse) {
    padding: 10px;
    position: fixed;
    z-index: 50;
    visibility: hidden;
    width: 100%;
  }
}

.sidebar__fixed-content {
  background: $gradient-sidebar;
  position: fixed;
  width: 418px;
  max-width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 36px 28px 42px 28px;

  @media screen and (max-width: $bp-collapse) {
    position: relative;
    width: auto;
    padding: 20px;
    border-radius: $border-radius;
    background: linear-gradient(180deg, #2f37f4 0%, #1820de 100%);
    box-shadow: 0px 4px 12px rgba(23, 30, 198, 0.35);
    transition: opacity 0.3s ease, transform 0.3s ease;
    opacity: 0;
    visibility: hidden;
    transform: translateY(5%);
    cursor: pointer;
  }
}

.sidebar__fixed-content--show {
  opacity: 1;
  transform: translateY(0);
  visibility: visible;
}

.sidebar__content {
  margin-bottom: 30px;

  @media screen and (max-width: $bp-collapse) {
    margin-bottom: 0;
  }
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

  @media screen and (max-width: $bp-collapse) {
    font-size: 20px;
  }
}

.sidebar__amount {
  font-size: 34px;
  line-height: 44px;

  @media screen and (max-width: $bp-collapse) {
    font-size: 28px;
  }
}

.sidebar__amount-hint {
  font-size: 16px;
  line-height: 20px;
  color: $color-white-mutted;
  margin-bottom: 40px;

  @media screen and (max-width: $bp-collapse) {
    margin-bottom: 0;
    font-size: 15px;
  }
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

.sidebar__mobile-icon {
  width: 28px;
  height: 2px;
  background: #6066f3;
  border-radius: 5px;
  position: absolute;
  bottom: 8px;
  right: calc(50% - 20px);
  transform: translateX(-50%);
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

  @media screen and (max-width: $bp-collapse) {
    margin-bottom: 40px;
  }
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
    box-shadow: $box-shadow;
  }
}
</style>
