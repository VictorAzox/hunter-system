# ⚔️ SISTEMA DE HUNTER: MONARCA DAS SOMBRAS

Este é um sistema de monitoramento de treino inspirado no universo de **Solo Leveling**. O projeto funciona como uma aplicação Full-Stack, permitindo que usuários (Hunters) registrem seus treinos, subam de nível e disputem o topo do Ranking Global.

## 🚀 Funcionalidades Atuais

- **Identificação Única:** Sistema de "Despertar" que bloqueia nomes duplicados, garantindo que cada Hunter tenha sua identidade exclusiva.
- **Progressão de Rank:** Evolução dinâmica de **Rank E até Rank S** baseada no nível do usuário.
- **Ranking Global em Tempo Real:** Conexão bidirecional com **Firebase Firestore**, onde as mudanças no servidor refletem instantaneamente no navegador/celular.
- **Sistema de Quests Dinâmicas:** Exercícios que mudam automaticamente conforme o seu Rank atual aumenta.
- **Trilha Sonora Imersiva:** Player integrado com API do YouTube para tocar playlists épicas durante o treino.
- **Penalidade por Falha:** Sistema que reseta seu "Combo" (Streak) caso você fique mais de 24 horas sem registrar uma missão.

## 🛠️ Tecnologias Utilizadas

- **Frontend:** HTML5, CSS3 (Custom Variables & Flexbox), JavaScript (ES6+).
- **Backend/Database:** Google Firebase Firestore (NoSQL).
- **Integrações:** YouTube IFrame Player API.
- **Hospedagem:** GitHub Pages.

## 📊 Estrutura de Progressão

| Rank | Nível Necessário | Dificuldade |
| :--- | :--- | :--- |
| **E** | Nível 1 - 4 | Iniciante |
| **D** | Nível 5 - 14 | Recruta |
| **C** | Nível 15 - 29 | Combatente |
| **B** | Nível 30 - 49 | Elite |
| **A** | Nível 50 - 79 | Mestre |
| **S** | Nível 80+ | Monarca |

## ⚙️ Como o Sistema funciona (Lógica Técnica)

1.  **Sincronização:** O site utiliza um "Listener" (`onSnapshot`) que monitora o banco de dados. Se o nível do Hunter for alterado manualmente no painel do Firebase, o site atualiza a interface sem necessidade de recarregar.
2.  **Segurança:** Implementada trava de verificação assíncrona para evitar que dois usuários utilizem o mesmo ID de Hunter.
3.  **Persistência:** Uso de `localStorage` para cache rápido e `Firestore` para armazenamento persistente na nuvem.

## ✒️ Autor

Projeto desenvolvido como parte do treinamento de evolução de Hunter.
*"Erga-se."*
