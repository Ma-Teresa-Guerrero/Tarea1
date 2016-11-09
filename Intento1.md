#include <iostream>
#include <string>
using namespace std;
/* run this program using the console pauser or add your own getch, system("pause") or input loop */

class bus {
	
	protected:
		string origen;
		string destino;
		string hora;
		int santiago_bus[5];
		int rancagua_bus[5];
		int valparaiso_bus[5];
		int laserena_bus[5];
	public:
		bus (string origen1, string destino1, string hora1){
			
			origen = origen1;
			destino = destino1;
			hora = hora1;
			santiago_bus[0] = {0};
			santiago_bus[1] = {0};
			santiago_bus[2] = {0};
			santiago_bus[3] = {0};
			santiago_bus[4] = {0};
			santiago_bus[5] = {0};
			rancagua_bus[0] = {0};
			rancagua_bus[1] = {0};
			rancagua_bus[2] = {0};
			rancagua_bus[3] = {0};
			rancagua_bus[4] = {0};
			rancagua_bus[5] = {0};
			valparaiso_bus[0] = {0};
			valparaiso_bus[1] = {0};
			valparaiso_bus[2] = {0};
			valparaiso_bus[3] = {0};
			valparaiso_bus[4] = {0};
			valparaiso_bus[5] = {0};
			laserena_bus[0] = {0};
			laserena_bus[1] = {0};
			laserena_bus[2] = {0};
			laserena_bus[3] = {0};
			laserena_bus[4] = {0};
			laserena_bus[5] = {0};
		}
		
};

