<template>
  <pinyin_content :content="poetryList" :startSpace="false"/>
</template>
<script setup>
import {ref, onMounted} from "vue";
import resource from "@/util/resource.js";

const poetryList = ref()

onMounted(async ()=> {
  poetryList.value = await resource.getChinesePoetry()
})
</script>
