<template>
  <transition name="modal" appear>
    <div class="modal modal-overlay" @click.self="$emit('close')">
      <div class="modal-window">
        <div class="modal-container">
          <div class="modal-left">
            <h2>{{ value.name }}</h2>
            <br>
            <img :src="value.picture" @click="openModal(work)">
          </div>
          <div class="modal-right">
            <h3 class="work-description">
              <span>作品説明</span>
            </h3>
            <p class="modal-description">{{ value.description }}</p>
            <br>
            <h3 class="tech-index">
              <span>使用技術</span>
            </h3>
            <p class="modal-tech">{{ value.tech }}</p>
            <br>
            <div class="links">
              <a :href="value.link" target="_blank" class="web-link">Website</a>
              <a :href="value.github" target="_blank" class="github-link">Github</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  name: 'Modal',
  props: ['value']
}
</script>

<style lang="scss" scoped>
.modal {
  .modal-window {
    width: 80%;
    .modal-container {
      display: flex;
      .modal-left {
        width: 100%;
        h2 {
          margin: 2vw;
          display: inline-block;
          font-weight: normal;
          font-size: 24px;
          border-bottom: 1px solid #0da8bd;
          text-align: center;
          width: 80%;
          padding-bottom: 1vw;
        }
        img {
          width: 80%;
          height: 60%;
        }
      }
      .modal-right {
        padding: 140px;
        width: 45%;
        h3 {
          padding: 0 10px;
          position: relative;
          span {
            background: #fafafa;
            padding: 0 10px;
            position: relative;
            z-index: 5;
          }
          &::before {
            content: "";
            display: block;
            border-top: solid 1px #ddd;
            width: 100%;
            height: 1px;
            position: absolute;
            top: 50%;
            z-index: 1;
          }
        }
        .links {
          a {
            border-radius: 12px;
            border: 1px solid #0da8bd;
            padding: 5px 10px;
            text-decoration: none;
            margin: 0 10px;
            color: #333;
          }
        }
      }
    }
  }
  &.modal-overlay {
    display: flex;
    align-items: center;
    justify-content: center;
    position: fixed;
    z-index: 30;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
  }
  &-window {
    background: #fff;
    border-radius: 4px;
    overflow: hidden;
  }
  &-content {
    padding: 10px 20px;
  }
  &-footer {
    padding: 10px;
    text-align: right;
  }
}
.modal-enter-active, .modal-leave-active {
  transition: opacity 0.4s;
  .modal-window {
    transition: opacity 0.4s, transform 0.4s;
  }
}
.modal-leave-active {
  transition: opacity 0.6s ease 0.4s;
}
.modal-enter, .modal-leave-to {
  opacity: 0;
  .modal-window {
    opacity: 0;
    transform: translateY(-20px);
  }
}

@media screen and (max-width: 768px) {
 .modal {
  .modal-window {
    width: 90%;
    .modal-container {
      display: inline-block;
      .modal-left {
        width: 100%;
        h2 {
          display: inline-block;
          margin: 4vw;
          font-size: 24px;
          border-bottom: 1px solid #0da8bd;
          width: 80%;
          padding-bottom: 2vw;
        }
        img {
          width: 80%;
          height: 80%;
        }
      }
      .modal-right {
        padding: 37px;
        width: 80%;
        h3 {
          padding: 1px;
          position: relative;
          span {
            background: #fafafa;
            padding: 0 10px;
            position: relative;
            z-index: 5;
          }
          &::before {
            content: "";
            display: block;
            border-top: solid 1px #ddd;
            width: 100%;
            height: 1px;
            position: absolute;
            top: 50%;
            z-index: 1;
          }
        }
        .links {
          a {
            border-radius: 12px;
            border: 1px solid #0da8bd;
            padding: 5px 10px;
            text-decoration: none;
            margin: 0 10px;
            color: #333;
          }
        }
      }
    }
  }
  &.modal-overlay {
    display: flex;
    align-items: center;
    justify-content: center;
    position: fixed;
    z-index: 30;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
  }
  &-window {
    background: #fff;
    border-radius: 4px;
    overflow: hidden;
  }
  &-content {
    padding: 10px 20px;
  }
  &-footer {
    padding: 10px;
    text-align: right;
  }
}
.modal-enter-active, .modal-leave-active {
  transition: opacity 0.4s;
  .modal-window {
    transition: opacity 0.4s, transform 0.4s;
  }
}
.modal-leave-active {
  transition: opacity 0.6s ease 0.4s;
}
.modal-enter, .modal-leave-to {
  opacity: 0;
  .modal-window {
    opacity: 0;
    transform: translateY(-20px);
  }
}
}

</style>