class semicama : public bus {
	private:
		string tipo;
		string asientos[45];
		int precio;
	public:
		semicama() : bus(origen, destino, hora){	
			tipo = "semicama";
			for (int i=0; i<45; i++){
				asientos[i] = 0;
			}
		}
		void listarAsientos1(){
			
			int n=0;
			if (origen == "santiago"){
				if (santiago_bus[0] == 0){
					cout << "Informacion de los asientos del 1er bus semi-cama de Santiago:" << endl;
					for (int i=0; i<45; i++){
						
						if (asientos[i] == 0){	
							n = n+1;
							if (45-n == 0){
								santiago_bus[0] == 1;
							}
						}
						else {
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
							if (santiago_bus[0] == 1){
								cout << "El 1er. bus semi-cama de Santiago se encuentra lleno." << endl;
								if (santiago_bus[1] == 1){
									cout << "Todos los buses de Santiago se encuentras ocupados, intente mas tarde." << endl;
								}
								else if (santiago_bus[1] == 0){
									cout << "El 2do bus de Santiago aun posee cupos." << endl;
								}
							}
							else if(santiago_bus[0] == 0){
								cout << "El 1er. bus semi-cama de Santiago aun conserva cupos." << endl;
							}
						}
					}
					cout << "Hay " << n << " asientos disponibles." << endl;
				}
				else if (santiago_bus[0] == 1){
					cout << "Informacion de los asientos del 1er bus semi-cama de Santiago:" << endl;
					for (int i=0; i<45; i++){
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
					}
					cout << "El 1er bus semi-cama de Santiago no posee cupos." << endl;
				}
			}
			else if (origen == "rancagua"){
				if (rancagua_bus[0] == 0){
					cout << "Informacion de los asientos del 1er bus semi-cama de Rancagua:" << endl;
					for (int i=0; i<45; i++){
						
						if (asientos[i] == 0){	
							n = n+1;
							if (45-n == 0){
								rancagua_bus[0] == 1;
							}
						}
						else {
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
							if (rancagua_bus[0] == 1){
								cout << "El 1er. bus semi-cama de Rancagua se encuentra lleno." << endl;
								if (rancagua_bus[1] == 1){
									cout << "Todos los buses de Rancagua se encuentras ocupados, intente mas tarde." << endl;
								}
								else if (rancagua_bus[1] == 0){
									cout << "El 2do bus de Rancagua aun posee cupos." << endl;
								}
							}
							else if(rancagua_bus[0] == 0){
								cout << "El 1er. bus semi-cama de Rancagua aun conserva cupos." << endl;
							}
						}
					}
					cout << "Hay " << n << " asientos disponibles." << endl;
				}
				else if (rancagua_bus[0] == 1){
					cout << "Informacion de los asientos del 1er bus semi-cama de Rancagua:" << endl;
					for (int i=0; i<45; i++){
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
					}
					cout << "El 1er bus semi-cama de Rancagua no posee cupos." << endl;
				}
			}
			else if (origen == "valparaiso"){
				if (valparaiso_bus[0] == 0){
					cout << "Informacion de los asientos del 1er bus semi-cama de valparaiso:" << endl;
					for (int i=0; i<45; i++){
						
						if (asientos[i] == 0){	
							n = n+1;
							if (45-n == 0){
								valparaiso_bus[0] == 1;
							}
						}
						else {
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
							if (valparaiso_bus[0] == 1){
								cout << "El 1er. bus semi-cama de Valparaiso se encuentra lleno." << endl;
								if (valparaiso_bus[1] == 1){
									cout << "Todos los buses de Valparaiso se encuentran ocupados, intente mas tarde." << endl;
								}
								else if (valparaiso_bus[1] == 0){
									cout << "El 2do bus de Valparaiso aun posee cupos." << endl;
								}
							}
							else if(valparaiso_bus[0] == 0){
								cout << "El 1er. bus semi-cama de Valparaiso aun conserva cupos." << endl;
							}
						}
					}
					cout << "Hay " << n << " asientos disponibles." << endl;
				}
				else if (valparaiso_bus[0] == 1){
					cout << "Informacion de los asientos del 1er bus semi-cama de Santiago:" << endl;
					for (int i=0; i<45; i++){
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
					}
					cout << "El 1er bus semi-cama de santiago no posee cupos." << endl;
				}
			}
			else if (origen == "laserena"){
				if (laserena_bus[0] == 0){
					cout << "Informacion de los asientos del 1er bus salon-cama de La Serena:" << endl;
					for (int i=0; i<45; i++){
						
						if (asientos[i] == 0){	
							n = n+1;
							if (45-n == 0){
								laserena_bus[0] == 1;
							}
						}
						else {
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
							if (laserena_bus[0] == 1){
								cout << "El 1er. bus semi-cama de La Serena se encuentra lleno." << endl;
								if (laserena_bus[1] == 1){
									cout << "Todos los buses de La Serena se encuentras ocupados, intente mas tarde." << endl;
								}
								else if (laserena_bus[1] == 0){
									cout << "El 2do bus de La Serena aun posee cupos." << endl;
								}
							}
							else if(laserena_bus[0] == 0){
								cout << "El 1er. bus semi-cama de La Serena aun conserva cupos." << endl;
							}
						}
					}
					cout << "Hay " << n << " asientos disponibles." << endl;
				}
				else if (laserena_bus[0] == 1){
					cout << "Informacion de los asientos del 1er bus semi-cama de La Serena:" << endl;
					for (int i=0; i<45; i++){
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
					}
					cout << "El 1er bus semi-cama de La Serena no posee cupos." << endl;
				}
			}
		}
		bool venderAsiento1(int asiento2, string rut){    //le puse el 2 al nombre para no confundirlo con "asientos"
			
			int puesto = asiento2;
			if (asientos[puesto] == 0){
				asientos[puesto] = rut;
				return true;
			}
			else {
				return false;
			}
		}
		int asignarPrecio1(){
			
			if (origen == "rancagua"){
				if(destino == "santiago"){
					precio = 4000;
				}
				else if(destino == "valparaiso"){
					precio = 6000;
				}
				else if(destino == "laserena"){
					precio = 9000;
				}
			}
			else if (origen == "santiago"){
				if(destino == "rancagua"){
					precio = 4000;
				}
				else if(destino == "valparaiso"){
					precio = 2000;
				}
				else if(destino == "laserena"){
					precio = 7000;
				}
			}
			else if (origen == "valparaiso"){
				if(destino == "santiago"){
					precio = 2000;
				}
				else if(destino == "rancagua"){
					precio = 6000;
				}
				else if(destino == "laserena"){
					precio = 5000;
				}
			}
			else if (origen == "laserena"){
				if(destino == "santiago"){
					precio = 7000;
				}
				else if(destino == "rancagua"){
					precio = 9000;
				}
				else if(destino == "valparaiso"){
					precio = 5000;
				}
			}
			return precio;
		}
		void info1(){
			cout << "Usted ira desde " << origen << " hasta " << destino << " en un bus " << tipo << " a las " << hora << " hrs. por $" << precio << endl;
		}
};

