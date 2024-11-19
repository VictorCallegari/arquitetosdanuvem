
# **Topologia de Rede Estrela - Cisco Packet Tracer**

Este repositório contém a atividade prática realizada para o curso **Arquitetos da Nuvem** da **PROZ e AWS**, onde configuramos uma rede de computadores utilizando o Cisco Packet Tracer. A tarefa consistiu em criar uma topologia de rede estrela para garantir a comunicação entre os membros da equipe de produção de um show.

---

## **Objetivo**

Configurar uma topologia de rede do tipo estrela para que quatro computadores, representando os membros da equipe de produção, possam se comunicar de forma eficiente e garantir que o show ocorra sem problemas.

---

## **Detalhes da Configuração**

1. **Dispositivos Utilizados:**
   - 1 Switch.
   - 4 PCs (representando membros da equipe de produção).

2. **Conexões:**
   - Todos os PCs foram conectados ao switch utilizando cabos **Copper Straight-Through (Ethernet)**.

3. **Configuração de Endereços IP:**
   - Os computadores foram configurados na mesma sub-rede:
     - **PC1:** `192.168.1.2`
     - **PC2:** `192.168.1.3`
     - **PC3:** `192.168.1.4`
     - **PC4:** `192.168.1.5`
   - Máscara de sub-rede utilizada: `255.255.255.0`.

4. **Testes Realizados:**
   - Foi utilizado o comando `ping` em cada PC para testar a comunicação com os outros dispositivos na rede.

---

## **Resultados Esperados**

- Comunicação bem-sucedida entre todos os computadores.  
- Comando `ping` retornando pacotes enviados e recebidos sem perdas.  
- Rede configurada no formato estrela, com o switch no centro, garantindo eficiência na comunicação.

---

## **Arquivos Disponíveis**

- **`Topologia_Rede_Estrela.pkt`**: Arquivo do Cisco Packet Tracer com a configuração completa da rede.
- **`screenshots/`**: Prints da topologia e dos testes de comunicação realizados com o comando `ping`.

---

## **Como Carregar o Projeto**

1. Baixe o arquivo `Topologia_Rede_Estrela.pkt`.
2. Abra o Cisco Packet Tracer.
3. Carregue o arquivo no programa.
4. Explore a configuração e os testes realizados.

---

## **Instruções para Testar**

1. Acesse qualquer PC na topologia.
2. Abra o **Prompt de Comando** do PC.
3. Execute o comando `ping` para os outros PCs na rede. Por exemplo:
   ```bash
   ping 192.168.1.3
   ```
4. Observe o retorno indicando sucesso na comunicação.

---

## **Contribuição**

Este projeto foi desenvolvido por **Victor Ramos Andrade Callegari** como parte das atividades do curso **Arquitetos da Nuvem** oferecido pela **PROZ e AWS**.

Caso tenha dúvidas ou sugestões, fique à vontade para entrar em contato! 😊
