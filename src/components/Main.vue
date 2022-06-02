<template>
  <main>
    <section class="container section-working mt-4">
      <div class="row">
        <div
          class="
            col-md-6
            d-flex
            flex-column
            align-items-start
            justify-content-center
          "
        >
          <p class="section-working__title">
            Rachi, é tudo que você precisa em um só lugar.
          </p>
          <button class="mt-5 section-working__btn-cadastrar">
            Cadastrar-se
          </button>
        </div>

        <div class="col-md-6 d-flex justify-content-center">
          <img class="img-fluid" src="@/assets/images/working.svg" alt="" />
        </div>
      </div>
    </section>

    <section class="section-how-it-works">
      <div class="container">
        <p class="--title-default text-center mb-5">Como funciona</p>

        <div class="row justify-content-center">
          <div
            class="col-md-3"
            v-for="cardHowItWork in cardsHowItWorks"
            :key="'howItWorks' + cardHowItWork.title"
          >
            <HowWorkCard
              :image="cardHowItWork.image"
              :title="cardHowItWork.title"
              :description="cardHowItWork.description"
            />
          </div>
        </div>
      </div>
    </section>

    <section class="container section-download-app pt-2 pb-5">
      <div class="row">
        <div class="col-md-7 d-flex flex-column justify-content-center">
          <p class="section-download-app__title">
            Baixe nosso app para desfrutar mais!
          </p>
          <p class="--subtitle-default">
            Amet in elementum nulla scelerisque dui, egestas at. Elit
            consectetur turpis elementum amet vitae et etiam nec. Varius
            volutpat hac adipiscing tincidunt pretium.
          </p>
          <div
            class="
              section-download-app__container-buttons
              d-flex
              flex-wrap
              mt-2
            "
          >
            <button class="section-download-app__button me-2">
              <img src="@/assets/images/playstore.svg" alt="Botão Play Store" />
            </button>
            <button class="section-download-app__button">
              <img src="@/assets/images/appstore.svg" alt="Botão App Store" />
            </button>
          </div>
        </div>
        <div
          class="
            col-md-5
            mt-5 mt-xl-0
            d-flex
            align-items-center
            justify-content-center
          "
        >
          <img
            class="img-fluid"
            src="@/assets/images/notifications.svg"
            alt=""
          />
        </div>
      </div>
    </section>

    <section class="section-our-plans pt-4 pb-5">
      <p class="text-center --title-default">Nossos Planos</p>
      <p class="text-center --subtitle-default">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec lacinia
        mi quis euismod ultrices.
      </p>
      <div class="container mt-5">
        <div
          class="
            row
            flex-wrap
            justify-content-center
            align-center
            --gap-20
            pt-4
          "
        >
          <div
            v-for="cardPlan in cardPlans"
            class="
              col-12 col-xl-3
              d-flex
              align-items-center
              justify-content-center
              mb-5 mb-xl-0
            "
            :key="cardPlan.type"
          >
            <CardPlans
              :type="cardPlan.type"
              :price="cardPlan.price"
              :description="cardPlan.description"
              :preferred="cardPlan.preferred"
            />
          </div>
        </div>
      </div>
    </section>

    <section class="section-contact">
      <div
        class="
          section-contact__container
          d-flex
          flex-column
          justify-content-center
          align-items-center
        "
      >
        <p class="text-center --title-default">Contato</p>
        <p class="text-center section-contact__description">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec lacinia
          mi quis euismod ultrices.
        </p>

        <div
          class="
            mt-5
            d-flex
            flex-column flex-xl-row
            justify-content-center justify-content-lg-end
            align-items-xl-end
          "
        >
          <input
            class="section-contact__input-search me-xl-3"
            placeholder="Seu melhor e-mail"
          />
          <button class="mt-5 section-contact__button">Enviar</button>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import HowWorkCard from "./HowWorkCard.vue";
import CardPlans from "./CardPlans.vue";
export default {
  name: "Main",
  components: {
    HowWorkCard,
    CardPlans,
  },
  data() {
    return {
      cardsHowItWorks: [
        {
          image: "conections.svg",
          title: "Conexões",
          description: "Lorem ipsum dolor sit amet,consecteteu.",
        },
        {
          image: "security.svg",
          title: "100% gratuito",
          description: "Lorem ipsum dolor sit amet,consecteteu.",
        },
        {
          image: "smile.svg",
          title: "Compartilhamento",
          description: "Lorem ipsum dolor sit amet,consecteteu.",
        },
      ],
      cardPlans: [
        {
          type: "Bronze",
          price: 28,
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec lacinia mi quis euismod ultrices.",
          preferred: false,
        },
        {
          type: "Prata",
          price: 57,
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec lacinia mi quis euismod ultrices.",
          preferred: true,
        },
        {
          type: "Ouro",
          price: 94,
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec lacinia mi quis euismod ultrices.",
          preferredr: false,
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
%btn-blue {
  background-color: $blue-color;
  color: $white-color;
  box-shadow: 1px 3px 4px rgba(19, 125, 224, 0.5);
  border-radius: 50px;
}
.--gap-20 {
  gap: 20px;
}
.--white-color {
  color: $white-color;
}
.--title-default {
  font-family: "Sora", sans-serif;
  font-size: 2.5rem;
}
.--subtitle-default {
  color: $gray-color;
}

.section-working {
  min-height: 80vh;
  display: flex;
  align-items: center;
  &__title {
    font-size: 3rem;
    font-weight: 600;
    color: $gray-200-color;
  }
  &__btn-cadastrar {
    @extend %btn-blue;
    padding: 10px 30px;
    font-weight: 600;
  }
}
.section-how-it-works {
  background-color: $white-color;
  margin-top: 160px;
  padding: 100px 0px;

  @media (max-width: 800px) {
    & {
      margin-top: 20px;
      padding: 20px 0px;
    }
  }
}

.section-download-app {
  margin-top: 120px;

  &__title {
    font-size: 2.7rem;
    font-weight: 600;
    color: $gray-200-color;
    font-family: "Sora", sans-serif;
  }

  &__button {
    background-color: $gray-200-color;
    padding: 5px 25px;
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;

    img {
      max-height: 80%;
    }

    @media (max-width: 415px) {
      & {
        max-width: 48%;
        margin-top: 15px;
      }
    }
  }
  @media (max-width: 800px) {
    & {
      margin-top: 20px;
    }
  }
}

.section-our-plans {
  background-color: $white-color;
  margin-top: 100px;
}

.section-contact {
  margin-top: 200px;
  min-height: 380px;
  background: url("@/assets/images/contact.svg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  color: $white-color;
  padding-top: 40px;
  padding-bottom: 150px;
  position: relative;

  &::before {
    content: "";
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0px;
    background: rgba(41, 49, 69, 0.7);
    z-index: 1;
  }

  &__description {
    color: $gray-light-color;
    max-width: 600px;
  }

  &__container {
    z-index: 2;
    position: relative;
  }

  &__button {
    @extend %btn-blue;
    padding: 8px 50px;
  }
  &__input-search {
    background-color: transparent;
    width: 300px;
    position: relative;
    border-bottom: 2px solid $white-color;
    border-radius: 2px;
    height: 40px;

    font-size: 1.1rem;
    color: $white-color;
    &::placeholder {
      font-size: 1.1rem;
      color: $white-color;
    }
  }
  @media (max-width: 800px) {
    & {
      margin-top: 20px;
    }
  }
}
</style>
