# BÁSICO REDES
O objetivo deste projeto é realizar um estudo básico de redes, combinando uma análise teórica com a observação prática no CMD. Essa abordagem busca complementar e fortalecer meu aprendizado continuamente.

# COMANDO PING 

O ping é um comando utilizado para testar a conectividade entre dois dispositivos em uma rede. Ele funciona enviando pacotes ICMP (Internet Control Message Protocol) para um endereço de destino e aguardando uma resposta.

Como funciona?
1 - O dispositivo de origem envia um pacote ICMP Echo Request para o destino.
2 -  Se o destino estiver acessível, ele responde com um ICMP Echo Reply.
3 - O ping mede o tempo de resposta (latência) e indica se houve perda de pacotes.

📌 Exemplo de uso no CMD:

ping google.com

📌 Saída esperada:

Resposta de 142.250.78.238: bytes=32 tempo=25ms TTL=56

🔹 bytes=32 → Tamanho do pacote enviado.

🔹 tempo=25ms → Tempo que o pacote levou para ir e voltar (latência).

🔹 TTL=56 → Quantidade de saltos (roteadores) que o pacote pode fazer antes de ser descartado.

📌 Para que serve?
✅ Verificar se um site ou servidor está respondendo.

✅ Medir a qualidade da conexão (latência).

✅ Diagnosticar problemas de rede (como perda de pacotes).

Exemplo: Utilizado DNS do Google

![Image](https://github.com/user-attachments/assets/b1867418-beb1-4567-9c21-f1318173d006)


# COMANDO TRACERT 

🔹 Como Funciona?

1) Envio de Pacotes

O tracert envia pacotes ICMP (ou UDP no caso do traceroute em Linux).
Ele começa com um Time To Live (TTL) = 1, e a cada salto (hop) o TTL aumenta.

 
2) Respostas dos Roteadores

Quando um pacote atinge um roteador, se o TTL for 0, o roteador responde com uma mensagem Time Exceeded.
O tracert anota o tempo da resposta e o endereço IP do roteador.

3) Destino Alcançado

O processo continua até que os pacotes alcancem o servidor de destino.

📌 Exemplo de uso no CMD:

tracert google.com

📌 Saída esperada:

(EXEMPLO)
Rastreando a rota para google.com [142.250.219.78]
1    <1 ms    <1 ms    <1 ms  192.168.1.1
2     9 ms     7 ms     8 ms  10.10.10.1
3    15 ms    14 ms    13 ms  200.100.50.1
4    30 ms    29 ms    28 ms  142.250.219.78

Exemplo: Utilizado DNS do Google

![Image](https://github.com/user-attachments/assets/df5e1922-be34-4154-8df3-04ef218de47a)
