<template>
  <div class="HomeAboutGDG">
    <div class="HomeAboutGDG__container container">
      <clazy-load src="/assets/gdg.png" :threshold="0">
        <transition name="fade" appear>
          <div class="HomeAboutGDG__image"></div>
        </transition>
        <div class="preloader" slot="placeholder"></div>
      </clazy-load>

      <div class="HomeAboutGDG__about">
        <h1 class="section-title">About GDG Vientiane</h1>
        <p>Google Developer Group Vientiane is inspired by GTUG/GDG Family . We started our journey in late 2010. We try to engage student developers, fresh graduates and professionals through our hack events & meetups. The motive is to create a local ecosystem of programmers & hackers in and around Vientiane. </p>
        <a
          class="button-link"
          target="_blank"
          rel="noreferrer"
          href="https://gdgvientiane.org/team"
        >Meet the Team</a>
      </div>
    </div>
  </div>
</template>


<style lang="sass">
@import '../assets/style'
.HomeAboutGDG
  background-color: $color-surface
  // background: url(/assets/abstract-background.png)
  // background-size: cover


  &__container
    padding: 2rem 1rem
    @include from($tablet)
      padding: 3rem
    @include from($desktop)
      display: flex
      align-items: stretch
      align-content: stretch
    @include from($hd)
      padding: 4rem 3rem

  &__image
    background: url(/assets/gdg.png)
    background-size: cover
    background-position: center
    background-repeat: no-repeat

  &__image, .loaded
    width: 100%
    
    margin: auto
    border-radius: 1rem
    height: 250px
    @include from($tablet)
      height: 300px
    @include from($desktop)
      margin-right: 3rem
      max-width: 40vw
    @include from($hd)
      height: 400px

  &__about
    @include from($hd)
      width: 50%

  
</style>