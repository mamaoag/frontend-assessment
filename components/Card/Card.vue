<template>
  <div class="card p-4">
    <div class="card__image">
      <img :src="image" :alt="imageAlt" />
      <span class="watermark">Powered by HTML.COM</span>
    </div>
    <div class="card__content mt-2">
      <p>{{ content }}</p>
      <div class="card__action mt-2">
        <button>Read More</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CardComponent',
  props: {
    content: {
      type: String,
      required: false,
      default: '',
    },
    image: {
      type: String,
      required: false,
      default: 'http://via.placeholder.com/400x300',
    },
    imageAlt: {
      type: String,
      required: false,
      default:
        'Picture with gray background with 400x300 as text on the center',
    },
  },
}
</script>

<style>
.card {
  border: 2px solid #ebebeb;
  border-radius: 12px;
  max-width: 328px;
  margin-left: 0.5rem;
  margin-right: 0.5rem;
  margin-bottom: 2.5rem;
}

.card__image {
  position: relative;
}

.card__image img {
  border-radius: 12px;
  width: 100%;
  object-fit: contain;
}

.card__image img {
  border-radius: 12px;
  max-width: 280px;
  object-fit: contain;
}

.card__image .watermark {
  font-size: 0.65rem;
}

.card__content {
  display: flex;
  flex-direction: column;
  flex-grow: 1;
  justify-content: space-between;
}

.card__content p {
  word-wrap: break-word;
  text-align: center;
  line-clamp: 7;
}

.card__action {
  display: flex;
  justify-content: center;
}

.card__action > button {
  border: 4px solid #333;
  border-radius: 30px;
  text-transform: uppercase;
  color: #000;
  letter-spacing: 0.1rem;
  font-weight: bold;
  padding: 0.5rem 1rem;
  background: #fff;
  margin: auto;
  transition: ease-in 0.15s;
}

.card__action > button:hover {
  color: #fff;
  background: #333;
}
</style>
