<template>
    <header class="header">
      
      <div class="header-wrapper">
        
        <nav class="nav-list-wrapper">
        <div class="logo">logo</div>
          <ul class="nav-list">
            <li class="nav-item">
              <a href="#">MENU</a>
            </li>
            <li class="nav-item">
              <a href="#">REWARDS</a>
            </li>
            <li class="nav-item">
              <a href="#">GIFT CARDS</a>
            </li>
          </ul>
        </nav>
        <div class="buttons-wrapper">
          <a href="#">
            <i class="fas fa-map-marker-alt"></i>
            Find a store
          </a>
          <div class="auth">
            <button type="button" class="signin">Sign In</button>
            <button type="button" class="register">Join now</button>
          </div>
        </div>
      </div>
    </header>
    <main>
      <div class="banner">COFFEE REWARDS</div>
      <section>
        <div class="container">
        <div class="content">
          <h1>FREE COFFEE <br/> IS A TAP AWAY</h1>
          <h2>Join now to start earning Rewards</h2>
          <button type="button" @click="yes">Join now</button>
          <h2>Or <a href="#1" class="underline">join in the app</a> for the best experience</h2>
        </div>
        </div>
      </section>
      <section>
        <div class="content-wrapper">
          <h2>Getting started is easy</h2>
          <p>Earn Starts and get rewarded in a few easy steps</p>
          
          <div class="cards-container">
            <div class="card">
              <div class="card-img">
                <img src="./assets/1.png" alt="number1">
              </div>
              <h3>Create an account</h3>
              <p>To get started, <a href="#">join now</a>. You can also <a href="#">join in the app</a> to get access to the full range of Coffee Rewards benefits.</p>
            </div>
            <div class="card">
              <div class="card-img">
                <img src="./assets/2.png" alt="number2">
              </div>
              <h3>Order and pay how you’d like</h3>
              <p>Use cash, credit/debit card or save some time and pay right through the app. You’ll collect Stars all ways. <a href="#">Learn how</a></p>
            </div>
            <div class="card">
              <div class="card-img">
                <img src="./assets/3.png" alt="number3">
              </div>
              <h3>Earn Stars, get Rewards</h3>
              <p>As you earn Stars, you can redeem them for Rewards—like free food, drinks, and more. Start redeeming with as little as 25 Stars!</p>
            </div>
          </div>
        </div>
      </section>
      <section>
        <div class="tabs-container">
          <h2>Get your favourite for free</h2>
          <div>
            <div class="tablist-bg">
              <div class="tablist-wrapper">
                
                <button @click="updateTab(25)" class="tab-btn">
                  <h2>25<span class="star">★</span></h2>
                  <div :class="{'selected-tab': tab === 25 }"></div>
                </button>
                <button @click="updateTab(50)" class="tab-btn">
                  <h2>50<span class="star">★</span></h2>
                  <div :class="{'selected-tab': tab === 50 }"></div>
                </button>
                <button @click="updateTab(150)" class="tab-btn">
                  <h2>150<span class="star">★</span></h2>
                  <div :class="{'selected-tab': tab === 150 }"></div>
                </button>
                <button @click="updateTab(200)" class="tab-btn">
                  <h2>200<span class="star">★</span></h2>
                  <div :class="{'selected-tab': tab === 200 }"></div>
                </button>
                <button @click="updateTab(400)" class="tab-btn">
                  <h2>400<span class="star">★</span></h2>
                  <div :class="{'selected-tab': tab === 400 }"></div>
                </button>
              </div>
            </div>
            
            <div class="selected-tabs">
              <transition name="fade" mode="out-in">
              <div v-if="tab === 25" :key="25" class="tab">
                <div class="tab-img">
                  <img src="./assets/025.png" alt="">
                </div>
                <div class="tab-content">
                  <h2>Customize your drink</h2>
                  <p>Make your drink just right with an extra espresso shot, dairy substitute or a dash of your favorite syrup.</p>
                </div>
              </div>
              <div v-else-if="tab === 50" :key="50" class="tab">
                <div class="tab-img">
                  <img src="./assets/050.png" alt="">
                </div>
                <div class="tab-content">
                  <h2>Brewed hot coffee, bakery item or hot tea</h2>
                  <p>Pair coffee cake or an almond croissant with your fresh cup of hot brew.</p>
                </div>
              </div>
              <div v-else-if="tab === 150" :key="150" class="tab">
                <div class="tab-img">
                  <img src="./assets/150.png" alt="">
                </div>
                <div class="tab-content">
                  <h2>Handcrafted drink, hot breakfast or parfait</h2>
                  <p>Have a really good morning with a breakfast sandwich, oatmeal or your favorite drink.</p>
                </div>
              </div>
              <div v-else-if="tab === 200" :key="200" class="tab">
                <div class="tab-img">
                  <img src="./assets/200.png" alt="">
                </div>
                <div class="tab-content">
                  <h2>Salad, sandwich or protein box</h2>
                  <p>Nourish your day with a hearty Chipotle Chicken Wrap or Eggs & Cheese Protein Box.</p>
                </div>
              </div>
              <div v-else-if="tab === 400" :key="400" class="tab">
                <div class="tab-img">
                  <img src="./assets/400.png" alt="">
                </div>
                <div class="tab-content">
                  <h2>Select merchandise or at-home coffee</h2>
                  <p>Take home a signature cup, a bag of coffee or your choice of select coffee accessories.</p>
                </div>
              </div>
              </transition>
            </div>
            
          </div>
        </div>
      </section>
      <section></section>
      <section></section>
    </main>
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      tab: 25,
    }
  },
  components: {
    
  },
  methods: {
    updateTab(value) {
      console.log(value, 'updated');
      this.tab = value;
    }
  }
}
</script>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
