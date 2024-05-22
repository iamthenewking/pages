<template>
  <button @click="aboutModal.openModal(); isSidebarActive = false;" class="btn-icon-secondary ml-auto group relative">
    <Icon name="HelpCircle" class="h-4 w-4 stroke-2"/>
    <div class="tooltip-top-right">About Pages CMS</div>
  </button>
  <!-- About modal -->
  <Modal ref="aboutModal">
    <template #header>About Pages CMS</template>
    <template #content>
      <p class="text-neutral-500">Pages CMS is an Open Source Content Management System built for static websites
      (Jekyll, Next.js, VuePress, Hugo, etc). It allows you to edit your website's content directly on GitHub via
      a user-friendly interface.</p>
       
    </template>
  </Modal>
</template>

<script setup>
import { ref } from 'vue';
import Modal from '@/components/utils/Modal.vue';
import Icon from '@/components/utils/Icon.vue';

const aboutModal = ref(null);

const openModal = () => {
  aboutModal.value.openModal();
};

defineExpose({ openModal });
</script>