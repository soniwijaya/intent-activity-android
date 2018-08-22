### Activity Live Cycle

***Using Intent to move next page.***

First Page use .this
Second Page use .class

Intent <variable_name> = new Intent ( <right_now_page> , <next_page> )

example :
```
Intent move = new Intent ( MainActivity.this , MoveNextPage.class )
```

***If you want to bring data in Next Page you can handle with***
```
Intent moveWithData = new Intent ( MainActivity.this , MoveNextPage.class )
moveWithData.putExtra( MoveNextPage.<variable_name> , <value> )
startActivity(moveWithData)
```

Kita memanfaatkan metode ***putExtra()*** untuk mengirimkan data bersamaan dengan obyek Intent. Sedangkan metode ***putExtra()*** itu sendiri merupakan metode yang menampung pasangan *key-value* dan memiliki beberapa pilihan tipe input.

Di sini kita akan mengirimkan data bertipe string ke MoveWithDataActivity. Di dalam MoveWithdataActivity kita akan mengambil nilai data berdasarkan key yang dikirimkan dengan menggunakan metode getIntent().getStringExtra(key). Implementasinya sebagai berikut

```
String name = getIntent().getStringExtra(EXTRA_NAME);
```

***If you want to bring data in Next Page with Object, you can use parcelable***

Buat object dengan create *new* constructor contoh:
```
Person mPerson = new Person()
mPerson.setName("Ini Android")
```




