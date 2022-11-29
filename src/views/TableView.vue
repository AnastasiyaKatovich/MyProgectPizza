<template>
    <home-top></home-top> 
    <table-list></table-list>
    <home-footer></home-footer>

 
    <router-view/>
    </template>
    
    <script>

      import homeTop from "@/components/template/homeTop.vue";
      import tableList from "@/components/template/tableList.vue";
      import homeFooter from "@/components/template/homeFooter.vue";
      export default{
        name: "TableView",
        setup(){
            
        },
        components:{
          homeTop,
          tableList,
          homeFooter
        }
      }
    </script>