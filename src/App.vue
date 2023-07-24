<script>
  import { PivotViewComponent, GroupingBar } from "@syncfusion/ej2-vue-pivotview";
  
export default{
  components: {
    "ejs-pivotview": PivotViewComponent
  },
  data()
  {
    return{
      dataSourceSettings:{
        dataSource:[
            { Amount: 5100, Country: "Canada", Date: "FY 2006", Quarter: "Q1", Product: "Car", Quantity: 21, State: "Alberta" },
            { Amount: 1900, Country: "France", Date: "FY 2007", Quarter: "Q2", Product: "Bike", Quantity: 23, State: "Alberta" },
            { Amount: 1000, Country: "Sweden", Date: "FY 2008", Quarter: "Q3", Product: "Car", Quantity: 29, State: "Alberta" },
            { Amount: 2060, Country: "Canada", Date: "FY 2006", Quarter: "Q4", Product: "Bike", Quantity: 93, State: "British Columbia" },
            { Amount: 6200, Country: "France", Date: "FY 2007", Quarter: "Q1", Product: "Car", Quantity: 36, State: "British Columbia" },
            { Amount: 2000, Country: "Sweden", Date: "FY 2008", Quarter: "Q2", Product: "Bike", Quantity: 31, State: "British Columbia" },
            { Amount: 1300, Country: "Canada", Date: "FY 2005", Quarter: "Q3", Product: "Car", Quantity: 45, State: "Brunswick" },
            { Amount: 3400, Country: "France", Date: "FY 2006", Quarter: "Q4", Product: "Bike", Quantity: 47, State: "Brunswick" },
            { Amount: 2300, Country: "Sweden", Date: "FY 2007", Quarter: "Q1", Product: "Car", Quantity: 43, State: "Brunswick" },
            { Amount: 5100, Country: "Canada", Date: "FY 2006", Quarter: "Q2", Product: "Bike", Quantity: 21, State: "Alberta" },
            { Amount: 1900, Country: "France", Date: "FY 2007", Quarter: "Q3", Product: "Car", Quantity: 23, State: "Alberta" },
            { Amount: 1000, Country: "Sweden", Date: "FY 2008", Quarter: "Q4", Product: "Bike", Quantity: 29, State: "Alberta" },
            { Amount: 2060, Country: "Canada", Date: "FY 2006", Quarter: "Q1", Product: "Car", Quantity: 93, State: "British Columbia" },
            { Amount: 6200, Country: "France", Date: "FY 2007", Quarter: "Q2", Product: "Bike", Quantity: 36, State: "British Columbia" },
            { Amount: 2000, Country: "Sweden", Date: "FY 2008", Quarter: "Q3", Product: "Car", Quantity: 31, State: "British Columbia" },
            { Amount: 1300, Country: "Canada", Date: "FY 2005", Quarter: "Q4", Product: "Bike", Quantity: 45, State: "Brunswick" },
            { Amount: 3400, Country: "France", Date: "FY 2006", Quarter: "Q1", Product: "Car", Quantity: 47, State: "Brunswick" },
            { Amount: 2300, Country: "Sweden", Date: "FY 2007", Quarter: "Q2", Product: "Bike", Quantity: 43, State: "Brunswick" },
       ],
        rows: [{name: 'Country', showSortIcon:false}, {name: 'Product', showFilterIcon:false}],
        columns: [{name:'Date', allowDragAndDrop:false}, {name:'Quarter', showRemoveIcon:false}],
        values: [{name:'Amount', caption:'Sold Amount', showValueTypeIcon:false}, {name:'Quantity', caption:'Units Sold'}],
        formatSettings: [{name:'Amount', format:'C1'}],
        filterSettings: [{name:'Product', type:'Exclude', items:['Bike']}],
        showAggregationOnValueField: false

      },
      height:'350px',
      width:'900px',
      showGroupingBar: true,
      groupingBarSettings:{
        showFieldsPanel: true,
        showFilterIcon: false,
        showSortIcon: false
       
      },
      aggregateTypes:['DistinctCount', 'Avg', 'Product']
    };
  } ,
  provide:
  {
    pivotview:[GroupingBar]
  }
}
</script>

<template>
  <ejs-pivotview :height="height" :width="width"
                 :dataSourceSettings="dataSourceSettings"
                 :showGroupingBar ="showGroupingBar"
                 :groupingBarSettings="groupingBarSettings"
                 :aggregateTypes="aggregateTypes"></ejs-pivotview>
</template>

<style >
  @import "../node_modules/@syncfusion/ej2-base/styles/bootstrap5.css";
  @import "../node_modules/@syncfusion/ej2-inputs/styles/bootstrap5.css";
  @import "../node_modules/@syncfusion/ej2-buttons/styles/bootstrap5.css";
  @import "../node_modules/@syncfusion/ej2-splitbuttons/styles/bootstrap5.css";
  @import "../node_modules/@syncfusion/ej2-calendars/styles/bootstrap5.css";
  @import "../node_modules/@syncfusion/ej2-dropdowns/styles/bootstrap5.css";
  @import "../node_modules/@syncfusion/ej2-lists/styles/bootstrap5.css";
  @import "../node_modules/@syncfusion/ej2-popups/styles/bootstrap5.css";
  @import "../node_modules/@syncfusion/ej2-navigations/styles/bootstrap5.css";
  @import "../node_modules/@syncfusion/ej2-grids/styles/bootstrap5.css";
  @import "../node_modules/@syncfusion/ej2-vue-pivotview/styles/bootstrap5.css";

 </style>


