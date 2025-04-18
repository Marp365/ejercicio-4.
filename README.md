#include <iostream>
using namespace std;

int main() {
    int numeros[20];

    for (int i = 0; i < 20; i++) {
        cout << "Ingrese el número " << i + 1 << ": ";
        cin >> numeros[i];
    }

    for (int i = 0; i < 20; i++) {
        bool yaContado = false;

        for (int j = 0; j < i; j++) {
            if (numeros[i] == numeros[j]) {
                yaContado = true;
                break;
            }
        }

        if (!yaContado) {
            int frecuencia = 1;
            for (int j = i + 1; j < 20; j++) {
                if (numeros[i] == numeros[j]) {
                    frecuencia++;
                }
            }
            cout << "El número " << numeros[i] << " aparece " << frecuencia << " veces." << endl;
        }
    }

    return 0;
}
