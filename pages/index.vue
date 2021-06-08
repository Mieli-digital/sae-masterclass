<template>
  <div>
    <div class="hero">
      <BaseLayout columns="two">
        <div class=""></div>
        <div class="">
          <div class="hero__list">
            <Nuxt-link to="/">About us</Nuxt-link>
            <Nuxt-link to="/">Reviews</Nuxt-link>
            <Nuxt-link to="/">Services</Nuxt-link>
            <Nuxt-link to="/">Sign up</Nuxt-link>
          </div>
          <h1>We care for your furry little loved ones while you’re away</h1>
          <BaseButton class="hero__button" />
        </div>
      </BaseLayout>
    </div>
    <section>
      <BaseLayout columns="two">
        <div class="">
          <BaseHeadlineWithText
            title="Expert care for your furry, feathery, or scaley friend"
            text="We know how stressful it is to leave your pets at home alone. We’re
            a team of experienced animal caregivers, well connected to local
            veterinarians. Trust to us to love them like our own, and to keep
            them safe and happy till you’re home."
          />
          <BaseButton dark class="hero__button" />
        </div>
        <div class="">
          <FourByFourGrid>
            <img src="@/assets/images/cat.jpg" alt="" />
            <img src="@/assets/images/bird.jpg" alt="" />
            <img src="@/assets/images/dog.jpg" alt="" />
            <img src="@/assets/images/hamster.jpg" alt="" />
          </FourByFourGrid>
        </div>
      </BaseLayout>
    </section>
    <section class="noMarginBottom">
      <div class="backgroundSection">
        <div class="backgroundSection__card"></div>
        <BaseLayout columns="one" padding="4rem">
          <div>
            <BaseHeadlineWithText
              title="Expert care for your furry, feathery, or scaley friend"
              text="We know how stressful it is to leave your pets at home alone. We’re
            a team of experienced animal caregivers, well connected to local
            veterinarians. Trust to us to love them like our own, and to keep
            them safe and happy till you’re home."
            />
            <BaseButton dark class="hero__button" />
          </div>
        </BaseLayout>
      </div>
    </section>
    <section class="dark noMarginTop">
      <BaseLayout center columns="one" padding="4rem">
        <div>
          <BaseHeadlineWithText
            marginBottom="4rem"
            title="Pets  (and their humans) love us"
          />
          <div class="reviewCards">
            <div class="reviewCards__card" v-for="i in 4" :key="i">
              <img src="@/assets/images/review_1.jpg" alt="" />
              <div>
                <b>Lindsay M.</b>
                <p>
                  Pawtastic is awesome! They are passionate about pets and
                  employ trustworthy, dependable staff. We love them!”
                </p>
              </div>
            </div>
          </div>
          <BaseButton class="hero__button" />
        </div>
      </BaseLayout>
    </section>
  </div>
</template>

<script>
import FourByFourGrid from '@/components/FourbyFourGrid.vue'
export default {
  middleware: 'mymiddleware',
  components: {
    FourByFourGrid,
  },
}
</script>

<style lang="scss" scoped>
.hero {
  height: 100vh;
  width: 100vw;
  background: url('@/assets/images/hero.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: none;
  padding: 2rem;
  color: white;

  h1 {
    font-size: 4.5rem;
  }
  &__list {
    display: flex;
    justify-content: space-between;
    margin-bottom: 4rem;
    a {
      &:hover {
        border-bottom: 1px solid white;
      }
      font-size: 1rem;
      border-bottom: 1px solid transparent;
      color: white;
      text-decoration: none;
    }
  }

  &__button {
    margin-top: 4rem;
  }
}

.backgroundSection {
  display: grid;
  grid-template-columns: 48vw 48vw;
  align-content: center;
  gap: 2vw;
  background: #f7eceb;

  &__card {
    width: 100%;
    background: url('@/assets/images/service.jpg');
    background-size: cover;
    background-position: center;
    background-repeat: none;
    img {
      max-width: 100%;
    }
  }
}

.dark {
  background: #545871;
  color: white;
}

.reviewCards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(450px, 1fr));
  gap: 3rem;
  &__card {
    background: white;
    color: #545871;
    padding: 32px;
    border-radius: 5px;
    display: grid;
    align-items: center;
    text-align: left;
    width: 100%;
    gap: 40px;
    grid-template-columns: 1fr 2fr;
    p {
      font-size: 1rem;
      line-height: 1.3rem;
    }
  }
}
.noMarginBottom {
  margin-bottom: 0;
}
.noMarginTop {
  margin-top: 0;
}
</style>
