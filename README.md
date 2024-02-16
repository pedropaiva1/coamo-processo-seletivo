# coamo-processo-seletivo

Modelo Entidade Relacionamento (MER):

```
Cooperativa:
    codigo: inteiro
    nome: string
    endereço: string
    estado: string

Unidade:
    codigo: inteiro
    nome: string
    município: string
    cooperativa: Cooperativa

Cooperado:
    codigo: inteiro
    tipo: string ("Pessoa Física", "Pessoa Jurídica")
    conceito: string ("A", "B", "C")

PessoaFisica:
    cpf: string
    rg: string
    estadoCivil: string
    dataNascimento: data
    cooperado: Cooperado

PessoaJuridica:
    cnpj: string
    dataFundacao: data
    cooperado: Cooperado

Socio:
    cpf: string
    rg: string
    nacionalidade: string (opcional)
    pessoaJuridica: PessoaJuridica

Produto:
    codigo: inteiro
    nomeComercial: string
    formulaPrincipioAtivo: string
    unidadeMedida: string

GrupoProduto:
    codigo: inteiro
    descricao: string

```

# Cardinalidades:

Cooperativa

```
Possui (1:N) -> Unidade 
```


Unidade

```
Fornece (N:N) -> Cooperado 
Fornece (N:N) -> Produto 
```


Cooperado 

```
É (1:1) -> Pessoa Física
É (1:1) -> Pessoa Jurídica 
```


Pessoa Física 

```
Pertence (1:N) -> Cooperado
```


Pessoa Jurídica 

```
Pertence (1:N) -> Cooperado
Possui (1:N) -> Sócio
```


Sócio


```
Pertence (1:N) -> Pessoa Jurídica
```

Produto 

```
Pertence (N:N) -> Grupo de Produto
```
