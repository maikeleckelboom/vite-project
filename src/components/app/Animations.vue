<script setup lang="ts">

</script>

<template>
  <style>
    html,
    body {
      height: 100%;
      background: #f6f7fd;
      font-size: 16px;
      overflow: auto;
    }

    .snippet {
      position: relative;
      background: #fff;
      padding: 2rem 5%;
      margin: 1.5rem 0;
      box-shadow: 0 .4rem .8rem -.1rem rgba(0, 32, 128, .1), 0 0 0 1px #f0f2f7;
      border-radius: .25rem;
    }

    .examples .snippet:before {
      display: inline-block;
      position: absolute;
      top: 0;
      left: 0;
      padding: 0 5px;
      content: attr(data-title);
      font-size: .75rem;
      font-family: SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
      color: white;
      background-color: rgb(255, 25, 100);
      border-radius: .25rem 0 .25rem 0;
    }

    .stage {
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
      padding: 2rem 0;
      margin: 0 -5%;
      overflow: hidden;
    }

    .filter-contrast {
      filter: contrast(5);
      background-color: white;
    }

    .footer {
      margin: 120px 0 20px;
      text-align: center;
      overflow: auto;
    }
  </style>

  <main>
    <div class="container">
      <div class="snippet">
        🔮 <a href="https://github.com/nzbin/three-dots" target="_blank" title="three-dots">The
        project</a> is a set of CSS loading animations created with three dots which made by
        just
        single element. I think the project can not only enhance your CSS skills but also
        improve
        your imagination. 🔥
      </div>

      <div class="row examples">
        <div class="col-3">
          <div class="snippet" data-title=".dot-elastic">
            <div class="stage">
              <div class="dot-elastic"></div>
            </div>
          </div>
        </div>

        <div class="col-3">
          <div class="snippet" data-title=".dot-pulse">
            <div class="stage">
              <div class="dot-pulse"></div>
            </div>
          </div>
        </div>

        <div class="col-3">
          <div class="snippet" data-title=".dot-flashing">
            <div class="stage">
              <div class="dot-flashing"></div>
            </div>
          </div>
        </div>

        <div class="col-3">
          <div class="snippet" data-title=".dot-collision">
            <div class="stage">
              <div class="dot-collision"></div>
            </div>
          </div>
        </div>

        <div class="col-3">
          <div class="snippet" data-title=".dot-revolution">
            <div class="stage">
              <div class="dot-revolution"></div>
            </div>
          </div>
        </div>

        <div class="col-3">
          <div class="snippet" data-title=".dot-carousel">
            <div class="stage">
              <div class="dot-carousel"></div>
            </div>
          </div>
        </div>

        <div class="col-3">
          <div class="snippet" data-title=".dot-typing">
            <div class="stage">
              <div class="dot-typing"></div>
            </div>
          </div>
        </div>

        <div class="col-3">
          <div class="snippet" data-title=".dot-windmill">
            <div class="stage">
              <div class="dot-windmill"></div>
            </div>
          </div>
        </div>

        <div class="col-3">
          <div class="snippet" data-title=".dot-bricks">
            <div class="stage">
              <div class="dot-bricks"></div>
            </div>
          </div>
        </div>

        <div class="col-3">
          <div class="snippet" data-title=".dot-floating">
            <div class="stage">
              <div class="dot-floating"></div>
            </div>
          </div>
        </div>

        <div class="col-3">
          <div class="snippet" data-title=".dot-fire">
            <div class="stage">
              <div class="dot-fire"></div>
            </div>
          </div>
        </div>

        <div class="col-3">
          <div class="snippet" data-title=".dot-spin">
            <div class="stage">
              <div class="dot-spin"></div>
            </div>
          </div>
        </div>

        <div class="col-3">
          <div class="snippet" data-title=".dot-falling">
            <div class="stage">
              <div class="dot-falling"></div>
            </div>
          </div>
        </div>

        <div class="col-3">
          <div class="snippet" data-title=".dot-stretching">
            <div class="stage">
              <div class="dot-stretching"></div>
            </div>
          </div>
        </div>
      </div>

      <div class="snippet">
        ⚗️ Experiment: The experimental loading animation needs special conditions.
      </div>

      <div class="row examples">

        <div class="col-3">
          <div class="snippet" data-title=".dot-gathering">
            <div class="stage filter-contrast">
              <div class="dot-gathering"></div>
            </div>
          </div>
        </div>

        <div class="col-3">
          <div class="snippet" data-title=".dot-hourglass">
            <div class="stage filter-contrast">
              <div class="dot-hourglass"></div>
            </div>
          </div>
        </div>

        <div class="col-3">
          <div class="snippet" data-title=".dot-overtaking">
            <div class="stage filter-contrast">
              <div class="dot-overtaking"></div>
            </div>
          </div>
        </div>

        <div class="col-3">
          <div class="snippet" data-title=".dot-shuttle">
            <div class="stage filter-contrast">
              <div class="dot-shuttle"></div>
            </div>
          </div>
        </div>

        <div class="col-3">
          <div class="snippet" data-title=".dot-bouncing">
            <div class="stage">
              <div class="dot-bouncing"></div>
            </div>
          </div>
        </div>

        <div class="col-3">
          <div class="snippet" data-title=".dot-rolling">
            <div class="stage">
              <div class="dot-rolling"></div>
            </div>
          </div>
        </div>

      </div>

    </div>
  </main>

  <footer class="footer text-center">
    <p>
      Created with ❤️ by <a href="https://github.com/nzbin" target="_blank">nzbin</a>.
      Made with <a href="https://github.com/nzbin/snack" target="_blank">snack</a>.
    </p>
  </footer>
</template>