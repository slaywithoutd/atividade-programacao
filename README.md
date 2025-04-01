# atividade-programacao
Perguntas Dissertativas
1. Estrutura de Classes e Objetos
a) Quais atributos são definidos na classe Animal?
		nome, especie, idade
b) Como a classe AnimalSelvagem amplia a estrutura de Animal?
		novo atributo: habitat
		 
2. Herança
c) O que significa a linha class AnimalSelvagem extends Animal?
		significa que a classe AnimalSelvagem é uma "classe filha" da classe mãe Animal. Nisso dela ser filha, ela recebe os mesmos atributos qeu a classe mae. 
d) O que acontece internamente quando usamos o comando super(...) dentro do
construtor da subclasse?
		o super puxa quais atributos da classe mae a nova classe terá
		
3. Instanciação
e) O que ocorre passo a passo quando o comando new AnimalSelvagem("Nala",
"Leoa", 5, "Savana Africana") é executado?
		o novo animal selvagem criado é colocado dentro da da variavel animal2. na criaçao dessa variavel, como ela é parte da classe animal selvagem, na sua criação tem que ser dado valores pros atributos "nome", etc.. : ("Nala", "Leoa", 5, "Savana Africana").
		daqui a pouco. alem disso, previamente foi criada um método (funçao dentro de classe) exibir informaçoes como o nome, especie... depois o codigo printa no console log as informaçoes do animal2
f) Qual a diferença entre a criação dos objetos animal1 e animal2?

4. Acesso a Métodos
g) Por que o método exibirInformacoes() pode ser utilizado tanto em animal1 quanto
em animal2?
		o animal 1 é da classe animal, só tem 3 atributos
		o animal 2 é da classe animal selvagem, tem 4 atributos
h) O método exibirHabitat() está disponível em animal1? Justifique sua resposta.
		nao, exibir habitat é um metodo da classe animal selvagem, e o animal um é so animal.
		
5. Reutilização de Código
i) Como a herança contribui para evitar duplicação de código nesse exemplo?
		economiza linha, se nao teria que repetir todos os atributos do animal pro animal selvagem, alem de fazer outro metodo pra exibir as informaçoes
j) Se fosse necessário adicionar um novo comportamento a todos os animais, como
"dormir()", em qual classe ele deveria ser implementado? Por quê?
		 na classe animal, pois todos as outras presentes no código herdam dela, entao ao adicionar isso a ela, todos os animais vao ter esse atributos

6. Retorno e Impressão
k) Qual é a saída exata exibida no console ao executar o código apresentado?
		Nome: Tico, Espécie: macaco}, Idade: 4
		Nome: Nala}, Espécie: Leoa, Idade: 5
		Habitat natural: Savana Africana
l) O que aconteceria se fosse removida a linha super(nome, especie, idade) do
construtor da classe AnimalSelvagem?
	erro

7. Prática de Extensão
m) Crie uma nova subclasse chamada AnimalDomestico, que herda de Animal e inclui
um novo atributo chamado nomeDono.
n) Implemente um método chamado exibirDono() que retorne: "Dono de [nome do
animal]: [nome do dono]".

```js
// Classe derivada
class AnimalDoméstico extends Animal {
  constructor(nome, especie, idade, nomeDono) {
    super(nome, especie, idade);
    this.nomeDono = nomeDono;
  }

  exibirDono() {
    return `Dono de ${this.nome}: ${this.nomeDono}`;
  }
}
