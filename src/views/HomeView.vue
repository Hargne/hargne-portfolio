<script setup lang="ts">
import AppIcon from '@/components/AppIcon.vue'
import AppView from '@/components/AppView.vue'
import HomeSection from '@/components/HomeSection.vue'
import HomeWorkList from '@/components/HomeWorkList.vue'
import type { WorkEntry } from '@/components/HomeWorkListEntry.vue'

const work: WorkEntry[] = [
  {
    title: 'Eagle Island',
    year: 2019,
    type: 'game',
    url: 'https://store.steampowered.com/app/681110/Eagle_Island/'
  },
  {
    title: 'Kings of Israel',
    year: 2017,
    type: 'game',
    url: 'http://store.steampowered.com/app/428460'
  },
  {
    title: 'In The Gap',
    year: 2017,
    type: 'motion-picture',
    url: 'http://www.imdb.com/title/tt6678328'
  },
  {
    title: 'Bliss',
    year: 2014,
    type: 'game',
    url: 'http://store.steampowered.com/app/315450'
  },
  {
    title: 'Mördarbilen',
    year: 2014,
    type: 'motion-picture',
    url: 'https://www.imdb.com/title/tt3403328/'
  },
  {
    title: 'Angvik',
    year: 2014,
    type: 'game',
    url: 'http://store.steampowered.com/app/278890'
  },
  {
    title: 'Splotches',
    year: 2013,
    type: 'game',
    url: 'https://store.steampowered.com/app/373640/Splotches/'
  },
  {
    title: 'Lament',
    year: 2012,
    type: 'game',
    url: 'https://www.gamersgate.com/DD-LAMENT/lament'
  },
  {
    title: 'Rodent Rush',
    year: 2011,
    type: 'game',
    url: 'http://rodentrush.com/'
  },
  {
    title: 'Beyond the Black Hole',
    year: 2010,
    type: 'game',
    url: 'http://www.hempuli.com/games/games.php?title=btbh'
  },
  {
    title: 'Floating Islands Game',
    year: 2008,
    type: 'game',
    url: 'http://www.hempuli.com/games/games.php?title=fig'
  },
  {
    title: 'Ainevoltas 2',
    year: 2008,
    type: 'game',
    url: 'http://alastairjack.tumblr.com/'
  }
]
work.sort((a, b) => b.year - a.year)
</script>

<style scoped>
h1 {
  font-size: 4rem;
  line-height: 3.5rem;
  font-weight: 400;
  text-align: center;
  margin-bottom: 1rem;
  font-family: 'Tilt Prism', cursive;
}

.subtitle {
  font-size: 1rem;
  font-weight: 300;
  text-align: center;
  margin: 0;
  text-transform: uppercase;
}

.socials {
  display: flex;
  margin-top: 2rem;
  padding: 0;
  list-style-type: none;
}
.socials li {
  display: flex;
  flex-direction: column;
  font-weight: 300;
  align-items: center;
}
.socials > li:first-child {
  margin-right: 1rem;
}
.socials > li:last-child {
  margin-left: 1rem;
}
.socials a {
  transition: all 0.2s;
  display: block;
}
.socials a:hover {
  transform: scale(1.2);
}

iframe {
  max-width: 30rem;
  width: 100%;
  height: 25rem;
}
</style>

<template>
  <AppView>
    <HomeSection full-height>
      <h1>JOHAN HARGNE</h1>
      <p class="subtitle">Composer / Audio Designer</p>
      <ul class="socials">
        <li>
          <a href="https://soundcloud.com/johanhargne/tracks" target="_blank">
            <AppIcon icon="soundcloud"
          /></a>
        </li>
        <li>
          <a href="https://johanhargne.bandcamp.com/" target="_blank">
            <AppIcon icon="bandcamp" />
          </a>
        </li>
      </ul>
    </HomeSection>
    <HomeSection title="Listen">
      <iframe
        title="Johan Hargne Soundcloud"
        src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/users/3304605&auto_play=false&hide_related=true&show_comments=false&show_user=false&show_reposts=false&visual=false"
      ></iframe>
    </HomeSection>
    <HomeSection title="Previous Work">
      <HomeWorkList :entries="work" />
    </HomeSection>
    <HomeSection title="About Me" background="dark">
      <p>👋 Hi! I am Johan Hargne - a Swedish composer for games and motion pictures.</p>
      <p>
        I have been creating and playing music for as long as I can remember. Same thing can also be
        said about video games. To be able to use music to add another layer to a game is fantastic
        and I simply love to face the challenges it brings.
      </p>
      <p>
        <strong
          >Feel free to contact me if you want me to work with you on your next project!</strong
        >
      </p>
      <ul class="socials">
        <li>
          <a href="mailto:johan.hargne@gmail.com" target="_blank">
            <AppIcon icon="email" size="small" />
          </a>
          johan.hargne@gmail.com
        </li>
      </ul>
    </HomeSection>
  </AppView>
</template>
