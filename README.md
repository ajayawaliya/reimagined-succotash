# reimagined-succotash
fetch("http://localhost:5000/api/orders/stats")
.then(res=>res.json())
.then(data=>{
  new Chart(document.getElementById("salesChart"),{
    type:"bar",
    data:{
      labels:data.labels,
      datasets:[{
        label:"Revenue",
        data:data.values,
        backgroundColor:"#007bff"
      }]
    }
  });
});
