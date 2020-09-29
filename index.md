<html>

<head></head>

<body>
 <center>
      
      <h1>Calculadora DGOI Em fase de Testes</h1>
      <h3>Criado por Lucas Ribeiro</h3>
      <h4>Atualize a página para calcular novamente</h4>
      <h4>Contato: 11 94131-4539</h4>
      <h4>Adicione a página a sua tela inicial </h4>
      <h4>Calcula para Padrão Prumada de 8 Tubos 6 Fibras 
Por Tubo</h4>

    <script type="text/javascript">
        alert("Calculadora de Prumada DGOI \n criado por Lucas Ribeiro");
        alert("Padrão para Prumada de 8 Tubos 6 Fibras por Tudo");
        var NumeracaoCaboRise = [
            [0,0],
            [1,6],
            [7,12],
            [13,18],
            [19,24],
            [25,30],
            [31,36],
            [37,42],
            [43,48]
        ];

        var coresTuboRise = ["", "VERDE","AMARELO"
        ,"BRANCO","AZUL","VERMELHO","VIOLETA","MARROM","ROSA"];

        var coresRiseFibra = ["", "VIOLETA", "VERMELHO", "AZUL", "BRANCA", "AMARELA", "VERDE"];

        var opt = prompt("Digite a numeração da caixa para saber");

        var respTubo, respFibra, cabo;

        function validarCorTubo(){
            
            var o = opt;
            cabo = 1;
            if(o >= 49 && o <= 96){
                o = o - 48;
                cabo = 2;
            }else if(o >= 97 && o <= 144){
               o = o - 96;
               cabo = 3;
            }

            if(o >= 1 && o < 1+6){
                respTubo = coresTuboRise[1];
            }else if(o >= 7 && o < 7+6){
                respTubo = coresTuboRise[2];
            }else if(o >= 13 && o < 13+6){
                respTubo = coresTuboRise[3]
            }else if(o >= 19 && o < 19+6){
                respTubo = coresTuboRise[4]
            }else if(o >= 25 && o < 25+6){
                respTubo = coresTuboRise[5]
            }else if(o >= 31 && o < 31+6){
                respTubo = coresTuboRise[6]
            }else if(o >= 37 && o < 37+6){
                respTubo = coresTuboRise[7]
            }else if(o >= 43 && o < 43+6){
                respTubo = coresTuboRise[8]
            }
                        
        }

      function validarCorFibra(){
            var o = opt;
            
            if(o >= 49 && o <= 96){
                o = o - 48;
            }else if(o >= 97 && o <= 144){
               o = o - 96;
            }
            
            var x = 0;
            
            if(o >= 1 && o < 1+6){
                x = 1+6 - o;
            }else if(o >= 7 && o < 7+6){
                x = 7+6 - o;
            }else if(o >= 13 && o < 13+6){
                x = 13+6 - o;
            }else if(o >= 19 && o < 19+6){
                x = 19+6 - o;
            }else if(o >= 25 && o < 25+6){
                x = 25+6 - o;
            }else if(o >= 31 && o < 31+6){
                x = 31+6 - o;
            }else if(o >= 37 && o < 37+6){
                x = 37+6 - o;
            }else if(o >= 43 && o < 43+6){
                x = 43+6 - o;
            }
            
            o = x;
            
            switch(o){
              case 1:
                  respFibra = coresRiseFibra[1];
                  break;
                case 2:
                  respFibra = coresRiseFibra[2];
                  break;
                case 3:
                  respFibra = coresRiseFibra[3];
                  break;
                case 4:
                  respFibra = coresRiseFibra[4];
                  break;
                case 5:
                  respFibra = coresRiseFibra[5];
                  break;
                case 6:
                  respFibra = coresRiseFibra[6];
                  break;
            }
            
      }


      validarCorTubo();
      validarCorFibra();

      alert("CABO " + cabo + " TUBO " + respTubo + " COR DA FIBRA " + respFibra);

    </script>

</body>

</html>
