# quiz3

import std.stdio;

void main(){
    int[] n = [635, 97, 346, 441, 46, 248, 726, 303, 153, 481, 521, 579, 387, 674, 785, 836, 193];
    int[] indeks = [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17];
    ulong c = n.length;

    int h=0;
    while (h<c){
        int i=0;
        while (i<c-1){
            if (n[i]>n[i+1]){
                int k=n[i];
                n[i]=n[i+1];
                n[i+1]=k;
                int l=indeks[i];
                indeks[i]=indeks[i+1];
                indeks[i+1]=l;
            }
            i++;
        }
        h++;
    }

    int i=0;
    while (i<c){
        write(indeks[i],' ');
        i++;
    }
}
