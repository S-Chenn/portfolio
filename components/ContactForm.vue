<template lang="pug">
section.contact.section
  .container
    Heading.contact__heading(title="Contact" ruby="お問い合わせ")
    .wrap-form
      .form
        label.form__label Your Name
          span.required *
        input.form__input(type="text" name="name" id="name" autocomplete="name" required)
        label.form__label E-mail
          span.required *
        input.form__input(type="email" name="email" id="email" required)
        label.form__label Message
          span.required *
        textarea.form__input.form__input--textarea(name="body" id="body" required)
        .form__footer
          button.form__btn(type="submit") 送信
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
.required {
  color: #de3f3f;
  margin-left: 3px;
}
.wrap-form {
  max-width: 560px;
  width: 100%;
}
.form{
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr;
  gap: 16px;

  &__label {
    text-align: left;
    padding-top: 0;
  }
  &__input {
    font-size: 16px;
    border: 1px solid rgba(0, 0, 0, .12);
    border-radius: 3px;
    padding: 8px;
    width: 100%;
  }
  &__input--textarea {
    height: 160px;
  }
  &__footer {
    grid-column: 1/2;
  }
  &__btn {
    background-color: transparent;
    box-shadow: none;
    width: 120px;
    border: 2px solid #000;
    font-size: 14px;
    line-height: 46px;
    border-radius: 25px;
  }
}
@include pc(){
  .contact{
    padding-top: 120px;
  }
  .form {
  grid-template-columns: 160px 1fr;
  &__label {
    text-align: right;
    padding-top: 10px;
  }
  &__footer {
    grid-column: 2/3;
    margin-top: 16px;
  }
  }
}
</style>
