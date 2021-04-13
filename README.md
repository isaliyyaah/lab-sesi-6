# lab-sesi-6
package com.company;

public class Main
{
    public static void main(String[] args)
    {
        int Mahasiswa = 8, Jawaban = 10;
        char[][] jwbn = {
                {'A','B','A','C','C','D','E','E','A','D'},
                {'D','B','A','B','C','A','E','E','A','D'},
                {'E','D','D','A','C','B','E','E','A','D'},
                {'C','B','A','E','D','C','E','E','A','D'},
                {'A','B','D','C','C','D','E','E','A','D'},
                {'B','B','E','C','C','D','E','E','A','D'},
                {'B','B','A','C','C','D','E','E','A','D'},
                {'E','B','E','C','C','D','E','E','A','D'}
        };

        char[] Kunci = {'D','B','D','C','C','D','A','E','A','D'};
        int[] Hasil = new int[Mahasiswa];

        for(int i=0; i < Mahasiswa; ++i) {
            int benar = 0;
            for(int x=0; x < Jawaban; ++x) {
                if(jwbn[i][x] == Kunci[x]) {
                    benar++;
                }
            }
            Hasil[i] = benar;
        }

        System.out.println("jumlah jawaban benar masing-masing mahasiswa: \n");
        for(int i=0; i<Mahasiswa; ++i) {
            System.out.println("Mhs " + i + " jumlah jawaban benar adalah " + Hasil[i]);
        }
    }
}
