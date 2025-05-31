# COMPARISON-QUERY-nosql
#Nama : Muh Alfiansyah Akbar 
#NIM : D0222326

1. Buku dengan stok lebih dari 3
db.buku.find({ stok: { $gt: 3 } });
2. Buku yang diterbitkan pada tahun 2021 atau setelahnya
db.buku.find({ tahun: { $gte: 2021 } });
3. Buku dengan stok kurang dari atau sama dengan 2
db.buku.find({ stok: { $lte: 2 } });
4. Buku yang bukan tahun 2020
db.buku.find({ tahun: { $ne: 2020 } });
5. 📒 Buku yang tahun terbitnya adalah 2020, 2021, atau 2023
db.buku.find({ tahun: { $in: [2020, 2021, 2023] } });
6. 📓 Buku yang stok-nya bukan 0, 1, atau 2
db.buku.find({ stok: { $nin: [0, 1, 2] } });
db.buku.find({
  $and: [
    { stok: { $gt: 2 } },
    { tahun: { $gte: 2021 } }
  ]
});
