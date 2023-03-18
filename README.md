# Pilha
## Imprimir o último valor da pilha que seja diferente de zero
	function imprimirUltimoValorDiferenteDeZero($pilha) {
	    $stack = new SplStack();
	    foreach ($pilha as $valor) {
		$stack->push($valor);
	    }
	    $ultimo_valor = 0; // Define um valor padrão para o último valor
	    while (!$stack->isEmpty()) {
		$valor_atual = $stack->pop(); // Obtém o valor atual da pilha
		if ($valor_atual != 0) { // Verifica se o valor é diferente de 0
		    $ultimo_valor = $valor_atual; // Armazena o valor atual como último valor diferente de 0
		    break; // Interrompe o loop
		}
	    }
	    echo $ultimo_valor; // Imprime o último valor
	}

	$pilha = [-1, 2, 0, -4, 5, -6, -10, 0, 0, 0, 0, 0, 0];
	imprimirUltimoValorDiferenteDeZero($pilha); // Imprime -10

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
