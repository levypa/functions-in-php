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
#Random

function sortearNumero() {
  $numerosSorteados = array();
  do {
    $numeroSorteado = rand(1, 100);
  } while (in_array($numeroSorteado, $numerosSorteados));
  array_push($numerosSorteados, $numeroSorteado);
  return $numeroSorteado;
}

$numerosSorteados = array();
for ($i = 0; $i < 5; $i++) {
  $numeroSorteado = sortearNumero();
  array_push($numerosSorteados, $numeroSorteado);
  echo "O número sorteado é: " . $numeroSorteado . ",\n";
}

  
  
  
  
/*
$precoVenda = 7.00;
$precoDesconto = 6.98;
$taxaPadrao = 5;
$precoVendaPadrao = ($precoVenda * $taxaPadrao) * 0.01;
$comissao = $precoVendaPadrao / 50.00;

echo "Preço de Venda Padrão = ", number_format($precoVendaPadrao,4,",","."), "\n";
echo "Comissão Padrão = ", number_format($comissao,4,",","."), "\n";
echo "###########################", "\n";


for($precoVenda = 7.00; $precoVenda >= $precoDesconto; $precoVenda-=0.01){
	
	$precoVendaReduzida = ($precoVendaPadrao - $comissao);
	
	$precoAjustado = $precoVenda - $precoVendaReduzida;
	
	echo "Preço de Venda = ", number_format($precoVenda,4,",","."), "\n";
	echo "Preço de Venda Reduzida = ", number_format($precoVendaReduzida,4,",","."), "\n";
	echo "Preço de Venda Reduzido e Ajustado = ", number_format($precoAjustado,4,",","."), "\n";
	
}


/*

for($precoVenda = 7.00; $precoVenda >= $desconto; $precoVenda-=0.01){
	
	$precoVendaReduzida = $precoVenda -=0.01;
	echo "Preço Venda Reduzida = ", number_format($precoVendaReduzida,2,",","."), "\n";
	$custoVendaPadrao = ($precoVenda * $taxaPadrao) / 100;
	echo "Custo de Venda Padrão = ", number_format($custoVendaPadrao,4,",","."), "\n";
	$taxaReduzida = $precoVendaReduzida / ($taxaPadrao-=0.01);
	echo "Taxa Reduzida = ", number_format($taxaReduzida,4,",","."), "\n";

//	$comissaoReduzida = $precoVendaReduzida - 
	
    //$custoVendaPadrao = ($precoVenda * $taxaPadrao) * 0.01;
    
     


	//echo "Preço de Venda = ", number_format($precoVenda,4,",","."), "\n";
    //echo "Custo de Venda Padrão = ", number_format($custoVendaPadrao,4,",","."), "\n";
    //echo "Taxa Reduzida = ", number_format($taxaReduzida,4,",","."), "\n";
   
    
}




