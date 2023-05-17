<template>
  <h1>{{ msg }}</h1>
  <div v-for="data in tableData" :key="data" class="text item">  
    <el-collapse @change="handleChange" shadow="hover">
      <el-collapse-item :title="data.name" name="1">
        <div>{{ data.discretion }}</div>
        <div>{{ data.date }}</div>
      </el-collapse-item>
    </el-collapse>
  </div>
</template>

<script>
export default {
  name: 'FormComp',
  props: {
    msg: String
  },
  data() {
    return {
      tableData: [{
          date: '2016-05-03 10:30 a.m.',
          name: 'Vue',
          discretion: 'Vue是一個流行的JavaScript框架，用於構建用戶界面。它是一個用於構建單頁應用程序（SPA）和可交互的網頁界面的逐漸採用的框架。Vue具有簡單易學、輕量級、高效的特點，並且易於與其他庫或現有的項目集成。它使用了基於組件的架構，使得代碼組織和重用更加容易。Vue提供了豐富的功能，如數據綁定、組件化、路由、狀態管理等，使開發人員能夠快速構建現代化的Web應用程序。'
        }, {
          date: '2016-05-02 20:49 p.m.',
          name: 'Vuex',
          discretion: 'Vuex是Vue.js的狀態管理庫，用於管理應用程序中的狀態。它解決了在大型應用程序中的組件之間共享狀態時的困難，並提供了一個集中式的狀態管理機制。Vuex的核心概念是"狀態（State）、突變（Mutations）、行動（Actions）和Getter"。狀態是應用程序中需要共享的數據，突變用於修改狀態，行動用於觸發異步操作並提交突變，Getter用於獲取狀態的計算屬性。使用Vuex，可以更好地組織和管理應用程序的狀態，使數據的流動和變更更加可控和可追蹤。'
        }, {
          date: '2016-05-04 09:21 a.m.',
          name: 'Element UI',
          discretion: 'Element UI是一個基於Vue.js的UI框架，提供了一套豐富的可重用UI組件，用於快速構建現代化的Web界面。Element UI的特點是美觀、易用、高度可定制和可擴展。它提供了各種常見的界面元素，如按鈕、表單、對話框、菜單、表格等，並且支持自定義主題和國際化。Element UI的組件設計遵循了現代化的設計標準和最佳實踐，使開發人員能夠快速構建具有一致性和優雅外觀的用戶界面。它還提供了豐富的文檔和示例，方便開發人員學習和使用。'
      }]      
    }    
  }
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