class saloncama : public bus {
	private:
		string tipo;
		int asientos[30];
		int precio;
	public:
		saloncama() : bus(origen, destino, hora){
			
			tipo = "saloncama";
			for (int i=0; i<30; i++){
				asientos[i] = 0;
			}
		}
		void listarAsientos2(){
			
			int n;
			if (origen == "santiago"){
				if (santiago_bus[2] == 0){
					cout << "Informacion de los asientos del 1er bus salon-cama de Santiago:" << endl;
					for (int i=0; i<45; i++){
						
						if (asientos[i] == 0){	
							n = n+1;
							if (45-n == 0){
								santiago_bus[2] == 1;
							}
						}
						else {
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
							if (santiago_bus[2] == 1){
								cout << "El 1er. bus salon-cama de Santiago se encuentra lleno." << endl;
								if (santiago_bus[3] == 1){
									cout << "Todos los buses de Santiago se encuentras ocupados, intente mas tarde." << endl;
								}
								else if (santiago_bus[3] == 0){
									cout << "El 2do bus de Santiago aun posee cupos." << endl;
								}
							}
							else if(santiago_bus[2] == 0){
								cout << "El 1er. bus salon-cama de Santiago aun conserva cupos." << endl;
							}
						}
					}
					cout << "Hay " << n << " asientos disponibles." << endl;
				}
				else if (santiago_bus[2] == 1){
					cout << "Informacion de los asientos del 1er bus salon-cama de Santiago:" << endl;
					for (int i=0; i<45; i++){
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
					}
					cout << "El 1er bus salon-cama de santiago no posee cupos." << endl;
				}
			}
			else if (origen == "rancagua"){
				if (rancagua_bus[2] == 0){
					cout << "Informacion de los asientos del 1er bus salon-cama de Rancagua:" << endl;
					for (int i=0; i<45; i++){
						
						if (asientos[i] == 0){	
							n = n+1;
							if (45-n == 0){
								rancagua_bus[2] == 1;
							}
						}
						else {
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
							if (rancagua_bus[2] == 1){
								cout << "El 1er. bus salon-cama de Rancagua se encuentra lleno." << endl;
								if (rancagua_bus[3] == 1){
									cout << "Todos los buses de Rancagua se encuentras ocupados, intente mas tarde." << endl;
								}
								else if (rancagua_bus[3] == 0){
									cout << "El 2do bus de Rancagua aun posee cupos." << endl;
								}
							}
							else if(rancagua_bus[2] == 0){
								cout << "El 1er. bus salon-cama de Rancagua aun conserva cupos." << endl;
							}
						}
					}
					cout << "Hay " << n << " asientos disponibles." << endl;
				}
				else if (rancagua_bus[2] == 1){
					cout << "Informacion de los asientos del 1er bus salon-cama de Rancagua:" << endl;
					for (int i=0; i<45; i++){
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
					}
					cout << "El 1er bus salon-cama de Rancagua no posee cupos." << endl;
				}
			}
			else if (origen == "valparaiso"){
				if (valparaiso_bus[2] == 0){
					cout << "Informacion de los asientos del 1er bus salon-cama de valparaiso:" << endl;
					for (int i=0; i<45; i++){
						
						if (asientos[i] == 0){	
							n = n+1;
							if (45-n == 0){
								valparaiso_bus[2] == 1;
							}
						}
						else {
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
							if (valparaiso_bus[2] == 1){
								cout << "El 1er. bus salon-cama de Valparaiso se encuentra lleno." << endl;
								if (valparaiso_bus[3] == 1){
									cout << "Todos los buses de Valparaiso se encuentras ocupados, intente mas tarde." << endl;
								}
								else if (valparaiso_bus[3] == 0){
									cout << "El 2do bus de Valparaiso aun posee cupos." << endl;
								}
							}
							else if(valparaiso_bus[2] == 0){
								cout << "El 1er. bus salon-cama de Valparaiso aun conserva cupos." << endl;
							}
						}
					}
					cout << "Hay " << n << " asientos disponibles." << endl;
				}
				else if (valparaiso_bus[2] == 1){
					cout << "Informacion de los asientos del 1er bus salon-cama de Santiago:" << endl;
					for (int i=0; i<45; i++){
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
					}
					cout << "El 1er bus salon-cama de santiago no posee cupos." << endl;
				}
			}
			else if (origen == "laserena"){
				if (laserena_bus[2] == 0){
					cout << "Informacion de los asientos del 1er bus salon-cama de La Serena:" << endl;
					for (int i=0; i<45; i++){
						
						if (asientos[i] == 0){	
							n = n+1;
							if (45-n == 0){
								laserena_bus[2] == 1;
							}
						}
						else {
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
							if (laserena_bus[2] == 1){
								cout << "El 1er. bus salon-cama de La Serena se encuentra lleno." << endl;
								if (laserena_bus[3] == 1){
									cout << "Todos los buses de La Serena se encuentras ocupados, intente mas tarde." << endl;
								}
								else if (laserena_bus[3] == 0){
									cout << "El 2do bus de La Serena aun posee cupos." << endl;
								}
							}
							else if(laserena_bus[2] == 0){
								cout << "El 1er. bus salon-cama de La Serena aun conserva cupos." << endl;
							}
						}
					}
					cout << "Hay " << n << " asientos disponibles." << endl;
				}
				else if (laserena_bus[2] == 1){
					cout << "Informacion de los asientos del 1er bus salon-cama de La Serena:" << endl;
					for (int i=0; i<45; i++){
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
					}
					cout << "El 1er bus salon-cama de La Serena no posee cupos." << endl;
				}
			}
		}
		bool venderAsiento2(int asiento2, string rut){    //le puse el 2 al nombre para no confundirlo con "asientos"
			
			int puesto = asiento2;
			if (asientos[puesto] == 0){
				asientos[puesto] = rut;
				return true;
			}
			else {
				return false;
			}
		}
		int asignarPrecio2(){
			
			if (origen == "rancagua"){
				if(destino == "santiago"){
					precio = 8000;
				}
				else if(destino == "valparaiso"){
					precio = 8000;
				}
				else if(destino == "laserena"){
					precio = 14000;
				}
			}
			else if (origen == "santiago"){
				if(destino == "rancagua"){
					precio = 8000;
				}
				else if(destino == "valparaiso"){
					precio = 4000;
				}
				else if(destino == "laserena"){
					precio = 10000;
				}
			}
			else if (origen == "valparaiso"){
				if(destino == "santiago"){
					precio = 4000;
				}
				else if(destino == "rancagua"){
					precio = 8000;
				}
				else if(destino == "laserena"){
					precio = 8000;
				}
			}
			else if (origen == "laserena"){
				if(destino == "santiago"){
					precio = 10000;
				}
				else if(destino == "rancagua"){
					precio = 14000;
				}
				else if(destino == "valparaiso"){
					precio = 8000;
				}
			}
			return precio;
		}
		void info2(){
			cout << "Usted ira desde " << origen << " hasta " << destino << " en un bus " << tipo << " a las " << hora << " hrs. por $" << precio << endl;
		}
};

