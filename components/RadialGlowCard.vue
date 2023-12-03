<script lang="ts" setup>
const features = [
  {
    icon: 'i-heroicons-banknotes-solid',
    title: ' Lorem ipsum dolor sit amet.',
    content:
      ' Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe voluptatem minima ex harum accusantium itaque dignissimos fugiat magnam repudiandae accusamus?',
  },
  {
    icon: 'i-heroicons-banknotes-solid',
    title: ' Lorem ipsum dolor sit amet.',
    content:
      ' Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe voluptatem minima ex harum accusantium itaque dignissimos fugiat magnam repudiandae accusamus?',
  },
  {
    icon: 'i-heroicons-banknotes-solid',
    title: ' Lorem ipsum dolor sit amet.',
    content:
      ' Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe voluptatem minima ex harum accusantium itaque dignissimos fugiat magnam repudiandae accusamus?',
  },
  {
    icon: 'i-heroicons-banknotes-solid',
    title: ' Lorem ipsum dolor sit amet.',
    content:
      ' Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe voluptatem minima ex harum accusantium itaque dignissimos fugiat magnam repudiandae accusamus?',
  },
  {
    icon: 'i-heroicons-banknotes-solid',
    title: ' Lorem ipsum dolor sit amet.',
    content:
      ' Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe voluptatem minima ex harum accusantium itaque dignissimos fugiat magnam repudiandae accusamus?',
  },
  {
    icon: 'i-heroicons-banknotes-solid',
    title: ' Lorem ipsum dolor sit amet.',
    content:
      ' Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe voluptatem minima ex harum accusantium itaque dignissimos fugiat magnam repudiandae accusamus?',
  },
]

onMounted(() => {
  const featuresEl = document.querySelector('.features')
  const featureEls = document.querySelectorAll('.feature')
  featuresEl!.addEventListener('pointermove', (ev) => {
    featureEls.forEach((featureEl) => {
      // Not optimized yet, I know
      const rect = featureEl.getBoundingClientRect()
      featureEl.style.setProperty('--x', ev.clientX - rect.left)
      featureEl.style.setProperty('--y', ev.clientY - rect.top)
    })
  })
})
</script>

<template>
  <div class="flex w-full flex-col items-center justify-center">
    <LandingSection title="What we offer" headline="Features" />
    <div class="features">
      <div v-for="f in features" :key="f.title" class="feature">
        <a href="#" class="feature-content">
          <!-- <UIcon :name="f.icon" /> -->
          <strong>{{ f.title }}</strong>
          <span>{{ f.content }}</span>
        </a>
      </div>
    </div>
  </div>
</template>

<style scoped>
*,
*:before,
*:after {
  box-sizing: border-box;
  position: relative;
}

.features {
  width: 75vw;
  height: 50vh;

  display: grid;
  grid-column-gap: 0.3rem;
  grid-row-gap: 0.3rem;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(2, 1fr);
}

.feature {
  --x-px: calc(var(--x) * 1px);
  --y-px: calc(var(--y) * 1px);
  --border: 2px;
  background: rgba(255, 255, 255, 0.125);
  border-radius: 0.5rem;
  overflow: hidden;
  padding: 40px;
}

.feature:before,
.feature:after {
  content: "";
  display: block;
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  inset: 0px;
  border-radius: inherit;
  background: radial-gradient(
    800px circle at var(--x-px) var(--y-px),
    rgba(246, 199, 59, 0.2),
    transparent 40%
  );
}

.feature:before {
  z-index: 1;
}

.feature:after {
  opacity: 0;
  z-index: 2;
  transition: opacity 0.4s ease;
}

.feature:hover:after {
  opacity: 1;
}

.feature-content {
  background: #131315;
  border-radius: inherit;
  color: white;
  text-decoration: none;
  z-index: 1;
  position: absolute;
  inset: var(--border);
  display: grid;
  grid-template-rows: 1fr 1fr;
  grid-row-gap: 0.5rem;
  padding: 0 1rem 0 2rem;
}

.feature-content > strong {
  align-self: self-end;
  font-size: 125%;
}

.feature-content > span {
  opacity: 0.7;
}
</style>
