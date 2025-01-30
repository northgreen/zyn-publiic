<script setup>
import Card from "./Card.vue";
import axios from "axios";
import {onMounted, ref} from "vue";

let link = "https://raw.githubusercontent.com/northgreen/zyn-record/refs/heads/main/data/data.json"

let data = ref(null)
let l = ref(null)
let headers = axios.defaults.headers
headers.common["Cache-Control"] = "max-age:30"
const fetchData = async () => {
  try {
    const response = await axios.get(link,headers);
    data.value = response.data.data;
    l.value = response.data.data.length;
  } catch (error) {
    console.error('Error fetching data:', error);
  }
};

onMounted(fetchData)
</script>

<template>
  <div class="inform">
    <h2 class="tittle h2" id="main-tittle">
      张钰宁
    </h2>
    <p>
      中国大陆居民，冒充惯犯{{ l }}次有记录（本站）地冒充正常活动的twitter账号，
      并且使用极端的恶劣言语辱骂与其毫无关系的账户，情节恶劣，不知悔改,
      但是因为外网追查难度大所以很长时间使其逍遥法外

    </p>
    <div class="container">
      <div class="row">
        <p class="col-12 col-md-8">
          其个人信息：<br/>
          身份证号：140105200806220091<br/>
          性别：男<br/>
          出生日期：2008/06/22<br/>
          民族：汉<br/>
          住址：山西省太原市小店区<br/>
        </p>
        <img src="/src/assets/zyn.jpg" class="col-12 col-md-4 rounded float-end" alt="zyn"/>
      </div>
    </div>

    <div class="clearfix"/>
    <p>
      将会在此处列出所有由zyn创建的非法账户与对应的受害者：
    </p>

    <div class="container">
      <div class="d-flex flex-wrap row">
        <Card v-for="item in data"
              :icon="item.icon"
              :name="item.name"
              :link="item.link"
              :desc="item.desc"
              :ori_link="item.ori_link"
        />
      </div>
    </div>
  </div>
</template>

<style scoped>
#main-tittle {
  text-align: center;
  color: red;
}

.inform {
  margin: 10px;
  border: 2px solid #d9d9d9;
  padding: 10px;
  border-radius: 5px;
}
</style>