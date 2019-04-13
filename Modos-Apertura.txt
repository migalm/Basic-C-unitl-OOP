#include <iostream>
#include <fstream>
using namespace std;

int main(){
    /***** MODOS DE APERTURA *****/
    /**
        ios:: in   -> modo lectura (entrada)
        ios:: out  -> modo escritura (salida)
        ios::binary-> modo binario
        ios::ate   -> La posicion inicial al final del archivo (AT the End -> al final)
        ios::app   -> Las operaciones se realizan siempre al final del archivo
        ios::trunc -> si el archivo existe, se elimina su contenido para escritura
     **/
    ofstream salida;
    salida.open("archivo.txt",ios::app);
    salida<<"Linea 7"<<endl;
    salida<<"Linea 8"<<endl;
    salida<<"Linea 9"<<endl;
    salida.close();
    return 0;
}
