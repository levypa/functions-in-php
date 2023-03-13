# Calcular Juros
## Calcular o juro de 13% a cada 12 meses sobre o montante acumulado:

	function calculaJuros($valorInicial, $numAnos) {
	    $percentualJuros = 0.13;
	    $valorAtual = $valorInicial;

	    for ($i = 1; $i <= $numAnos * 12; $i++) {
		if ($i % 12 == 0) {
		   $valorAtual *= (1 + $percentualJuros);
		}

			echo $i, " - ", $valorAtual, "<br>";
	    }

	    return $valorAtual;
	}

	calculaJuros(1000, 2);
