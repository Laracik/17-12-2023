TASARLAYICI
#include <iostream>
#include <string>
using namespace std;


class Yarismaci {
public:
    string ad;
    string soyad;
    string sehir;
    int puan;
};


class Sunucu {
public:
    void yarismaciBilgileriniGoster(Yarismaci yarismaci) {
        cout << "Ad: " << yarismaci.ad << endl;
        cout << "Soyad: " << yarismaci.soyad << endl;
        cout << "Sehir: " << yarismaci.sehir << endl;
        cout << "Puan: " << yarismaci.puan << endl;
    }
};

int main() {

    Yarismaci yarismaci1;
    yarismaci1.ad = "Fatih";
    yarismaci1.soyad = "Ozcelik";
    yarismaci1.sehir = "Ankara";
    yarismaci1.puan = 100;

    Yarismaci yarismaci2;
    yarismaci2.ad = "Zeynep";
    yarismaci2.soyad = "Kaya";
    yarismaci2.sehir = "Mugla";
    yarismaci2.puan = 150;

    Yarismaci yarismaci3;
    yarismaci3.ad = "Kubra";
    yarismaci3.soyad = "Demir";
    yarismaci3.sehir = "Nigde";
    yarismaci3.puan = 120;


    Sunucu sunucu;
    sunucu.yarismaciBilgileriniGoster(yarismaci1);
    sunucu.yarismaciBilgileriniGoster(yarismaci2);
    sunucu.yarismaciBilgileriniGoster(yarismaci3);

    return 0;
}
KODLAYICI
#include <iostream>
#include <string>
using namespace std;

class Pazarlik {
public:
    double eskiFiyat;
    double yeniFiyat;
    string teklifEden;

    void goster() {
        cout << "Eski Fiyat: " << eskiFiyat << endl;
        cout << "Yeni Fiyat: " << yeniFiyat << endl;
        cout << "Teklif Eden: " << teklifEden << endl;
    }

    void indirim(double indirimOrani) {
        double indirimMiktari = eskiFiyat * indirimOrani;
        yeniFiyat = eskiFiyat - indirimMiktari;
        cout << "Yeni Fiyat (Indirim Uygulandi): " << yeniFiyat << endl;
    }
};

int main() {
    Pazarlik pazarlik;

    pazarlik.eskiFiyat = 100.0;
    pazarlik.yeniFiyat = 0.0;
    pazarlik.teklifEden = "Ahmet";

    pazarlik.goster();

    pazarlik.indirim(0.1);

    return 0;
}


