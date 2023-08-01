# ATM PROJESİ ÖDEVİ

* Switch case kullanılarak yapıldı.

```
package DongulerPratik;

import java.util.Scanner;

public class AtmProjesi {
    public static void main(String[] args) {
        String userName,password;
        Scanner input = new Scanner(System.in);
        int right=3;
        int balance=1500;
        int select;
        while (right>0){
            System.out.print("Kullanıcı Adınız : ");
            userName=input.nextLine();
            System.out.print("Parolanız : ");
            password=input.nextLine();
            if (userName.equals("patika") && password.equals("dev123")){
                System.out.println("Merhabe, Kodluyoruz Bankasına Hosşgeldiniz.");
                do {
                    System.out.println("1-Para Yatırma\n" +
                            "2-Para Çekme\n" +
                            "3-Bakiye Sorgulama\n" +
                            "4-Çıkıs Yap");
                    System.out.println("Lütfen Yapmak İstediğiniz İşlemi Seçiniz");
                    select=input.nextInt();
                    switch (select){
                        case 1:
                            System.out.print("Para Miktarı : ");
                            int price = input.nextInt();
                            balance+=price;
                            break;
                        case 2:
                            System.out.print("Para Miktarı : ");
                            price = input.nextInt();
                            if (price>balance){
                                System.out.println("Yetersiz Bakiye");
                            }else {
                                balance-=price;
                            }
                            break;
                        case 3:
                            System.out.println("Toplam Bakiye : "+balance);
                    }

                }while (select!=4);
                System.out.print("Tekrar Görüşmek Üzere...");
                break;
            }else {
                right--;
                System.out.println("Hatalı Giriş Yaptınız. Lütfen Tekrar Deneyiniz.");
                if (right==0){
                    System.out.println("Hesabınız Bloke Olmuştur.Lütfen Banka İle İletişime Geçiniz.");
                }else {
                    System.out.println("Kalan Hakkınız : "+right);
                }
            }
        }
    }
}
```

# Patika Profilim
<a href="https://academy.patika.dev/tr/profile">patika linki</a>