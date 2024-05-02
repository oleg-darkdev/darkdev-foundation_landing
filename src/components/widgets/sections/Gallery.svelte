<script>
  	// import cardCategories from '../data/cardCategor/ies';
</script>

<div class="grid grid-cols-2 md:grid-cols-4 gap-4  px-4">
    <div class="grid gap-4">
        <div data-filter="image-hue-rotate">
            <img class="h-auto max-w-full rounded-lg" src="/images/gallery/1.JPG" alt="photo handmade fest magnets and tools">
        </div>
        <div data-filter="image-hue-rotate" class=''>
            <img class=" max-w-full rounded-lg  max-h-[360px] object-cover w-full " src="/images/gallery/2.jpg" alt="photo handmade boardgames workshop">
        </div>
        <div data-filter="image-hue-rotate">
            <img class="h-auto max-w-full rounded-lg" src="/images/gallery/3.png" alt="photo handmade magnets">
        </div>
    </div>
    <div class="grid gap-4">
        <div data-filter="image-hue-rotate" class=''>
            <img class="my-auto h-auto max-w-full rounded-lg max-h-[340px] object-cover  w-full" src="/images/gallery/4.jpg" alt="photo education workshop for bussines">
        </div>
        <div data-filter="image-hue-rotate">
            <img class="h-auto max-w-full rounded-lg" src="/images/gallery/5.jpg" alt="photo chess tournament banner">
        </div>
        <div data-filter="image-hue-rotate">
            <img class="h-auto max-w-full rounded-lg max-h-[270px] object-cover  w-full" src="/images/gallery/6.jpg" alt="photo workshop for bussines">
        </div>
    </div>
    <div class="grid gap-4">
        <div data-filter="image-hue-rotate">
            <img class="h-auto max-w-full rounded-lg" src="/images/gallery/7.png" alt="photo chess tournament young">
        </div>
        <div data-filter="image-hue-rotate">
            <img class="h-auto max-w-full rounded-lg max-h-[360px] object-cover  w-full" src="/images/gallery/8.png" alt="photo boardgame and appication">
        </div>
        <div data-filter="image-hue-rotate">
            <img class="h-auto max-w-full rounded-lg max-h-[460px] object-cover w-full"  src="/images/gallery/9.png" alt="photo handmade fest">
        </div>
    </div>
    <div class="grid gap-4">
        <div data-filter="image-hue-rotate">
            <img class="h-auto max-w-full rounded-lg max-h-[360px] object-cover  w-full" src="/images/gallery/10.JPG" alt="photo young people on workshop ">
        </div>
        <div data-filter="image-hue-rotate">
            <img class="h-auto max-w-full rounded-lg" src="/images/gallery/11.png" alt="photo markers and bardgames">
        </div>
        <div data-filter="image-hue-rotate">
            <img class="h-auto max-w-full rounded-lg max-h-[270px] object-cover w-full" src="/images/gallery/12.JPG" alt="photo workshop for ngo ">
        </div>
    </div>
</div>



<style>
    /* @import url("https://fonts.googleapis.com/css?family=Dosis:300,800");
[data-filter*=image-] {
  flex: 0 1 20%;
  line-height: 0;
  position: relative;
  z-index: 0;
}
[data-filter*=image-] img {
  height: auto;
  width: 100%;
} */

[data-filter=image-hue-rotate] img {
  filter: hue-rotate(70%);
}

[data-filter=image-saturate] img {
  filter: saturate(360%);
}

[data-filter=image-sepia] img {
  filter: sepia(100%);
}

[data-filter=image-invert] img {
  filter: invert(100%);
}

[data-filter=image-opacity] img {
  filter: opacity(50%);
}

[data-filter=image-brightness] img {
  filter: brightness(120%);
}

[data-filter=image-contrast] img {
  filter: contrast(160%);
}

[data-filter=image-hue-rotate] img {
  filter: hue-rotate(160deg);
}

[data-filter=image-blur] img {
  filter: blur(2px);
}

body {
  background: #163065;
  color: #fff;
  font-family: "Dosis", sans-serif;
  line-height: 1;
}

main {
  display: flex;
  flex-wrap: wrap;
}

h1 {
  font-size: 2.5rem;
  font-weight: 300;
  line-height: 1;
  margin: 2rem 0 3rem;
  padding: 0;
  text-align: center;
  width: 100vw;
}
h1 span {
  color: #f8be00;
  font-size: 5rem;
  font-weight: 800;
  margin: 0;
}

h2 {
  background: rgba(100, 0, 50, 0.8);
  color: #fff;
  display: block;
  font-size: 1.25rem;
  font-weight: 300;
  left: 0;
  line-height: 1.5;
  margin: 0;
  padding: 0.5rem;
  position: absolute;
  top: 0;
  z-index: 1;
}

a {
  color: #fff;
  display: inline-block;
  font-size: 1rem;
}
a:hover {
  color: #f8be00;
}
</style>
