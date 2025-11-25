# Desafio-Detective-Quest
Descrição Detalhada dos Códigos

🎮 Código 1: Sistema Básico de Exploração

O que acontece:

· Cria uma mansão como árvore binária com 7 salas
· O jogador começa no "Hall de Entrada"
· Navega escolhendo entre Esquerda (e) ou Direita (d)
· Quando chega em uma sala sem saídas, o jogo termina

Estrutura da Mansão:

```
Hall de Entrada
    ├── Sala de Estar
    │   ├── Biblioteca
    │   └── Escritório Secreto
    └── Cozinha
        ├── Jardim de Inverno
        └── Sala de Jogos
```

Fluxo do Programa:

1. Monta a árvore manualmente na main()
2. Chama explorarSalas() começando pelo Hall
3. Mostra sala atual e opções disponíveis
4. Repete até encontrar sala sem saídas

---

🔍 Código 2: Sistema de Coleta de Pistas

Novidades adicionadas:

· Cada sala agora tem uma pista específica
· Cria uma árvore BST para armazenar pistas em ordem alfabética
· Pistas são coletadas automaticamente ao entrar na sala
· Exibe todas as pistas ordenadas ao final

Pistas por Sala:

· Hall de Entrada: Porta arrombada
· Sala de Estar: Copo de vinho
· Biblioteca: Livro de venenos
· Escritório: Carta de ameaça
· Cozinha: Faca desaparecida
· Jardim: Pegadas de barro
· Sala de Jogos: Relógio quebrado

Fluxo Aprimorado:

1. Entra na sala → Mostra pista → Adiciona na BST
2. Pista é removida da sala após coleta
3. Ao sair, exibe pistas em ordem alfabética

---

🕵️ Código 3: Sistema Completo de Investigação

Recursos Adicionados:

· Tabela Hash vinculando pistas a suspeitos
· 5 suspeitos com múltiplas pistas cada
· Sistema de acusação final
· Validação requer ≥2 pistas contra o culpado

Tabela Hash de Suspeitos:

```
Carlos    → Porta arrombada, Faca desaparecida
Ana       → Copo com batom, Relógio parado
Roberto   → Livro de venenos
Mariana   → Carta datilografada, Perfume francês
Pedro     → Pegadas de lama
```

Fases do Jogo:

1. Exploração: Coletar pistas pelas salas
2. Análise: Ver pistas e suspeitos associados
3. Acusação: Escolher culpado baseado nas evidências
4. Veredito: Sistema valida se há provas suficientes

Estruturas de Dados Integradas:

```
ÁRVORE BINÁRIA (Salas)
        ↓
   ÁRVORE BST (Pistas ordenadas)
        ↓
  TABELA HASH (Pista → Suspeito)
        ↓
SISTEMA DE ACUSAÇÃO (Validação)
```

---

📋 RESUMO GERAL

Evolução dos Três Códigos:

1. 🎯 Básico → Exploração Pura

· Só navegação pela árvore binária
· Objetivo: Chegar ao final da mansão
· Estrutura: Apenas árvore binária simples

2. 🔍 Intermediário → Coleta de Evidências

· Adiciona sistema de pistas em BST ordenada
· Objetivo: Coletar todas as pistas possíveis
· Estruturas: Árvore binária + Árvore BST

3. 🕵️ Avançado → Investigação Completa

· Sistema dedutivo com suspeitos e acusação
· Objetivo: Identificar culpado com base em evidências
· Estruturas: Árvore binária + BST + Tabela Hash + Validação lógica

🎊 Conclusão:

O projeto evoluiu de uma simples exploração de mapa para um jogo detective completo onde o jogador usa múltiplas estruturas de dados integradas para coletar pistas, associá-las a suspeitos através de uma tabela hash, e finalmente fazer uma acusação validada logicamente baseada na contagem de evidências! 🎯