class premium : public bus {
	private:
		string tipo;
		int asientos[20];
		int precio;
	public:
		semicama() : bus(origen, destino, hora){
			
			tipo = "premium";
			for (int i=0; i<20; i++){
				asientos[i] = 0;
			}
		}
		void listarAsientos3(){
			
			int n;
			if (origen == "santiago"){
				if (santiago_bus[4] == 0){
					cout << "Informacion de los asientos del 1er bus premium de Santiago:" << endl;
					for (int i=0; i<45; i++){
						
						if (asientos[i] == 0){	
							n = n+1;
							if (45-n == 0){
								santiago_bus[4] == 1;
							}
						}
						else {
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
							if (santiago_bus[4] == 1){
								cout << "El 1er. bus premium de Santiago se encuentra lleno." << endl;
								if (santiago_bus[5] == 1){
									cout << "Todos los buses de Santiago se encuentras ocupados, intente mas tarde." << endl;
								}
								else if (santiago_bus[5] == 0){
									cout << "El 2do bus de Santiago aun posee cupos." << endl;
								}
							}
							else if(santiago_bus[4] == 0){
								cout << "El 1er. bus premium de Santiago aun conserva cupos." << endl;
							}
						}
					}
					cout << "Hay " << n << " asientos disponibles." << endl;
				}
				else if (santiago_bus[4] == 1){
					cout << "Informacion de los asientos del 1er bus premium de Santiago:" << endl;
					for (int i=0; i<45; i++){
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
					}
					cout << "El 1er bus premium de Santiago no posee cupos." << endl;
				}
			}
			else if (origen == "rancagua"){
				if (rancagua_bus[4] == 0){
					cout << "Informacion de los asientos del 1er bus premium de Rancagua:" << endl;
					for (int i=0; i<45; i++){
						
						if (asientos[i] == 0){	
							n = n+1;
							if (45-n == 0){
								rancagua_bus[4] == 1;
							}
						}
						else {
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
							if (rancagua_bus[4] == 1){
								cout << "El 1er. bus premium de Rancagua se encuentra lleno." << endl;
								if (rancagua_bus[5] == 1){
									cout << "Todos los buses de Rancagua se encuentras ocupados, intente mas tarde." << endl;
								}
								else if (rancagua_bus[5] == 0){
									cout << "El 2do bus de Rancagua aun posee cupos." << endl;
								}
							}
							else if(rancagua_bus[4] == 0){
								cout << "El 1er. bus premium de Rancagua aun conserva cupos." << endl;
							}
						}
					}
					cout << "Hay " << n << " asientos disponibles." << endl;
				}
				else if (rancagua_bus[4] == 1){
					cout << "Informacion de los asientos del 1er bus premium de Rancagua:" << endl;
					for (int i=0; i<45; i++){
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
					}
					cout << "El 1er bus premium de Rancagua no posee cupos." << endl;
				}
			}
			else if (origen == "valparaiso"){
				if (valparaiso_bus[4] == 0){
					cout << "Informacion de los asientos del 1er bus premium de valparaiso:" << endl;
					for (int i=0; i<45; i++){
						
						if (asientos[i] == 0){	
							n = n+1;
							if (45-n == 0){
								valparaiso_bus[4] == 1;
							}
						}
						else {
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
							if (valparaiso_bus[4] == 1){
								cout << "El 1er. bus premium de Valparaiso se encuentra lleno." << endl;
								if (valparaiso_bus[5] == 1){
									cout << "Todos los buses de Valparaiso se encuentras ocupados, intente mas tarde." << endl;
								}
								else if (valparaiso_bus[5] == 0){
									cout << "El 2do bus de Valparaiso aun posee cupos." << endl;
								}
							}
							else if(valparaiso_bus[4] == 0){
								cout << "El 1er. bus premium de Valparaiso aun conserva cupos." << endl;
							}
						}
					}
					cout << "Hay " << n << " asientos disponibles." << endl;
				}
				else if (valparaiso_bus[4] == 1){
					cout << "Informacion de los asientos del 1er bus premium de Santiago:" << endl;
					for (int i=0; i<45; i++){
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
					}
					cout << "El 1er bus premium de santiago no posee cupos." << endl;
				}
			}
			else if (origen == "laserena"){
				if (laserena_bus[4] == 0){
					cout << "Informacion de los asientos del 1er bus premium de La Serena:" << endl;
					for (int i=0; i<45; i++){
						
						if (asientos[i] == 0){	
							n = n+1;
							if (45-n == 0){
								laserena_bus[4] == 1;
							}
						}
						else {
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
							if (laserena_bus[4] == 1){
								cout << "El 1er. bus premium de La Serena se encuentra lleno." << endl;
								if (laserena_bus[5] == 1){
									cout << "Todos los buses de La Serena se encuentras ocupados, intente mas tarde." << endl;
								}
								else if (laserena_bus[5] == 0){
									cout << "El 2do bus de La Serena aun posee cupos." << endl;
								}
							}
							else if(laserena_bus[4] == 0){
								cout << "El 1er. bus premium de La Serena aun conserva cupos." << endl;
							}
						}
					}
					cout << "Hay " << n << " asientos disponibles." << endl;
				}
				else if (laserena_bus[4] == 1){
					cout << "Informacion de los asientos del 1er bus premium de La Serena:" << endl;
					for (int i=0; i<45; i++){
							cout << "El asiento " << i << " esta vendido al pasajero con rut " << asientos[i] << endl;
					}
					cout << "El 1er bus premium de La Serena no posee cupos." << endl;
				}
			}
		}
		bool venderAsiento3(int asiento2, string rut){    //le puse el 2 al nombre para no confundirlo con "asientos"
			
			int puesto = asiento2;
			if (asientos[puesto] == 0){
				asientos[puesto] = rut;
				return true;
			}
			else {
				return false;
			}
		}
		int asignarPrecio3(){
			
			if (origen == "rancagua"){
				if(destino == "santiago"){
					precio = 12000;
				}
				else if(destino == "valparaiso"){
					precio = 10000;
				}
				else if(destino == "laserena"){
					precio = 19000;
				}
			}
			else if (origen == "santiago"){
				if(destino == "rancagua"){
					precio = 12000;
				}
				else if(destino == "valparaiso"){
					precio = 6000;
				}
				else if(destino == "laserena"){
					precio = 13000;
				}
			}
			else if (origen == "valparaiso"){
				if(destino == "santiago"){
					precio = 6000;
				}
				else if(destino == "rancagua"){
					precio = 10000;
				}
				else if(destino == "laserena"){
					precio = 11000;
				}
			}
			else if (origen == "laserena"){
				if(destino == "santiago"){
					precio = 13000;
				}
				else if(destino == "rancagua"){
					precio = 19000;
				}
				else if(destino == "valparaiso"){
					precio = 11000;
				}
			}
			return precio;
		}
		void info3(){
			cout << "Usted ira desde " << origen << " hasta " << destino << " en un bus " << tipo << " a las " << hora << " por un precio de $" << precio << endl;
		}
};


