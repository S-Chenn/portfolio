<template>
  <section class="meet section">
    <div class="container">
      <Heading title="Meet Elephants" ruby="ゾウと出会う" />
      <figure class="meet__image">
        <img src="@/assets/images/elephant.jpg" alt="elephant" class="meet__africa">
      </figure>
      <Heading title="Access" ruby="場所" />
      <div class="meet__map">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d241884.70545449102!2d24.397807837560173!3d-18.688727218963596!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1950e0a266fc1989%3A0xaadc0ae563ad43ce!2z44OB44On44OZ5Zu956uL5YWs5ZyS!5e0!3m2!1sja!2sjp!4v1562076016947!5m2!1sja!2sjp"
          frameborder="0"
          style="border:0"
          allowfullscreen
        />
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
.meet {
  padding: 80px 0;
  .container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  &__image {
    margin-bottom: 40px;
  }
  &__map {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    iframe {
      max-width: 1000px;
      width: 100%;
      height: 300px;
    }
  }
}
@include pc (){
  .meet {
    &__image {
      margin-bottom: 40px;
    }
    &__map {
      iframe {
        height: 450px;
      }
    }

  }
}
</style>
