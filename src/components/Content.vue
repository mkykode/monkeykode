<template>
  <div>
    <main>
      <logo></logo>
      <div class="clearfix"></div>
      <h1>Monkey Kode</h1>
      <h2>Jull Weber</h2>
      <div class="talks">
        <h4>Talks</h4>

        <ul>
          <li><a href="https://mkykode.github.io/http2" target="_blank">Moving towards performance with HTTP/2</a></li>
          <li><a href="https://mkykode.github.io/devtools" target="_blank">Deep Dive into Chrome Dev Tools</a></li>
        </ul>
      </div>

    </main>

  </div>
</template>

<script>
  import Logo from './Logo.vue'

  export default {
    components: {
      Logo
    }
  }
</script>

<style lang="scss">

  main {
    margin: 0 17%;

    border-radius: 10px;
    background-color: rgba(0, 0, 0, .25);
    padding: 4em 2em;
    @media only screen and (max-width: 758px) {
      margin: 0 5%;
    }
    h1 {
      margin-bottom: 0;
    }
    h2 {
      font-weight: 400;
    }
    small {
      font-size: .95rem;
      font-weight: 100;
      letter-spacing: 3px;

    }

    .talks {
      position: relative;
      margin-top: 9.5%;

      h4 {
        font-size: .85rem;
        font-weight: 100;
        letter-spacing: 2px;
        position: absolute;
        text-transform: uppercase;
        left: 0;
        top: 0;
        transform: rotate(-90deg);
        text-align: right;
      }
      ul > li {
        /*margin-left: 20%;*/
        text-align: left;
        margin-left: 20px;
        list-style: circle;
        padding-top: 3px;
        a {
          transition: all .25s ease-out;
          &:hover {
            color: white;
            transform: translateX(2%) skew(-9deg);
            transition: all .25s ease-out;
          }
        }
      }
    }

  }


</style>
