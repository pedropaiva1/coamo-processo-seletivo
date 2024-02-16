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
