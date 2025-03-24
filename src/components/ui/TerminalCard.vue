<template>
    <div class="max-w-md mx-auto p-4 bg-gray-900 text-green-400 rounded-lg shadow-lg font-code">
      <!-- Barra do terminal -->
      <div class="flex items-center space-x-2 bg-gray-800 p-2 rounded-t-lg">
        <span class="w-3 h-3 bg-red-500 rounded-full"></span>
        <span class="w-3 h-3 bg-yellow-500 rounded-full"></span>
        <span class="w-3 h-3 bg-green-500 rounded-full"></span>
      </div>
  
      <!-- Conteúdo do terminal -->
      <div class="p-4">
        <p v-for="(line, index) in content" :key="index" class="text-sm">
          <span class="text-blue-400">rnoleto@portfolio</span>:~$ <span class="text-white">{{ line }}</span>
        </p>
  
        <!-- Se houver um botão de ação -->
        <div v-if="buttonText" class="mt-4">
          <p class="text-sm">
            <span class="text-blue-400">rnoleto@portfolio</span>:~$ <button @click="onButtonClick" class="bg-green-600 px-3 py-1 rounded text-white hover:bg-green-700">{{ buttonText }}</button>
          </p>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  // Recebe as props do componente
  defineProps({
    content: {
      type: Array,
      required: true,
    },
    buttonText: {
      type: String,
      required: false,
      default: '',
    },
    onButtonClick: {
      type: Function,
      required: false,
      default: () => {},
    },
  });
  </script>
  
  <style scoped>
  /* Estilo do botão quando estiver hover */
  button:hover {
    cursor: pointer;
  }
  </style>
  