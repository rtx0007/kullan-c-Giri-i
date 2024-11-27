package Exercise;

import java.util.Scanner;

public class kullanıcıGirişi {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        String userName, password1, password2;
        int select;

        System.out.print("Kullanıcı adınız: ");
        userName = input.nextLine();

        System.out.print("Şifreniz: ");
        password1 = input.nextLine();

        if (userName.equals("patika") && password1.equals("java123")) {
            System.out.println("Giriş Yaptınız!");
        } else {
            System.out.println("Bilgileriniz Yanlış!");
            System.out.println("Şifrenizi sıfırlamak ister misiniz?");
            System.out.println("1-Evet \t 2-Hayır");
            select = input.nextInt();
            input.nextLine(); // `nextInt` sonrası kalan `Enter` karakterini temizle

            if (select == 1) {
                System.out.println("Hatırlatma: Yeni şifreniz önceki şifrenizden farklı olmalıdır.");
                System.out.print("Yeni Şifreniz: ");
                password2 = input.nextLine();

                if (password1.equals(password2)) {
                    System.out.println("Şifre oluşturulamadı, lütfen başka bir şifre giriniz.");
                } else {
                    System.out.println("Şifre oluşturuldu.");
                }
            } else if (select == 2) {
                System.out.println("Şifre sıfırlama işlemi iptal edildi.");
            } else {
                System.out.println("Geçersiz seçim yaptınız.");
            }
        }
    }
}

