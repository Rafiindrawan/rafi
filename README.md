# rafi
menggunakan Software C++

SOAL NOMER 1
#include<conio.h>
#include<iostream>
using namespace std;

int main()
{
	bool lajang = true;
	string name = " Muhammad Rafi Indrawan";
	string address = " Jalan Bhakti No 21 Rt 03/07 Ciputat Tangerang Selatan";
	cout<<"Name :"<<name<<endl;
	cout<<"Address :"<<address<<endl;
	char hobbies[30] = " Renang, Futsal, Design ";
	cout<<"Hobbies :"<<hobbies<<endl;
	cout<<"Is_married : "<<lajang<<endl;
	char school[30] = " Akademi Telkom Jakarta";
	char skill[15]= " Fiber Optic";
	cout<<"School :"<<school<<endl;
	cout<<"Skill :"<<skill<<endl;

	
	getch();
}

SOAL NOMER 4
#include <stdio.h>
#include <stdlib.h>

int main(){

int hargaBuah=10000;
float beratBuah;
int bayar;
int totalHarga;
int kembalian;
int limaratus,seribu,duaribu,limaribu,sepuluhribu,duapuluhribu,limapuluhribu;
int sisakembalian,sisakembalian2,sisakembalian3,sisakembalian4,sisakembalian5,sisakembalian6,sisakembalian7;

printf("masukan berat buah \t\t:"); scanf("%f",&beratBuah);
printf("masukan nilai pembayaran \t:"); scanf("%d",&bayar);
system("CLS");
totalHarga=int(beratBuah*hargaBuah);
kembalian=bayar-totalHarga;

sisakembalian=(kembalian%50000);
limapuluhribu=(kembalian-sisakembalian)/50000;
sisakembalian2=(kembalian%20000);
duapuluhribu=(sisakembalian-sisakembalian2)/20000;
sisakembalian3=(kembalian%10000);
sepuluhribu=(sisakembalian-sisakembalian3)/10000;
sisakembalian4=(kembalian%5000);
limaribu=(sisakembalian-sisakembalian4)/5000;
sisakembalian5=(kembalian%2000);
duaribu=(sisakembalian-sisakembalian5)/2000;
sisakembalian6=(kembalian%1000);
seribu=(sisakembalian-sisakembalian6)/1000;
sisakembalian7=(kembalian%500);
limaratus=(sisakembalian-sisakembalian7)/500;

printf("\n Berat Buah \t: %0.1f \n\n",beratBuah);
printf("\n Total Harga \t: %d \n\n",totalHarga);
printf("\n Nilai Bayar \t: %d \n\n",bayar);
printf("\n Kembalian \t: %d \n\n",kembalian);
printf("\n ---------------------------------------------------\n");
printf("\n Jumlah Pecahan 50.000\t : %d \n\n",limapuluhribu);
printf("\n Jumlah Pecahan 20.000\t : %d \n\n",duapuluhribu);
printf("\n Jumlah Pecahan 10.000\t : %d \n\n",sepuluhribu);
printf("\n Jumlah Pecahan 5.000\t : %d \n\n",limaribu);
printf("\n Jumlah Pecahan 2.000\t : %d \n\n",duaribu);
printf("\n Jumlah Pecahan 1.000\t : %d \n\n",seribu);
printf("\n Jumlah Pecahan 500\t : %d \n\n",limaratus);

printf("\n");
system("pause");
}

SOAL NOMER 5
#include<stdio.h>
#include<conio.h>

int main (){
	int jamMasuk, menitMasuk, waktuMasuk, jamKeluar, menitKeluar, waktuKeluar, selisihParkir, biayaParkir;
	point1 :
	printf("---> Waktu Masuk <--- \nJam: ");
	scanf("%d", &jamMasuk);
	printf("Menit : ");
	scanf("%d", &menitMasuk);
	waktuMasuk = (jamMasuk*60) + menitMasuk;
	printf("---> Waktu Keluar <---\nJam :");
	scanf("%d", &jamKeluar);
	printf("Menit : ");
	scanf("%d", &menitKeluar);
	waktuKeluar = (jamKeluar*60) + menitKeluar;
	if(waktuMasuk>waktuKeluar) {
	printf("Waktu Masuk Tidak Bisa Lebih Besar dari Waktu Keluar \n");
	goto point1;}
	
	selisihParkir = ((jamKeluar - jamMasuk)*60) + (menitKeluar - menitMasuk);
	
	//proses
	if(selisihParkir <=60) {
		biayaParkir = 2000;
	}
	else if(selisihParkir>60) {
		biayaParkir = (selisihParkir/60*1000) + 2000;
	}
	else if(selisihParkir<=120) {
		biayaParkir = (selisihParkir/60*1000) + 2000;
	} 
	else if(selisihParkir>120){
		biayaParkir = (selisihParkir/60*1000) + 2000;
	}
	
	//output
	printf("Waktu Parkir anda %d menit dari %d:%d s/d %d:%d \nBiaya Parkir anda adalah : Rp %d", selisihParkir);
}

SOAL NOMER 6
#include<iostream>
#include<conio.h>
#include<windows.h>

using namespace std;
COORD coordinate;
void gotoxy(int x,int y){
	coordinate.X=x; coordinate.Y=y;
	SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE),coordinate);
}
int main(){


gotoxy (5,5);
cout<<"|---------------------------------------------------------------------|\n";

gotoxy (5,6); cout<<"| Categories ";
gotoxy (36,6); cout<<"|Products";

gotoxy (5,7);
cout<<"|---------------------------------------------------------------------|\n";

gotoxy (5,8);  cout<<"|ID";
gotoxy (12,8); cout<<"|Name";
gotoxy (36,8); cout<<"|ID";
gotoxy (50,8); cout<<"|Name";
gotoxy (60,8); cout<<"|Category_id";

gotoxy (5,9);
cout<<"|---------------------------------------------------------------------|\n";

gotoxy (5,10);  cout<<"|1";
gotoxy (12,10); cout<<"|Peralatan Mandi";
gotoxy (36,10); cout<<"|1";
gotoxy (50,10); cout<<"|Sampo";
gotoxy (60,10); cout<<"|1";

gotoxy (5,11);
cout<<"|---------------------------------------------------------------------|\n";

gotoxy (5,12);  cout<<"|2";
gotoxy (12,12); cout<<"|Mie Instan";
gotoxy (36,12); cout<<"|2";
gotoxy (50,12); cout<<"|Sikat Gigi";
gotoxy (60,12); cout<<"|1";

gotoxy (5,13);
cout<<"|---------------------------------------------------------------------|\n";

gotoxy (5,14);  cout<<"|3";
gotoxy (12,14); cout<<"|Olahan Daging";
gotoxy (36,14); cout<<"|3";
gotoxy (50,14); cout<<"|Indomie";
gotoxy (60,14); cout<<"|2";

gotoxy (5,15);
cout<<"|---------------------------------------------------------------------|\n";

gotoxy (36,16); cout<<"|4";
gotoxy (50,16); cout<<"|Mie Sedap";
gotoxy (60,16); cout<<"|2";

gotoxy (36,17);
cout<<"|--------------------------------------|\n";

gotoxy (36,18); cout<<"|5";
gotoxy (50,18); cout<<"|Nuget";
gotoxy (60,18); cout<<"|3";

gotoxy (36,19);
cout<<"|--------------------------------------|\n";
getch();
}

