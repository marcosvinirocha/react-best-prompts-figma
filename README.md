🔍 1. Pesquisa (Discovery)

Nesta fase, o objetivo é garantir que a IA não "invente" soluções, mas sim entenda as ferramentas e o código que já existem.

Prompt Modelo:

    "Atue como um Engenheiro de Software Sênior. Antes de sugerir qualquer implementação, realize uma pesquisa profunda no repositório atual.

        Analise a pasta /src/components e /src/lib para identificar padrões de design e utilitários existentes.

        Leia a documentação oficial de [Inserir Tecnologia/Biblioteca] para entender as melhores práticas da versão mais recente.

        Identifique como as rotas e o estado global estão sendo gerenciados neste projeto.
        Saída esperada: Um resumo técnico das dependências relevantes, componentes que podem ser reutilizados e potenciais conflitos técnicos."

📝 2. Spec (Especificação)

Aqui você cria o "contrato" do que será feito. É o filtro que impede o código de desviar do objetivo original.

Prompt Modelo:

    "Com base na pesquisa realizada, crie um arquivo chamado spec.md para a nova funcionalidade: [Nome da Funcionalidade].
    O documento deve conter:

        Objetivo: Descrição clara do que a feature faz.

        Arquivos Afetados: Lista de arquivos existentes que serão modificados.

        Novos Arquivos: Estrutura de pastas e nomes de arquivos a serem criados.

        Interface/Props: Definição de tipos TypeScript para os novos componentes/funções.

        Lógica de Negócio: Step-by-step do comportamento esperado.
        Regra: Não escreva o código completo ainda, foque na arquitetura e nas definições."

💻 3. Code (Implementação)

Com a spec aprovada, a IA agora tem um mapa exato. Isso minimiza alucinações e código desnecessário.

Prompt Modelo:

    "Utilize o arquivo spec.md como única fonte de verdade para a implementação.

        Implemente os arquivos listados seguindo rigorosamente as definições de tipos e a lógica descrita.

        Mantenha o estilo de código consistente com o restante do projeto (ex: Tailwind CSS, imports absolutos).

        Remova qualquer código morto ou redundante que não foi solicitado na spec.

        Após terminar, execute os testes ou verifique se a tipagem está correta.
        Foco: Simplicidade e aderência total à especificação."
