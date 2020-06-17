# Bubble-Short
Definition of Bubble Short 

#include <stdio.h>
#include <string.h>
#include <time.h>



int main(){

//10 elemanlı bir diziyi siralama.

int array[10]; // 10 elemanlı dizi tanımlaması.

srand(time(NULL)); // her çalışmada random değer vermesi için tanımlama.

int i = 0; // döngü için değişken.

printf("Rastgele atanan dizi su sekildedir:\n\n");


// diziye rastgele değer atamak için for döngüsü başlangıcı.
for(; i <= 10; i ++){

    if(i < 10)

         array[i] = rand() % 500; // dizinin 1-10 değer aralıklarına max. 500 değerler atama işlemi.

    else if (i = 10) // i'nin 10'a eşit olması durumunda 
    {                // Dizi'yi ekrana yazma komutu.
        int j = 0;

            for(; j < 10; j ++){ 

             printf("%d ",array[j]);

            }
    }
    
  } // Diziye eleman atayan ve dizi elemanlarını gösteren döngünün sonu.

printf("\n\n-----------\n\n");




int temporary , j , showArray; // döngü için gerekli tanımlamalar.


printf("Bubble Sort algoritmasinin asamalari su sekildedir: \n\n");
//Bubble Sort döngüsü.
for(i = 1; i < 10; i ++){

    for(j = 0; j < 10 - i; j ++)
   
         if(array[j] > array[j+1]){

             //Dizilerin yerini değiştirmek için geçici olarak birisinin değerini tutan değişken.
             temporary= array[j+1]; 

            //Dizinin büyük elemanı sağa kaydırılıyor.
             array[j+1] = array[j];
            
            //Dizinin küçük elemanı sola kaydırılıyor.
             array[j] = temporary;
            
            //DİZİ ELEMANLARI YER DEĞİŞTİRDİ.   

         }

                //Bubble Sort'u adım adım gösteren döngü.
                for(showArray = 0; showArray < 10; showArray ++){ 

                    printf("%d ",array[showArray]);
                } //Bubble Sort'u adım adım gösteren döngünün sonu.

                printf("\n\n----------\n\n");
    
}


printf("Dizinin siralanmis hali su sekildedir: \n\n");

//Sıralanan diziyi gösteren döngü.
    for(j = 0; j < 10; j ++){

         printf("%d ",array[j]);
    }

    return 0;
}


