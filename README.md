# StokGuncelleme

import java.util.Scanner;

public class StokTakip  {
    private int stokSayisi;
    private String [] stoklar;
    private int indeks;
    public StokTakip(int stokSayisi){
        this.stoklar = new String[stokSayisi];
        this.stokSayisi= stokSayisi;
        this.indeks=indeks;
    }
    public void stokEkle (Scanner scanner){
        for (int i = 0; i < stokSayisi; i++) {
            System.out.println(i+1 + " . ürün ekle ");
            stoklar [i]= scanner.next();
        }

    }

    public void stokCıkar(Scanner scanner){

        if(indeks >= 0 && indeks < stokSayisi){
            for (int i = 0; i < stokSayisi-1 ; i++) {
                stoklar[i]= stoklar[ i+1 ];//
            }
            stokSayisi--;

            }
    }


    public void stokYazir() {
        System.out.println("stoklar guncellendi");
        for (int i = 0; i < stokSayisi; i++) {
            System.out.println(stoklar[i]+ "  ");

        }

    }

} 

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

 System.out.println("stok güncelleme. kac ürün eklenecek  ");
        int stokSayisi = scanner.nextInt();
        StokTakip stokTakip = new StokTakip(stokSayisi);

        stokTakip.stokEkle(scanner);
        System.out.println(" kacıncı satır cıkıyor ");
        int cıkacak = scanner.nextInt();

        stokTakip.stokCıkar(scanner);

        stokTakip.stokYazir();


        scanner.close();
}}


