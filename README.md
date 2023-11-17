//# matris
#include <stdio.h>

    int matris_kontrol(int matris[][100], int sutun){
        int satir= sutun;

        for(int i=0;i<sutun;i++){
            for(int j=0;j<satir;j++){

                if(matris[i][j]==matris[j][i]){
                    printf("matris karedir!!\n");
                    return -1;

                }
            }
        }
    }

int main(){
 
   int matris[100][100];
   int satir;
   int sutun;
   printf("matrisin satir sayisini giriniz :\n");
   scanf("%d " ,&satir);

   printf("matrisinizin karakterlerini giriniz:\n");
    for(int i=0;i<satir;i++){
        for(int j=0;j<satir;j++){
            printf("matris[%d][%d]",i,j);
            scanf("%d",&matris[i][j]);
        }
   }

int sonuc=matris_kontrol(matris,satir);

    if(sonuc==-1){
        printf("matrisimiz karedir!\n");
    }
    else {
        printf("matrisimiz kare degildir!\n");
    }



    return(0);
}
