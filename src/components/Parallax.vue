<script lang="ts" setup>
import type {CSSProperties} from 'vue-demi'
import {computed, reactive, ref} from 'vue-demi'
import {useMediaQuery, useParallax} from '@vueuse/core'

const target = ref(null)
const isMobile = useMediaQuery('(max-width: 700px)')
const parallax = reactive(useParallax(target))
const targetStyle: CSSProperties = {
  display: 'flex',
  flexDirection: 'column',
  justifyContent: 'center',
  minHeight: '500px',
  transition: '.3s ease-out all',
}
const cardWindowStyle: CSSProperties = {
  overflow: 'hidden',
  fontSize: '6rem',
  position: 'absolute',
  top: 'calc(50% - 1em)',
  left: 'calc(50% - 1em)',
  height: '2em',
  width: '2em',
  margin: 'auto',
}
const layerBase: CSSProperties = {
  position: 'absolute',
  height: '100%',
  width: '100%',
  transition: '.3s ease-out all',
}
const containerStyle: CSSProperties = {
  margin: '3em auto',
  perspective: '300px',
}
const infoStyle = computed(() => ({
  opacity: 0.4,
  top: '20px',
  left: '40px',
  position: isMobile.value ? 'inherit' : 'absolute',
}))

const layer0 = computed(() => ({
  ...layerBase,
  transform: `translateX(${parallax.tilt * 10}px) translateY(${
      parallax.roll * 10
  }px) scale(1.33)`,
}))

const layer1 = computed(() => ({
  ...layerBase,
  transform: `translateX(${parallax.tilt * 20}px) translateY(${
      parallax.roll * 20
  }px) scale(1.33)`,
}))

const layer2 = computed(() => ({
  ...layerBase,
  transform: `translateX(${parallax.tilt * 30}px) translateY(${
      parallax.roll * 30
  }px) scale(1.33)`,
}))

const layer3 = computed(() => ({
  ...layerBase,
  transform: `translateX(${parallax.tilt * 40}px) translateY(${
      parallax.roll * 40
  }px) scale(1.33)`,
}))

const layer4 = layerBase

const cardStyle = computed(() => ({
  background: '#fff',
  height: '20rem',
  width: '15rem',
  borderRadius: '5px',
  border: '1px solid #cdcdcd',
  overflow: 'hidden',
  transition: '.3s ease-out all',
  boxShadow: '0 0 20px 0 rgba(255, 255, 255, 0.25)',
  transform: `rotateX(${parallax.roll * 20}deg) rotateY(${
      parallax.tilt * 20
  }deg)`,
}))
</script>

<template>
  <div>
    <div ref="target" :style="targetStyle">
      <pre :style="infoStyle">{{ parallax }}</pre>
      <div :style="containerStyle">
        <div :style="cardStyle">
          <div :style="cardWindowStyle">
            <img
                :style="layer0"
                alt=""
                src="https://jaromvogel.com/images/design/jumping_rabbit/page2layer0.png">
            <img
                :style="layer1"
                alt=""
                src="https://jaromvogel.com/images/design/jumping_rabbit/page2layer1.png">
            <img
                :style="layer2"
                alt=""
                src="https://jaromvogel.com/images/design/jumping_rabbit/page2layer2.png">
            <img
                :style="layer3"
                alt=""
                src="https://jaromvogel.com/images/design/jumping_rabbit/page2layer3.png">
            <img
                :style="layer4"
                alt=""
                src="https://jaromvogel.com/images/design/jumping_rabbit/page2layer4.png"
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>