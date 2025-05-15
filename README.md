# Arquitetura-de-Computadores (CE4411) - Projeto Máquina de Café Caseira

<p align="justify">
#### Este repositório serve como template para o desenvolvimento do projeto da disciplina de Arquitetura de Computadores (CE4411) do Centro Universitário FEI.

**Desenvolvedor:** Morgana Rodrigues Zanetti - R.A.: 24.223.010-0
---

**Introdução:**  
O projeto visa simular uma cafeteira caseira (modelo de cápsulas), utilizando a linguagem Assembly em conjunto com o simulador EdSim51. A proposta tem como objetivo implementar os conhecimentos adquiridos ao longo das aulas.


**Descrição do projeto:**  
Durante o desenvolvimento do projeto, foram utilizadas 3 periféricos disponíveis no simulador, sendo eles:
  - Monitor serial
  - 3 LEDs
  - 7 dos 8 botões disponíveis 

**Botões Utilizados:**
| Botão | Função | 
| --- | --- |
| 1 | Botão de temperatura | 
| 2 | Botão de intensidade |
| 4 | Botão para sair da sub-rotina |
| 4 | Botão para preparo da bebida |
| 5 | Botão para copo |
| 6 | Botão para cápsula |
| 7 | Botão para água |

>O botão 4 foi reutilizado para duas funções: sair da sub-rotina e iniciar o preparo da bebida.
    
**Registrador de Processador Utilizados:**  
| Registrador | Função |
| --- | --- |
| R0 | delay |
| R1 | timer de preparo da bebida |
| R2 | intensidade da bebida |
| R3 | sair da sub-rotina |
| R4 | temperatura da bebida |
| R5 | colocar copo |
| R6 | colocar cápsula |
| R7 |colocar água |

**Funcionamento:**  
Ao iniciar o programa, o LED vermelho será aceso, indicando que a cafeteira está desligada. Ao pressionar o botão 0, a máquina será ligada (o LED vermelho será apagado e o LED verde será aceso). Em seguida, o usuário deve adicionar os itens necessários para o preparo da bebida: água, cápsula e copo. Cada item possui um limite pré-definido:
   - Água: pode ser adicionada até 3 vezes (incrementa um até alcançar o limite)
   - Cápsula e copo: podem ser adicionados apenas uma vez
Enquanto faltar algum dos itens acima, a bebida não será preparada. E, quando todos os itens estiverem presentes, o usuário poderá definir:
	- Intensidade da bebida: fraco, médio ou forte
 	- Temperatura da bebida: frio, morno ou quente
Com todas as opções definidas, o preparo pode ser iniciado pressionando novamente o botão 4. Durante o preparo, o LED amarelo será aceso e a mensagem 'Preparando' será exibida no monitor serial. Após concluir o preparo, o LED verde acenderá e a mensagem "Bebida pronta" será exibida no monitor serial.

**Observações:**  
 - O botão 4 foi reaproveitado e está sendo utlizado tanto para sair da sub-rotina quanto para iniciar o preparo da bebida. Modo de funcionamento:
		- configure a temperatura → pressione 4 para sair
		- configure a intensidade → pressione 4 novamente para iniciar o preparo
 - A frequência indicada para a simulação no EdSim51 é 350 Hz
</p>

---
## **Resultados:**  
<p align="center">
Cafeteira Desligada
</p>

![](https://github.com/user-attachments/assets/e9e0c189-d838-48b9-8cc2-a65a36f1a321)

<p align="center">
Cafeteira Ligada
</p>

![](https://github.com/user-attachments/assets/7b6238aa-eb83-45e5-91e7-2bafdcf7252e)


<p align="center">
Mensagem de Erroo
</p>

![erro](https://github.com/user-attachments/assets/d098b654-136f-4862-85ee-c0858b428c41)


<p align="center">
Incrementando os Registradores
</p>

![](https://github.com/user-attachments/assets/175073c1-a723-4eb3-8a4b-b4d69bbeaf0d)


<p align="center">
Preparando Bebida
</p>

![](https://github.com/user-attachments/assets/2fa5b5c3-fea6-4036-8916-beba28a39cdb)


<p align="center">
Bebida Pronta
</p>

![](https://github.com/user-attachments/assets/90b6ebc9-e331-4d3d-956b-5aaa9aca02ba)


<p align="center">
Reiniciando Cafeteira
</p>

![](https://github.com/user-attachments/assets/4102f724-e67f-4307-ad28-c3a6aa177be4)

![reiniciando-cafeteira(2)](https://github.com/user-attachments/assets/02ea0307-d4b6-4b11-ac49-78926d3d7812)
