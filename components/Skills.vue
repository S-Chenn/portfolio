<template>
  <section id="skills" class="skills section">
    <div class="container">
      <Heading class="skills__heading" title="My Skills" ruby="スキル" />
      <div class="grid">
        <skill-card class="card" title="HTML/CSS" description="HTML/CSSを正しく設計することができます。">
          <img class="card__icon" src="~@/assets/images/materials/website.svg" alt="HTML/CSS">
        </skill-card>
        <skill-card class="card" title="AdobeXD" description="デザインツールを扱うことができます。">
          <img class="card__icon" src="~@/assets/images/materials/webdesign.svg" alt="AdobeXD">
        </skill-card>
        <skill-card class="card" title="Git開発" description="GitHubでソースレビューを通した開発ができます。">
          <img class="card__icon" src="~@/assets/images/materials/git.svg" alt="Git開発">
        </skill-card>
        <skill-card class="card" title="WordPress" description="WordPressによるメディア設計が可能です。">
          <img class="card__icon" src="~@/assets/images/materials/wordpress.svg" alt="WordPress">
        </skill-card>
        <skill-card class="card" title="jQuery" description="jQueryによるUI実装が可能です。">
          <img class="card__icon" src="~@/assets/images/materials/jquery.svg" alt="jQuery">
        </skill-card>
        <skill-card class="card" title="SEO" description="SEOに適したマークアップと運営構築が可能です。">
          <img class="card__icon" src="~@/assets/images/materials/seo.svg" alt="SEO">
        </skill-card>
        <skill-card class="card" title="Gulp" description="Gulpを用いたタスクの自動化が可能です。">
          <img class="card__icon" src="~@/assets/images/materials/gulp.svg" alt="Gulp">
        </skill-card>
        <skill-card class="card" title="Sass" description="Sassを用いた効率的な開発が可能です。">
          <img class="card__icon" src="~@/assets/images/materials/sass.svg" alt="Sass">
        </skill-card>
        <skill-card class="card" title="Pug" description="Pugを用いた効率的な開発が可能です。">
          <img class="card__icon" src="~@/assets/images/materials/pug.svg" alt="Pug">
        </skill-card>
        <skill-card class="card" title="Javascript" description="Javascriptを用いた開発が可能です。">
          <img class="card__icon" src="~@/assets/images/materials/javascript.svg" alt="Javascript">
        </skill-card>
        <skill-card class="card" title="Nuxt.js" description="Nuxt.jsを用いたモダンな開発が可能です。">
          <img class="card__icon" src="~@/assets/images/materials/vue.svg" alt="Nuxt.js">
        </skill-card>
        <skill-card class="card" title="Intel" description="Intel入ってます">
          <img class="card__icon" src="~@/assets/images/materials/intel.svg" alt="Intel">
        </skill-card>
      </div>
    </div>
  </section>
</template>
<script>
import Heading from '@/components/Heading.vue'
import SkillCard from '@/components/SkillCard.vue'
export default {
  components: {
    Heading,
    SkillCard
  }
}
</script>
<style lang="scss" scoped>
.skills {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 80px 0;
  &__heading {
    margin: 0 auto;
  }
  .grid {
    display: grid;
    gap: 24px;
    grid-template-columns: repeat(3, 1fr);
  }
}
.card {
  &__icon {
    height: 80px;
  }
}
</style>
