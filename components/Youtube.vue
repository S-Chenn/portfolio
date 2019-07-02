<template>
  <section class="youtube section--dark">
    <div class="container">
      <Heading class="heading" title="Elegant Elephants" ruby="優雅なゾウさん" />
      <div class="card">
        <div class="movie">
          <div>
            <iframe
              src="https://www.youtube.com/embed/mlOiXMvMaZo"
              frameborder="0"
              allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
            />
          </div>
        </div>
        <div class="card__text">
          <h4 class="card__heading">
            Description
          </h4>
          <p class="card__description">
            Come face to face with the largest land animal on the planet, the African elephant. This herd of giants take a detour to investigate a stranger in their midst.
          </p>
          <p class="card__description">
            Elegant Elephant Baking Co. is a gluten-free bakery in Eugene, OR, specializing in all kinds of baked goods, except without the wheat.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import Heading from '@/components/Heading.vue'
export default {
  components: {
    Heading
  }
}
</script>
<style lang="scss" scoped>
.section--dark {
  background-image: linear-gradient(to top right, #000, #2d033a);
}
/deep/ .heading__ruby::after {
      border-bottom: 4px solid #fff;
}
.youtube {
  padding: 80px 0;
  .heading {
    color: #fff;
    margin: 0 auto;
  }
  .card {
    background: #FAFFFF;
    display: grid;
    &__text {
      max-width: 560px;
      padding: 32px;
      width: 100%;
      height: 100%;
    }
    &__heading {
      font-size: 24px;
      font-weight: 600;
      margin-bottom: 16px;
    }
    &__description {
      text-align: left;
      margin-bottom: 16px;
    }
  }
}

iframe {
  display: block;
  width: 100%;
}
@include pc(){
  .youtube {
    .card {
    grid-template-columns: repeat(2, 1fr);
    grid-auto-flow: row;
    height: 315px;
    }
  }
  iframe {
  display: block;
  height: 315px;
  vertical-align: bottom;
}
}
</style>
