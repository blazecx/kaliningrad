<template>
  <div class="gallery">
    <div v-for="item in items" :key="item.id" class="image-container" @click="toggleExpand(item)">
      <img :src="item.imageSrc" :class="{ expanded: item.isExpanded }" alt="Image">
      <div v-if="item.isExpanded" class="text-overlay">
        <!-- <p>{{ item.text }}</p> -->
        <p>{{ item.imageSrc }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { id: 1, imageSrc: './components/icons/sobor_one.png', text: 'Текст для первого изображения', isExpanded: false },
        { id: 2, imageSrc: 'https://qawithexperts.com/Images/Upload/10-01-2018/bootstrap-popup-modal-appearing-below-background-min.png', text: 'Текст для второго изображения', isExpanded: false },
        { id: 3, imageSrc: 'https://w.forfun.com/fetch/da/daf8eb568fea522f6701fb9c66378cdc.jpeg', text: 'Текст для третьего изображения', isExpanded: false },
        { id: 4, imageSrc: 'https://qawithexperts.com/Images/Upload/10-01-2018/bootstrap-popup-modal-appearing-below-background-min.png', text: 'Текст для четвертого изображения', isExpanded: false }
      ]
    };
  },
  methods: {
    toggleExpand(item) {
      item.isExpanded = !item.isExpanded;
    }
  }
};
</script>

<style scoped>
.gallery {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.image-container {
  position: relative;
  width: calc(25% - 20px);
  /* Рассчитываем ширину для четырех элементов в ряд */
  margin: 10px;
  cursor: pointer;
}

.image-container img {
  width: 100%;
  height: auto;
  transition: transform 0.5s ease;
}

.image-container img.expanded {
  transform: scale(10);
  /* Размер картинки по умолчанию */
}

.text-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: rgba(0, 0, 0, 0.5);
  color: white;
  text-align: center;
  padding: 10px;
  box-sizing: border-box;
  opacity: 0;
  transition: opacity 0.5s ease;
}

.image-container img.expanded+.text-overlay {
  opacity: 1;
}
</style>

