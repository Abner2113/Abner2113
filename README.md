Algoritmo sin_titulo
	Definir base, altura, lado, base_superior, base_inferior Como Real;
	Definir area, perimetro, apotema, angulo Como Real;
	Definir ti, radio Como Real;
	Definir npoli Como Real;
	Definir numero_lados, resp Como Entero;
	ti=3.14;
	
	Escribir "========================================================================================================";
	Escribir "si tu figura es un circulo pon (0)";
	Escribir "si tu figura es un triangulo pon (1)";
	Escribir "si tu figura es un cuadrado pon (2)";
	Escribir "si tu figura es un polinomio pon (3)";
	Leer resp;
	Escribir "========================================================================================================";
	
	si resp>3 Entonces
		Escribir "tu figura no esta en el menu";
	FinSi
	si resp<0 Entonces
		Escribir "no puedes introducir numeros negativos";
	FinSi
	//Area del circulo
	si resp=0 Entonces
		Escribir "su figura es un circulo";
		Escribir "ingresa el radio del circulo";
		leer radio;
		area=ti*radio^2;
		Escribir "========================================================================================================";
		Escribir "el area de la figura es de: ", area "m^2";
		Escribir "========================================================================================================";
	FinSi
	//Area del triangulo
	si resp=1 Entonces
		Escribir "tu figura es un tringulo";
		Escribir "preciona (1) si es un equilatero (2) si es un isoseles (3) si es un escaleno";
		leer resp;
		Escribir "========================================================================================================";
		si resp=1 | resp=2 | resp=3 Entonces
			Escribir "ingresa base";
			Leer base;
			Escribir "ingrese la altura";
			leer altura;
			area=base*altura/2;
			Escribir "el area de la figura es de: ", area "m^2";
			Escribir "========================================================================================================";
		FinSi
	FinSi
	//Area del cuadrado
	si resp=2 Entonces
		Escribir "tu figura es un cuadrado";
		Escribir "preciona (1) si es un cuadrado (2) si es un rectangulo (3) si es paralelogramo (4) si es un rombo (5) si es un trapecio";
		Leer resp;
		Escribir "========================================================================================================";
		si resp=1 Entonces
			Escribir "ingresa uno de los lados";
			Leer lado;
			area=lado*lado;
			Escribir "el area de la figura es de: ", area "m^2";
			Escribir "========================================================================================================";
		SiNo
			si resp=2 | resp=3 Entonces
				Escribir "ingresa base";
				Leer base;
				Escribir "ingrese la altura";
				leer altura;
				area=base*altura;
				Escribir "el area de la figura es de: ", area "m^2";
				Escribir "========================================================================================================";
			sino
				si resp=4 Entonces
					Escribir "ingresa la diagonal mayor";
					leer base_superior;
					Escribir "ingresa la diagonal menor";
					leer base_inferior;
					area=base_superior*base_inferior/2;
					Escribir "el area de la figura es de: ", area "m^2";
					Escribir "========================================================================================================";
				SiNo
					si resp=5 Entonces
						Escribir "ingresa la base mayor";
						leer base_superior;
						Escribir "ingresa la base menor";
						leer base_inferior;
						Escribir "ingresa la altura";
						leer altura;
						area=(base_superior+base_inferior)*altura;
						Escribir "el area de la figura es de: ", area "m^2";
						Escribir "========================================================================================================";
					FinSi
				FinSi
			FinSi
		FinSi
	FinSi
	//Aream del poligono
	si resp=3 Entonces
		Escribir "su fiugura es un poligono";
		Escribir "ingresa el numero de lados que tiene su poligono";
		leer lado;
		Escribir "========================================================================================================";
		si lado>=3 Entonces
			Escribir "ingresa la medida de un lado del poligono";
			leer npoli;
			perimetro=lado*npoli;
			angulo=360/(2*lado);
			apotema=npoli/2*tan(angulo);
			area=perimetro*apotema/2;
			Escribir "el area de la figura es de: ", area "m^2";
			Escribir "========================================================================================================";
		FinSi
	FinSi
FinAlgoritmo
