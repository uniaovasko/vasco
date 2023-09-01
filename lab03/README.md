# Equipe União Vasko

# Subgrupo A
* Gabriel de Carvalho Silva Nascimento - 222103
* Breno Shigeki Guimarães Nishimoto - 220599
* Mateus da Costa e Silva Rios Alves de Andrade - 230806

# Modelo Conceitual

<img src="images/ER_Restaurante.png" width="400px" height="auto">

Diagrama ER Revisado

# Mapeamento para o Modelo Relacional
~~~
ALUNO(_RA_, Nome)

BANDEJA(_Aluno_, _Data_, _Turno_, Porções)
  Aluno chave estrangeira -> ALUNO(RA)
  Data chave estrangeira -> CARDÁPIO(Data)
  Turno chave estrangeira -> CARDÁPIO(Turno)

CARDÁPIO(_Data_, _Turno_, Bebida)
  Bebida chave estrangeira -> Porção(Nome)

CAFÉ_DA MANHA(_Data_, _Turno_, Bebida, Cereal, Complemento)
  Cereal chave estrangeira -> PORÇÃO(Nome)
  Complemento chave estrangeira -> PORÇÃO(Nome)

REFEIÇÃO(_Data_, _Turno_, Bebida, Salada, Prato Principal Vegano, Prato Principal, Sobremesa Natural, Sobremesa Industrializada)
  Salada chave estrangeira -> PORÇÃO(Nome)
  Prato Principal Vegano chave estrangeira -> PORÇÃO(Nome)
  Prato Principal chave estrangeira -> PORÇÃO(Nome)
  Sobremesa industrializada chave estrangeira -> PORÇÃO(Nome)
  Sobremesa natural chave estrangeira -> PORÇÃO(Nome)

INGREDIENTE(_Código_, Nome, Informação Nutricional, Ingredientes)
  Ingredientes chave estrangeira -> INGREDIENTE(Código)

PORÇÃO(_Código_, Nome, Informação Nutricional, É Vegano, Quantidade, Estatísticas de Consumo, Ingredientes)
  Ingredientes chave estrangeira -> INGREDIENTE(Código)
~~~