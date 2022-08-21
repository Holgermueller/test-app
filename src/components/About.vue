<template>
  <div id="About" class="about">
    <div class="image">
      <div class="caption">
        <span class="border">ABOUT</span>
      </div>
    </div>

    <div class="about-content">
      <p class="about-paragraph">
        I'm a full-stack front-end developer living in Batesville, Arkansas.
      </p>
      <p class="about-paragraph">
        Originally from Upstate New York, I moved to Batesville, Arkansas
        halfway through 2022 so my wife could pursue her dream job, working at a
        small liberal arts college. Prior to Arkansas, I lived in Minneapolis,
        MN, where I endured the winters for seven years. During that time, I
        earned my full-stack web developer certificate through the University of
        Minnesota's College of Continuing Education. Through that program, I've
        become proficient in Javascript, jQuery, React, VueJs, Google's Cloud
        Firebase, MongoDB, and a few other technologies. My plan of attack on
        projects is to break the overall task into the smallest manageable
        pieces and build up from there.
      </p>
      <p class="about-paragraph">
        When not coding, I enjoy reading and writing, watching movies, hiking,
        and travelling. One of my longshot dreams is to visit every country on
        the planet. Some of my bucket-list destinations are Japan, New Zealand,
        Portugal, South Africa, and Iceland. So far, I've been to Australia, the
        Republic of Korea, France, Canada, and Italy. As far as reading goes,
        I've recently rediscovered my love of Science Ficiton and fantasy, and
        I've always had an affinty for Marvel Comics. With movies, I tend to
        enjoy comedies over other genres. And with music, I'm fond of many
        genres, but jazz and punk rock tend to be my favorites.
      </p>
    </div>
  </div>
</template>

<style scoped>
.about {
  justify-content: center;
  margin: auto;
  top: 0;
}
.image {
  /* image by Pixabay via Pexels */
  background-image: url("../images/book.png");
  background-size: cover;
  height: 500px;
  width: 100%;
}
.caption {
  width: 100%;
  position: relative;
  left: 0;
  top: 50%;
  text-align: center;
  color: black;
}
.caption span.border {
  background-color: #111;
  color: white;
  width: fit-content;
  font-size: 25px;
  padding: 18px;
  letter-spacing: 10px;
}
.about-content {
  margin: 7% auto;
}
.about-paragraph {
  text-align: justify;
  text-justify: inter-word;
  margin-left: 10%;
  margin-right: 10%;
}
</style>
