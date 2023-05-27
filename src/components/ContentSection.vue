<template>
  <div class="content">
    <h3>This is {{ mode }} mode</h3>
    <div class="image-grid">
      <div class="col">
        <img
          src="https://i.pinimg.com/originals/f1/3d/55/f13d55b5392448a6739e8dda8d3fc77f.png"
        />
      </div>
      <div class="col">
        <img
          src="https://i.pinimg.com/originals/18/df/97/18df97a89abd65c27c5b2458af394378.png"
        />
      </div>
      <div class="col">
        <img
          src="https://i.pinimg.com/originals/8b/1c/31/8b1c31b048cc6f2b685439c739092204.png"
        />
      </div>
    </div>
    <p class="paragraph">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde distinctio
      cupiditate earum atque sint laboriosam incidunt repellat suscipit rerum
      dolores quae fugit molestias officia beatae vitae ducimus, ipsa nesciunt
      voluptates neque maxime dolor laborum! Expedita tenetur est aperiam ab
      porro veritatis adipisci reprehenderit numquam nesciunt voluptate, illo
      voluptatem recusandae sint.
    </p>
  </div>
</template>

<script>
export default {
  props: ["mode"],
};
</script>

<style lang="scss">
.content {
  padding: 25px;
  h3 {
    font-size: 28px;
    text-transform: uppercase;
    font-weight: 300;
    margin-bottom: 25px;
  }
  .image-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 15px;
    .col {
      img {
        width: 100%;
      }
    }
  }
  .paragraph {
    width: 100%;
    max-width: 600px;
    margin: 25px auto 0px;
  }
}
</style>
