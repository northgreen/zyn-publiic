<script setup>
import {ref} from 'vue'

defineProps({
  name: String,
  link:String,
  icon: String,
  desc:String,
  ori_link:String
})

const count = ref(0)
</script>

<template>
  <div class="col-12 col-sm-12 col-md-5 col-lg-3 card container px-0">
    <div class="row g-0 px-0">
      <!--头部图片-->
      <div class="card-img-top-box h-auto col-4">
        <img class="img-fluid rounded-start h-auto w-100"
             :src="icon"
             alt="">
      </div>
      <!--右侧名称区域-->
      <div class="col-8">
        <div class="card-body">
          <h5 class="card-title">
            {{name}}
          </h5>
          <a :href="link">
            {{link}}
          </a>
        </div>
      </div>
      <div class="card-body">
        <p class="card-text">
          {{desc}}
        </p>
        <p>受害者:<a :href="ori_link">{{ori_link}}</a>
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.card{
  margin: 5px;
}
</style>