int main(int argc, char** argv) {
	
	int santiago_bus[5] = {0};
	int rancagua_bus[5] = {0};
	int valparaiso_bus[5] = {0};
	int laserena_bus[5] = {0};
	string rut1;
	string tipo1;
	string origen1[4] = {"santiago", "rancagua", "valparaiso", "la serena"};
	string destino1[4] = {"santiago", "rancagua", "valparaiso", "la serena"};
	string origen2;
	string destino2;
	int precio1;
	int hora1;
	int asiento2;
	
	cout << "Ingrese:" << endl << "Tipo:  ";
	cin >> tipo1;
	cout << endl << "Rut:  ";
	cin >> rut1;
	while (origen2 == destino2){  //no se puede comprar un boleto si el destino y el origen son iguales
		cout << endl << "Origen:  ";
		cin >> origen2;
		cout << endl << "Destino:  ";
		cin >> destino2;
		cout << endl << 
	}
	cout << endl << "Hora:  ";
	cin >> hora1;
	cout << endl << endl;
	bus a(origen2, destino2, hora1);
	if (tipo1 == "semicama"){
		
		cout << "Ingrese el asiento que desea:  ";
		cin >> asiento2;
		cout << endl << "Ingrese su rut:  ";
		cin >> rut1;
		cout << endl << endl;
		a.listarAsientos1();
		a.venderAsiento1(asiento2, rut1);
		a.asignarPrecio1();
		a.info1();
	}
	else if (tipo1 == "saloncama"){
		
		cout << "Ingrese el asiento que desea:  ";
		cin >> asiento2;
		cout << endl << "Ingrese su rut:  ";
		cin >> rut1;
		cout << endl << endl;
		a.listarAsientos2();
		a.venderAsiento2(asiento2, rut1);
		a.asignarPrecio2();
		a.info2();
	}
	else if (tipo1 == "premium"){
		
		cout << "Ingrese el asiento que desea:  ";
		cin >> asiento2;
		cout << endl << "Ingrese su rut:  ";
		cin >> rut1;
		cout << endl << endl;
		a.listarAsientos3();
		a.venderAsiento3(asiento2, rut1);
		a.asignarPrecio3();
		a.info3();
	}

	system("pause");
	return 0;
}
