<template>
  <div>
    <footer>
      <ul class="inline">
        <li><a href="mailto:jull@monkeykodeagency.com">email me</a></li>
        <li><a href="https://www.monkrykodeagency.com" target="_blank">Monkey Kode Agency</a></li>
        <li><a href="https://github.com/mkykode" target="_blank">github</a></li>
      </ul>
    </footer>

  </div>
</template>

<script>
  export default {}
</script>

<style lang="scss">
  footer {
    font-size: .75rem;
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;

    ul {
      /*max-width: 20%;*/
      /*margin: 0 auto;*/
      li {
        list-style: none;
        margin-right: 20px;
        position: relative;
        &:after {
          position: absolute;
          top:0;
          right:-11px;

          content: ' - ';
        }
        &:last-child {
          &:after {
            content: ' ';
          }
        }
      }
    }
  }
</style>
