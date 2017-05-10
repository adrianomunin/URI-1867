#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include <stdlib.h>

void main()
{
	int i, j=0, a, b[250], c=0, k, l=0, x, y[250], z=0;

	scanf("%i", &a);
	scanf("%i", &x);
	
	//---------------------------------------------------------------------------------------------------------------------
	
	for (i = 0; i <= 250; i++) // zerando as posicoes da memoria do primeiro vetor
	{
		b[i] = 0;
	}
	
	i = 0;
	
	//----------------------------------------------------------------------------------------------------------------------
	
	for (k = 0; k <= 250; k++) // zerando as posicoes da memoria do segundo vetor
	{
		y[k] = 0;
	}

	k = 0;

	//----------------------------------------------------------------------------------------------------------------------

	while (a != 0)		// inicio da separacao e contagem do primeiro numero
	{
		b[i] = a % 10;
		a = a / 10;
		i++;
	}

	for (j=0;j<i; j++)
	{
		c = c + b[j];
	}

	printf("%i\n", c); // final da separacao e contagem do primeiro numero
	
	//-----------------------------------------------------------------------------------------------------------------------
	
	while (x != 0)		// inicio da separacao e contagem do segundo numero
	{
		y[k] = x % 10;
		x = x / 10;
		k++;
	}

	for (l = 0;l<k; l++)
	{
		z = z + y[l];
	}

	printf("%i\n", z); // final da separacao e contagem do segundo numero
	//-------------------------------------------------------------------------------------------------------------------------

	if (c > z)
	{
		printf("1\n");
	}
	else
	{
		if (c < z)
		{
			printf("2\n");
		}
		else
		{
			printf("0\n");
		}
	}
	


	system("pause");
}
