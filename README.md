NajaNative

NajaNative é a implementação oficial do NajaScript, incluindo o framework, o compilador e o runtime, projetada para desenvolver aplicações Web, Mobile e Desktop com um único código. Com uma sintaxe JSX-like no frontend e uma abordagem Arquitetura inspirada no Laravel no backend, o NajaNative combina a flexibilidade do React com a estrutura robusta do Laravel.

🚀 Recursos Principais

Fullstack com NajaScript → Crie frontend e backend no mesmo código.

JSX-like no Frontend → Desenvolva interfaces com sintaxe intuitiva.

Arquitetura inspirada no Laravel no Backend → Organização semelhante ao Laravel.

Código Único e Inteligente → O NajaNative se adapta automaticamente à plataforma (Web, Mobile, Desktop).

Acesso Direto às APIs → Sem necessidade de Java, Swift ou Objective-C.

Estilização com TailwindCSS → Design rápido e moderno.

CLI Poderosa → Comando naja make gera arquivos e CRUDs completos.

📦 Instalação

Atualmente, a instalação via Naja CLI ainda não está disponível. Para utilizar o NajaNative, siga os passos abaixo:

# Clone o repositório oficial
 git clone https://github.com/CreadorLanda/NajaNative.git
 cd NajaNative

# Instalação manual ainda em desenvolvimento

📂 Estrutura MVC do NajaNative

/najanative
├── app/
│   ├── Controllers/  # Lógica das rotas e requisições
│   ├── Models/       # Definição dos modelos de dados
│   ├── Views/        # Interfaces JSX-like para renderização
├── routes/           # Definição das rotas
├── public/           # Arquivos estáticos
├── config/           # Configurações do sistema
├── storage/          # Arquivos temporários e logs
├── database/         # Migrations e seeders
├── package.json      # Configuração de pacotes
└── README.md         # Documentação

🖥️ Exemplo de Código

✨ Componente Frontend (JSX-like)

component HelloWorld {
    render() {
        return <Text class='text-xl font-bold'>Olá, Mundo!</Text>
    }
}

🔥 Rota Backend (Função route)

fun route('/api/hello') {
    return { message: 'Olá do backend!' }
}

🛠️ Exemplo CRUD Completo

📌 Modelo (User)

model User {
    id: Int
    name: String
    email: String
}

📌 Controlador (UserController)

controller UserController {
    fun index() {
        return User.all()
    }

    fun show(id) {
        return User.find(id)
    }

    fun store(data) {
        return User.create(data)
    }

    fun update(id, data) {
        return User.update(id, data)
    }

    fun destroy(id) {
        return User.delete(id)
    }
}

📌 Rotas (Definição de API)

route('/users', UserController.index)
route('/users/:id', UserController.show)
route('/users', UserController.store).method('POST')
route('/users/:id', UserController.update).method('PUT')
route('/users/:id', UserController.destroy).method('DELETE')

📌 View (Lista de Usuários)

component UserList {
    data users = fetch('/users')
    
    render() {
        return (
            <View>
                <Text class='text-2xl'>Lista de Usuários</Text>
                {users.map(user => 
                    <Text key={user.id}>{user.name} - {user.email}</Text>
                )}
            </View>
        )
    }
}

⚙️ Componentes do NajaNative

Este repositório contém todo o código-fonte do NajaNative, desenvolvido em C++, incluindo:

Framework NajaNative → Para criar aplicações Fullstack com NajaScript.

Compilador NajaNative → Transforma código NajaScript em executáveis otimizados.

Runtime NajaNative → Gerencia a execução do código em diferentes plataformas.

CLI do NajaNative → Ferramentas para facilitar o desenvolvimento.

🤝 Como Contribuir

Este é o repositório oficial do código-fonte do NajaNative, incluindo todo o compilador, runtime e framework, escrito em C++! Aqui você pode contribuir com novas funcionalidades, melhorias e correções.

Faça um fork do projeto

Crie uma branch para sua funcionalidade: git checkout -b minha-feature

Commit suas alterações: git commit -m 'Adiciona nova funcionalidade'

Push para o repositório: git push origin minha-feature

Abra um Pull Request 🚀



🔗 Repositório Oficial: NajaNative

