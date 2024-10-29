<script setup>
import { nextTick } from 'vue'
import { ref } from 'vue'

const videoSource = ref(null)

const videoElement = ref(null)

function onFileChange(event) {
  const file = event.target.files[0]
  console.log(file)
  if (file === null) {
    videoSource.value = null
  }
  videoSource.value = URL.createObjectURL(file)

  nextTick(() => {
    if (videoElement) {
      videoElement.value.load()
    }
  })
}
</script>

<template>
  <div
    id="container-id"
    class="flex flex-col items-center justify-center h-screen font-mono"
  >
    <div
      id="container-upload-fil"
      class="flex flex-col items-center justify-center"
    >
      <label for="upload-fil" class="mb-5 text-white text-xl"
        >Upload your Project</label
      >
      <input
        id="upload-fil"
        type="file"
        accept=".mp4"
        @change="onFileChange"
        class="p-2 border-2 border-pink-500 rounded-lg hover:cursor-pointer"
      />
    </div>

    <div id="container-player">
      <video
        id="player"
        controls
        v-if="videoSource"
        ref="videoElement"
        class="mt-10"
      >
        <source :src="videoSource" type="video/mp4" />
      </video>

      <div id="container-selection-language" v-if="videoSource">
        <h1 id="oui">Option</h1>

        <select
          name="language-chosen"
          id="select-language"
          class="rounded-lg my-auto ml-auto p-1"
        >
          <option value="EN">English 🏴󠁧󠁢󠁥󠁮󠁧󠁿</option>
          <option value="FR">French 🇫🇷</option>
        </select>

        <button
          id="send-traduction-button"
          class="my-auto mx-auto p-3 bg-lime-400 rounded-lg"
        >
          Traduire
        </button>
      </div>
    </div>
  </div>
</template>

<style scoped>
#player {
  width: 450px;
  height: 250px;
  background: #070707;
  border-radius: 10px;
}

#container-player {
  display: flex;
  padding: auto;
}
#container-selection-language {
  display: flex;
  margin: 40px;
  background-color: aliceblue;
  border-radius: 10px;
  width: 450px;
  height: 250px;
}
</style>
