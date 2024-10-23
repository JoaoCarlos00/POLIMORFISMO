# POLIMORFISMO

Exercício da AC2 sobre Polimorfismo

## 🚀 Enunciado

Recrie a hierarquia de classes dessa aula e implemente o método enviar email. Esse método deve receber o corpo da mensagem e acrescentar a ela uma saudação de acordo com a implementação do objeto.

Por exemplo:

Olá Prof.  Alan Turing!

Mensagem ….

Ou

Olá Aluno Joseph!

Mensagem …

### 📋 Código

package Usuario;

	abstract class Usuario { //Começo criando a classe abstrata que irá fornecer a estrutura básica na qual as outras classes irão derivar
		protected String nome;

		public Usuario(String nome) {
        this.nome = nome;
    }

    public abstract String enviarEmail(String corpoMensagem);
}
	class Professor extends Usuario { //A primeira classe é a do professor. Também é criado o corpo da mensagem que irá por email ao aluno
		public Professor(String nome) {
        super(nome);
    }

    @Override
    public String enviarEmail(String corpoMensagem) {
        return "Olá Prof. " + nome + "!\n\n" + corpoMensagem;
    }
}
	class Aluno extends Usuario { //E a segunda classe é a do aluno que também é criado o corpo da mensagem que irá por email ao professor
	    public Aluno(String nome) {
	        super(nome);
	    }

	    @Override
	    public String enviarEmail(String corpoMensagem) {
	        return "Olá Aluno " + nome + "!\n\n" + corpoMensagem;
	    }
	

	    public static void main(String[] args) { //E por último é criado as mensagens que irão tanto para o professor como para o aluno via email
	        Usuario professor = new Professor("Alan Turing");
	        Usuario aluno = new Aluno("Joseph");

	        String mensagemProfessor = professor.enviarEmail("Olá professor, quando eu posso fazer a avaliação substitutiva?");
	        String mensagemAluno = aluno.enviarEmail("Você poderá fazer a avaliação substitutiva amanhã.");

	        System.out.println(mensagemProfessor);
	        System.out.println(mensagemAluno);
	    }
	}

### 🔧 Instalação

* Explicação de como deve ser utilizado o projeto

## 🛠️ Construído com

Ferramentas utilizadas e bibliotecas

* IDE Eclipse

## 📌 Versão

* **Versão 1.0** caso seja atualizado manter a descrição inicial e inserir uma nova linha com descrição da atualização.
* **Versão 1.1** - *Refatoração* *data 09/09/24*

## ✒️ Autores

* João Carlos Ferreira de Araujo RA 248152 - AC2 de Programação Orientada à Objetos

