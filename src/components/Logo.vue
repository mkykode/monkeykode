<template>
  <div id="logo" class="clearfix">

    <div class="logo1">
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
    <div class="logo2">
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
    <div class="logo3">
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

  </div>
</template>

<script>
  export default {}
</script>

<style lang="scss">
  @import "../assets/scss/variables";

  $top: 25%;
  $right: 100%;
  $left: 0;
  $bottom: 65%;

  $left-distance: 50%;
  $right-distance: 75%;

  $random-percentage: 150%;

  $border-color-hover: $daffodil;

  #logo {
    display: block;
    cursor: crosshair;
    min-height: 110.4px;
    position: relative;
    transition: all .25s ease-out;

    svg {
      max-width: 50px;
      transition: all .25s ease-out;
    }
    .cls-1, .cls-2, .cls-3 {
      fill: none;
      stroke: #fff;
      stroke-miterlimit: 10;
      stroke-width: 1px;
    }

    &:hover {
      //transform: rotate(-180deg);
      transition: all .25s ease-out;
      .logo1, .logo2 {
        opacity: 1;
        transition: all .25s ease-out;

      }
      .logo1 {
        animation: glitch-anim-1 2s infinite linear alternate-reverse;
      }
      .logo3 {
        animation: glitch-anim-2 2s infinite linear alternate-reverse;
      }
    }
    .logo1, .logo2, .logo3 {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      min-width: 50px;
    }

    .logo1 {
      left: $left-distance;
      opacity: 0;
      .cls-1, .cls-2, .cls-3 {
        stroke: $daffodil;
        stroke-width: 2px;
      }
    }
    .logo3 {
      opacity: 0;
      left: $right-distance;
      .cls-1, .cls-2, .cls-3 {
        stroke: $daffodil;
        stroke-width: 15px;
      }
    }

    @keyframes glitch-anim-1 {
      $steps: 10;
      @for $i from 0 through $steps {
        #{percentage($i*(1/$steps))} {
          $left: random($random-percentage)+%;
          $right: random($random-percentage)+%;
          $top: random($random-percentage)+%;
          $bottom: random($random-percentage)+%;
          clip-path: polygon($left $top, $right $top, $right $bottom, $left $bottom);
          opacity: random($random-percentage)+%;
        }
      }
    }

    @keyframes glitch-anim-2 {
      $steps: 10;
      @for $i from 0 through $steps {
        #{percentage($i*(1/$steps))} {
          $left: random($random-percentage)+%;
          $right: random($random-percentage)+%;
          $top: random($random-percentage)+%;
          $bottom: random($random-percentage)+%;
          clip-path: polygon($left $top, $right $top, $right $bottom, $left $bottom);
          opacity: random($random-percentage)+%;
        }
      }
    }

  }
</style>
