# semaforo_picow
## Atividade 1: Temporizador periódico. Aula síncrona 29/01/2025

**A função main contém:**  

 * todas as inicializações e configurações de interfaces seriais e pinos GPIO;
 * declaração da struct timer, que armazena as configurações de funcionamento do timer alocado pelo SDK;
 * chamada à função add_repeating_timer_ms(3000, traffic_light_callback, NULL, &timer);
             - argumentos: 3000-> intervalo de tempo em ms; traffic_light_callback -> nome da callback que será chamada periodicamente; NULL(não há dados do usuário);                             &timer-> endereço base da struct timer que será usada pela callback.
 * No loop infinito: haverá uma printf e um delay para repetir a cada segundo uma mensagem qualquer, por exeplo: Semáforo em Operação.
   
**A função traffic_light_callback:**

Utiliza a variável state que pode assumir os valores 0,1,2 - cada um desses valores representa uma cominação válidadas lâmpadas de um semáforo, as quais são mostradas na sequência estado vermelho, estado amarelo e estado verde. A incrementação da variável estado faz com que os leds sejam acesos na sequência correta. A introcução de uma operação de módulo (%3), faz com que o incremento vá de 0 até 2 e depois retorne ao 0, reiniciando a contagem.

Com base nessa variável state, é utilizado um switch-case para decidir qual é o estado a ser apresentado na tríade de leds.

## Vídeo Explicativo

Confira o vídeo no link abaixo:

[![Assista no YouTube](https://img.youtube.com/vi/uNkxGCQuGwY/maxresdefault.jpg)](https://youtu.be/uNkxGCQuGwY)
