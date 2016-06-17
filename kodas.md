#include <stdio.h>
main()
{

	int pir_trej, ant_trej; // pirmieji trys skaitmenys ir antrieji
	int sum, sum2;    // sumos pirmuju ir antruju
	int i;
	int sk1, sk2, sk3, sk4, sk5, sk6; // skaitmenys
	for (i = 100000; i <= 999999; i++)
		// ciklo pradzia
	{
	pir_trej =i / 1000;	// atskiriame pirmus trys skaicius
	sk1= pir_trej / 100;   // - pirmas skaicius
	sk2= pir_trej /10 % 10; //- antras skaicius
	sk3= pir_trej % 10 ;   // - trecias skaicius
	// pagrindine formule

	// ******************************
	ant_trej = i % 1000; // atskiriame paskutinius trys skaicius
	sk4= ant_trej / 100;   // - pirmas skaicius
	sk5= ant_trej /10 % 10; //- antras skaicius
	sk6= ant_trej % 10 ;   // - trecias skaicius
	// tikriname, kad nebutu panasus skaitmenys, patikrinus sudedame skaitmenys i suma ir sulyginame ja
	// pradzia
	if ((sk1 != sk2) & (sk1 != sk3) &(sk1 != sk4) & (sk1 != sk5) & (sk1 != sk6) &
		 (sk2 != sk3) & (sk2 != sk4) & (sk2 != sk5) & (sk2 != sk6) &
		 (sk3 != sk4) & (sk3 != sk5) & (sk3 != sk6) &
		 (sk4 != sk5) & (sk4 != sk6) &
		 (sk5 != sk6))
	{
	sum = sk1+sk2+sk3;
	sum2 = sk4 + sk5 + sk6;
	if (sum == sum2) printf("%d ", i); // isvedame i ekrana laimingus biletus.
	}
	// pabaiga
	}
	return 0;
	// ciklo pabaiga
}
