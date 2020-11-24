<template>
  <li class="blog">
    <nuxt-link 
      :to="localePath({ name: 'blog-slug', params: { slug: blog.name }})"
    >
      <ImageResponsive
        :imageURL="`blog/${blog.id}/_thumbnail.jpg`"
        :classes="'cardThumbnail'"
        :width="'952'"
        :height="'509'"
        :alt="blog.cardAlt" />
      <h3 class="blog__title">
        {{ blog.title }}
      </h3>
      <p class="blog__description">
        {{ blog.description }}
      </p>
    </nuxt-link>
  </li>
</template>

<script lang="js">
  export default {
    props: {
      blog: {
        type: Object
      }
    }
  }
</script>

<style lang="scss">
@import '~vuetify/src/styles/styles.sass';

.cardThumbnail {
    transition: all ease .75s;
    opacity: .7;
    &[lazy='loaded'] {
      opacity: 1;
    }
  }
  .blog {

    @media #{map-get($display-breakpoints, 'sm-and-down')} {
      padding-bottom: 0;

      &:last-child {
        margin-right: 0;
      }
    }

    &:hover {
      .blog__title {
        color: var(--v-primary-base);
      }
    }

    &__title {
      font-family: 'Tiempos Headline', Arial, sans-serif;
      color: var(--v-secondary-base);
      padding-top: 1rem;
      font-size: 2.5rem;
      transition: color .3s;
    }

    &__description {
      margin: 0;
      color: var(--v-grey-base);
    }
  }
</style>
