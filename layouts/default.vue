<template>
    <Nuxt />
</template>

<style lang="sass">
html
  font-family: 'Source Sans Pro', Roboto, Arial
  font-size: 16px
  word-spacing: 1px
  box-sizing: border-box

*
  box-sizing: border-box
  margin: 0

.button--green
  display: inline-block
  border-radius: 4px
  border: 1px solid #3b8070
  color: #3b8070
  text-decoration: none
  padding: 10px 30px

.button--green:hover
  color: #fff
  background-color: #3b8070

.button--grey
  display: inline-block
  border-radius: 4px
  border: 1px solid #35495e
  color: #35495e
  text-decoration: none
  padding: 10px 30px
  margin-left: 15px

.button--grey:hover
  color: #fff
  background-color: #35495e

.close
  position: absolute
  top: 5%
  right: 5%
  cursor: pointer
  color: #000
  font-size: 12px
  font-weight: 700
  border: 1px solid #fff
  border-radius: 3px
  box-shadow: 0px 4px 48px rgba(0, 0, 0, 0.26)
  padding: 4px 8px
  &:hover
    background-color: #000
    color: #fff
  &:active
    background-color: #444
    color: red
</style>
