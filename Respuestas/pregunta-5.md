db.sensores.aggregate([
  {
    $group: {
      _id: "$zona",
      temperaturaPromedio: { $avg: "$temperatura" }
    }
  }
])