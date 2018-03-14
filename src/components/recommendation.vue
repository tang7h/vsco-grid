<template>
  <div class="page">
    <div class="recommendation-item">
      <div class="recomendation-dislike">close</div>
      <div class="artist-gallery">
        <div class="gallery-item artist-profile"></div>
        <div class="airtist-pictures">
          <div class="gallery-item artist-picture"
          v-for="(i, index) in pictureList"
          :key="index"
          :style="{background: i.background, paddingTop: i.size /4 * 100 + '%'}"

          ></div>
        </div>

      </div>

      <div class="artist-action">
        <div class="airtist-information">
          <div class="artist-nickname">hellodevincastro</div>
          <div class="">DEVIN CASTRO</div>
        </div>
        <button class="artist-follow">关注</button>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {
      pictureList: [
        {
          size: 1.2,
          background: '#c6765a'
        },
        {
          size: 1.4,
          background: '#d8ca73'
        },
        {
          size: 0.75,
          background: '#3d3f2c'
        }
      ]
    }
  }
}
</script>

<style>
  body {
    margin: 0;
    font-family: sans-serif;
    line-height: 1.5;
    font-size: 14px;
  }
  * {
    box-sizing: border-box;
  }


  .page {
    /* display: grid; */
    grid-template-columns: 24px [edge-left] auto [edge-right] 24px;
  }
  .recommendation-item {
    /* grid-column: 2 / -2; */
    padding: 24px;
  }

  .artist-gallery {
    /* display: grid;
    grid-template-columns: repeat(4, 1fr 8fr) 1fr;
    align-items: end; */
    display: flex;
    align-items: flex-end;
    margin: 40px 0;
  }
  .gallery-item {
    width: 27.4%;
    flex: none;
    position: relative;
    opacity: .8;
  }
  .artist-picture {
    margin-left: -3.3%;
  }

  .airtist-pictures {
    display: contents;
  }


  .artist-follow {
    height: 36px;
    padding: 0 16px;
    border: 1px solid;
    border-radius: 0;
    background: none;
    font-size: 14px;
    color: #ad9959;
    border-radius: 2px;
  }
  .artist-profile {
    border-radius: 50%;
    padding-top: 27.4%;
    background: #cc7f86;
    grid-column: 1 / span 3;
    grid-row: 1;
  }
  .artist-action {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .artist-nickname {
    font-weight: bold;
  }
</style>
