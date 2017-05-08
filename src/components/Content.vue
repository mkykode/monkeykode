<template>
  <div>
    <main>
      <div id="logo">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 27.51 58.67">
          <title>Logo</title>
          <g id="Layer_2" data-name="Layer 2">
            <g id="face">
              <rect class="cls-1" x="1.5" y="1.5" width="24.51" height="55.67" rx="4" ry="4"/>
              <rect class="cls-2" x="1.9" y="22.73" width="23.82" height="10.8" rx="2" ry="2"/>
              <ellipse class="cls-3" cx="8.81" cy="27.95" rx="4.61" ry="4.91"/>
              <ellipse class="cls-3" cx="18.82" cy="27.95" rx="4.55" ry="4.91"/>
            </g>
          </g>
        </svg>
      </div>
      <h1>Monkey Kode <br></h1>
      <!--<small>-&#45;&#45; playground -&#45;&#45;</small>-->
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
  export default {}
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

    #logo {
      display: flex;
      flex-flow: row nowrap;
      justify-content: center;
      align-items: center;
      svg {
        flex: 1 100%;
        max-width: 50px;
        transition: transform .25s ease-out;
        &:hover {
          transform: rotate(180deg);
          transition: transform .25s ease-out;
        }
      }
      .cls-1, .cls-2, .cls-3 {
        fill: none;
        stroke: #fff;
        stroke-miterlimit: 10;
      }

      .cls-1 {
        stroke-width: 1px;
      }

      .cls-2 {
        stroke-width: 1px;
      }

      .cls-3 {
        stroke-width: 1px;
      }
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
          &:hover {
            color: white;
            text-decoration: underline;
          }
        }
      }
    }
  }


</style>
