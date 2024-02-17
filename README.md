# coamo-processo-seletivo

Modelo Entidade Relacionamento (MER):

```
Cooperativa
-----------
codigo (PK)
nome
endereco
estado

Unidade
-------
codigo (PK)
nome
municipio
cooperativa_codigo (FK)

Cooperado
---------
codigo (PK)
tipo ("Pessoa Física" ou "Pessoa Jurídica")
cpf (FK - referenciando PessoaFisica)
cnpj (FK - referenciando PessoaJuridica)

PessoaFisica
------------
cpf (PK)
rg
estadoCivil
dataNascimento

PessoaJuridica
--------------
cnpj (PK)
dataFundacao

Conceito_Cooperado
-----------------
codigo (PK)
conceito ("A", "B", "C")
cooperado_codigo (FK)

Socio
-----
nome
email
telefone
nacionalidade
pessoaJuridica_cnpj (FK)

Produto
-------
codigo (PK)
nomeComercial
formulaPrincipioAtivo
unidadeMedida

GrupoProduto
------------
codigo (PK)
tipo (Fertilizantes, Corretivos, Herbicidas, Fungicidas, Inseticidas)

Fornecimento
------------
numeroFornecimento (PK)
unidade_codigo (FK)
cooperado_codigo (FK)
produto_codigo (FK)
quantidade
data

Produto_GrupoProduto
--------------------
produto_codigo (PK, FK)
grupoProduto_codigo (PK, FK)
```

# Cardinalidades:
