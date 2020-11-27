<template>
  <div class="works">
    <h1 class="content-title"><font-awesome-icon icon="hammer" class="icon"/> WORKS</h1>
    <div class="works-container">
      <div class="card">
        <ul>
          <li v-for= "(work, index) in works" :key="index">
            <span class="work-name">
            {{ work.name }}
            </span>
            <br>
            <br>
            <img :src="work.picture" @click="openModal(work)" width="313px" height="150px">
            <br>
            <br>
            <Modal :value="workData" v-show="showContent" @close="closeModal"/>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import Modal from './Modal.vue'
export default {
  name: 'Works',
  components: { Modal },
  data () {
    return {
      works: [
        {
          name: 'CATPIA',
          description: '猫カフェを共有できるアプリです。',
          tech: 'Ruby, Ruby on Rails, JavaScript, Vue.js, MySQL, AWS, Docker, CircleCI, Capistrano',
          link: 'https://cat-pia.com',
          github: 'https://github.com/tomo-0131/CATPIA_v2',
          picture: require('../assets/catpia.png'),
          id: 1
        },
        {
          name: 'Portfolio site',
          description: 'こちらのWebサイトです。Vue.jsにより制作しました。',
          tech: 'Vue.js, Netlify, VueTyperPlugin(ライブラリ), smoothScroll(ライブラリ) etc...',
          link: 'https://tomoyuki-kumagai.netlify.app/',
          github: 'https://github.com/tomo-0131/my-project',
          picture: require('../assets/webpage.png'),
          id: 2
        }
      ],
      showContent: false,
      workData: ''
    }
  },
  methods: {
    openModal (work) {
      this.showContent = true
      this.workData = work
    },
    closeModal () {
      this.showContent = false
    }
  }
}

</script>

<style lang="scss" scoped>
.works {
  margin: 160px auto;
  .works-container {
    display: inline-block;
    margin: auto;
    padding: 0;
    width: 78%;
    position: relative;
    left: 12vw;

    ul {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      list-style-type: none;
      li {
        text-align: center;
        margin-bottom: -10px;
        margin-left: 20px;
        margin-right: 20px;
        list-style: none;
        .work-name {
          font-size: 24px;
        }
        &:hover {
          cursor: pointer;
        }
      }
    }
  }
}

@media screen and (max-width: 768px){
.works {
  margin: -12px auto;
  .works-container {
    display: inline-block;
    margin: 1px auto;
    padding: 0;
    width: 100%;
    position: relative;
    left: -0.5vw;
    ul {
      display: grid;
      grid-template-columns: repeat(1, 1fr);
      list-style-type: none;
      li {
        text-align: center;
        margin-bottom: 110px;
        margin-left: 20px;
        margin-right: 20px;
        list-style: none;
        .work-name {
          font-size: 24px;
        }
        &:hover {
          cursor: pointer;
        }
      }
    }
  }
}
}
</style>
