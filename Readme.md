# FRESH FRUIT
Freash Fruit merupakan sebuah aplikasi yang digunakan untuk menambahkan buah-buahan kedalam keranjang, serta menampilkan gambar/icon .
Pada Aplikasi ini juga terdapat konsep MVC (Model View Controller).

## SCOPE & FUNCTIONALITIES
- User dapat menekan tombol Add untuk menambahkan buah/fruit
- User dapat menampilkan nama buah yang sudah di ADD kedalam keranjang (Listbox)
- User dapat menghapus nama uah yang sudah tampil dikeranjang (Listbox) dengan menekan tombol DELETE.

## HOW DOES IT WORKS?
Pada Method `Fruit.cs` itu merupakan Logic View yang digunakan untuk menampilkan nama buah pada listbox. berikut merupakan source codenya
``` csharp
 public string name { get; set; }

        public Fruit(string name)
        {
            this.name = name;
        }
        public string getName()
        {
            return this.name;
        }
``` 
logic model bisnis pada `MainWindow.xaml.cs` digunakan untuk menambahkan buah dengan cara menekan tombol ADD pada setiap gambar , dan menampilkannya pada listbox melalui method `Fruit.cs`.
berikut merupakan source code pada `MainWindow.xaml.cs`
``` csharp
 private void Button1_Click(object sender, RoutedEventArgs e)
        {
            Fruit anggur = new Fruit("Anggur");
            Alfiyan.addFruit(anggur);
        }

        private void Button2_Click(object sender, RoutedEventArgs e)
        {
            Fruit apel = new Fruit("Apel");
            Alfiyan.addFruit(apel);
        }

        private void Button3_Click(object sender, RoutedEventArgs e)
        {
            Fruit pisang = new Fruit("Pisang");
            Alfiyan.addFruit(pisang);
        }

        private void Button4_Click(object sender, RoutedEventArgs e)
        {
            Fruit jeruk = new Fruit("Jeruk");
            Alfiyan.addFruit(jeruk);
        }
```