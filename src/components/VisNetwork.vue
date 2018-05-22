<template>
  <div>
    <div id="mynetwork"></div>
    <input name="" type="button" value="Set Nodes" @click="setNodes" />
  </div>
</template>

<script>
 import vis from 'vis'

 export default {
   data () {
     return {
       nodes: new vis.DataSet([]),
       edges: new vis.DataSet([])
     }
   },
   mounted () {
     const container = document.getElementById('mynetwork');
     const data = {
       nodes: this.nodes,
       edges: this.edges
     };
     const options = {};
     new vis.Network(container, data, options);
   },
   methods: {
     setNodes () {
       const nodesArray = [
         {id: 1, label: 'Node 1'},
         {id: 2, label: 'Node 2'},
         {id: 3, label: 'Node 3'},
         {id: 4, label: 'Node 4'},
         {id: 5, label: 'Node 5'}
       ]
       // create an array with edges
       const edgesArray = [
         {from: 1, to: 3},
         {from: 1, to: 2},
         {from: 2, to: 4},
         {from: 2, to: 5},
         {from: 3, to: 3}
       ]

       nodesArray.forEach((value) => {
         this.nodes.add(value)
       })
       edgesArray.forEach((value) => {
         this.edges.add(value)
       })
     }
   }
 }
</script>

<style>
 #mynetwork {
   width: 600px;
   height: 400px;
   border: 1px solid lightgray;
 }
</style>
