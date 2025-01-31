<script setup>
import Information from "./components/Information.vue";
import Bottom from "./components/Bottom.vue";
</script>

<template>
  <div>
    <div class="align-content-center">
      <h1>
        中推耻辱柱
        <small class="text-body-secondary">Hall Of Shame in Twitter(X)</small>
      </h1>
      <figure>
        <blockquote class="blockquote">
          <p>在此对肇事者提出谴责</p>
        </blockquote>
        <figcaption class="blockquote-footer">
          它要是知道悔改，就不会有这一步了
        </figcaption>
      </figure>
    </div>
    <h2>项目目的</h2>
    <p>
      此项目为了记录和公开在Twitter(X)上所有恶意注册的账号和这些人的恶行，同时对所有被冒仿的受害者表示同情以及对肇事者的声讨
    </p>
    <p>
      <span class="fa fa-github"/>
      <a href="https://github.com/northgreen/zyn-publiic">项目地址</a>|
      <a href="https://github.com/northgreen/zyn-record">记录仓库地址</a><br/>
      <span class="fa fa-dot-circle-o"/><a href="https://github.com/northgreen/zyn-record/issues/new?template=temple.yaml">汇报一个新的ZYN账号</a>
    </p>
    <Information/>
    <Bottom/>
  </div>
</template>

<style scoped>
</style>
