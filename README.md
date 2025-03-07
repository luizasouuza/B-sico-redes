# BÁSICO REDES
O objetivo deste projeto é realizar um estudo básico de redes, combinando uma análise teórica com a observação prática no CMD. Essa abordagem busca complementar e fortalecer meu aprendizado continuamente.

# PING 

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
