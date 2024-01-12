<!-- Admin.vue -->
<template>
    <div>
            <!-- 顯示所有投票項目 -->
        <div v-for="item in items" :key="item.id">
            {{ item.title }}
            <!-- 其他投票項目資訊... -->
        </div>
    
        <!-- 新增投票項目表單 -->
        <form @submit.prevent="addItem">
            <input v-model="newItemTitle" placeholder="新投票項目標題" />
            <button type="submit">新增</button>
        </form>
    </div>
</template>
  
<script>
    export default {
        data() {
            return {
                items: [], // 投票項目列表
                newItemTitle: '', // 新增投票項目標題
            };
        },
        methods: {
        // 從後端獲取投票項目列表
            fetchItems() {
                // 實作取得後端資料的邏輯...
            },
            // 新增投票項目
            addItem() {
                // 實作新增投票項目的邏輯...
            },
        },
        mounted() {
            this.fetchItems(); // 頁面載入時獲取投票項目列表
        },
    };
  </script>