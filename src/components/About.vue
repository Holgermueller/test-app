<template>
  <div id="About" class="about">
    <div class="image">
      <div class="caption">
        <span class="border">ABOUT</span>
      </div>
    </div>

    <div class="about-content body-1">
      <p class="about-paragraph hidden">
        I'm a designer and web developer living in Batesville, Arkansas. I like
        art and tech, and I like to bring them together in an attempt to make
        cool-looking things.
      </p>

      <p class="about-paragraph hidden">
        Originally from Upstate New York, I moved to Batesville, Arkansas
        halfway through 2022 so my wife could pursue her dream job, working at a
        small liberal arts college. Prior to Arkansas, I lived in Minneapolis,
        MN, where I endured the winters for seven years. During that time, I
        earned my full-stack web developer certificate through the University of
        Minnesota's College of Continuing Education. Through that program, I've
        become proficient in Javascript, jQuery, React, VueJs, Google's Cloud
        Firebase, MongoDB, and a few other technologies. Currently, I'm dipping
        my toes into Python, mainly because it has the coolest name of all the
        programming languages; it has nothing to do with building an AI that
        will help me take over the world. My plan of attack on projects is to
        break the overall task into the smallest manageable pieces and build up
        from there. And I'm happiest when solutions can be accomplished with
        just a line or two of code.
      </p>
      <p class="about-paragraph hidden">
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

      <!-- <p class="about-paragraph hidden">
        And yes, I realize that first paragraph and this one (depending on the
        screen size) are centered while the others aren't. I like it that way.
      </p> -->
    </div>
  </div>
</template>

<script>
export default {
  name: "AboutPage",

  data: () => ({
    observer: null,
  }),

  mounted() {
    this.observer = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("show");
        } else {
          entry.target.classList.remove("show");
        }
      });
    });

    const hiddenElements = document.querySelectorAll(".hidden");
    hiddenElements.forEach((el) => this.observer.observe(el));
  },
};
</script>

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
  width: 100%;
  height: 500px;
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
  display: grid;
  place-items: center;
  align-content: center;
}
.about-paragraph {
  text-align: justify;
  text-justify: inter-word;
  margin: 4% 10%;
  font-size: 1.125rem;
}
.about-paragraph:first-child {
  margin-top: 12%;
}
.about-content:last-child {
  margin-bottom: 4%;
}

.hidden {
  opacity: 0;
  filter: blur(5px);
  transform: translateX(-100%);
  transition: all 1s;
}

.show {
  opacity: 1;
  filter: blur(0);
  transform: translateX(0);
}

@media (prefers-reduced-motion) {
  .hidden {
    transition: none;
  }
}
</style>
