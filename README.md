# RELATÓRIO TÉCNICO - SOBRE PROGRAMAÇÃO ORIENTADA A OBJETOS (POO)

1- O QUE É A PROGRAMAÇÃO ORIENTADA A OBJETOS

A Programação Orientada a Objetos é um paradigma de desenvolvimento de software baseado no uso de objetos, que representam entidades do mundo real. Cada objeto possui atributos (dados) e métodos (ações).

2 - POR QUE O POO SURGIU?

Antes do POO, a programação era majoritariamente processual, baseada em funções que manipulavam dados soltos. À medida que os sistemas se apresentavam mais complexos, esse modelo se tornou difícil de manter por causa de problemas como:

•	Baixa modularidade
•	Código Repetido
•	Dificuldade de reutilização
•	Falta de proteção dos dados
•	falta de organização lógica

## PILARES DA POO

1 - Encapsulamento

Embale dados e comportamentos dentro de um objeto, permitindo que apenas métodos específicos tenham acesso a certas informações. Isso protege o estado interno e evita alterações indevidas.

•	EXEMPLO PYTHON

```python
class ContaBancaria:
def __init__(self, saldo):
self.__saldo = saldo 


def depositar(self, valor):
if valor > 0:
self.__saldo += valor


def consultar_saldo(self):
return self.__saldo


conta = ContaBancaria(200)
conta.depositar(80)
print(conta.consultar_saldo()) # 280 
```
2 - Herança

Permite que uma classe herde atributos e métodos de outra, reaproveitando código e criando especializações.

•	EXEMPLO PYTHON

```python
class ContaBancaria:
def __init__(self, saldo):
self.__saldo = saldo 


def depositar(self, valor):
if valor > 0:
self.__saldo += valor


def consultar_saldo(self):
return self.__saldo


conta = ContaBancaria(200)
conta.depositar(80)
print(conta.consultar_saldo()) # 280
```



3 - Polimorfismo

Permite que diferentes classes implementem o mesmo método de formas diferentes, possibilitando comportamentos variados usando uma mesma interface.

•	Exemplo (Python)

````PYTHON
class Funcionario:
def salario(self):
pass


class Estagiario(Funcionario):
def salario(self):
return 1200


class Gerente(Funcionario):
def salario(self):
return 8000


lista = [Estagiario(), Gerente()]


for f in lista:
print(f.salario())
````

4 - Abstração

Simplifica a complexidade destacando apenas o que é essencial para o uso de um objeto, escondendo detalhes internos.

•	EXEMPLO PYTHON

```PYTHON
From abc import ABC, abstractmethod


class Pagamento(ABC):
@abstractmethod
def processar(self):
pass


class Pix(Pagamento):
def processar(self):
print("Pagamento via Pix realizado.")


p = Pix()
p.processar()
```

CONCLUSÃO

A Programação Orientada a Objetos é fundamental para criar sistemas organizados, reutilizáveis e simples de manter. Ao desenvolver este relatório, foi possível reforçar o entendimento dos quatro pilares do POO e perceber como cada um deles contribui para estruturar softwares mais claros e eficientes.

