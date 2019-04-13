#include <iostream>
#include <fstream>
using namespace std;

struct Persona{
    char nombre[8];
    int edad;
};

int main(){
    /***** ARCHIVOS BINARIOS ******/
    ofstream salida;
    salida.open("data.bin",ios::binary);
    /**
        EL PROCESO DE ESCRITURA ES
            DESDE MEMORIA --> AL ARCHIVO
                (es byte por byte)
                1.- Desde que punto de la memoria empezaré el traspaso
                2.- Cuantos bytes voy a pasar
    **/
    /****
        1er parametro.-Un puntero de tipo char  que guarde el byte de inicio del registro
        2do parametro.- Cuantos bytes voy a pasar
    ****/
    Persona p = {"Gian",23};
    salida.write((char*)&p,sizeof(Persona));
    salida.write((char*)&p,sizeof(Persona));
    salida.close();
    return 0;
}
