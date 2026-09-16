# projetoDIO
Repositório com o Miniguia de Estudos e a documentação dos testes de Engenharia de Prompts realizados no NotebookLM para o desafio prático da DIO.

## Contexto e Objetivos

### Contexto
Este caderno temático foi desenvolvido para estruturar uma base de conhecimento confiável sobre o **Simples Nacional**, um dos regimes tributários mais relevantes para micro e pequenas empresas no Brasil. Para garantir respostas precisas e evitar alucinações da IA, a base foi alimentada exclusivamente com documentações oficiais do Governo Federal e portais tributários de referência.

### Objetivos
* **Criar um Especialista em Simples Nacional:** Utilizar o NotebookLM como um assistente de consulta rápida para regras, limites de faturamento e enquadramento de atividades.
* **Praticar Aprendizagem Ativa e Engenharia de Prompts:** Testar diferentes abordagens de perguntas para extrair análises comparativas, tabelas de alíquotas e resumos práticos das fontes.
* **Consolidar um Miniguia Reutilizável:** Gerar um acervo com resumos, glossário e um banco de prompts prontos para consultas fiscais e tributárias futuras.

* ## 📚 Curadoria de Fontes

Para garantir a precisão do assistente e evitar respostas incorretas, o caderno foi alimentado exclusivamente com fontes oficiais:

* **[Lei Complementar nº 123/2006](https://www.planalto.gov.br/ccivil_03/leis/lcp/lcp123.htm):** Estabelece o Estatuto Nacional da Microempresa e da Empresa de Pequeno Porte.
* **[Portal do Simples Nacional - Perguntas e Respostas](https://www8.receita.fazenda.gov.br/SimplesNacional/Arquivos/manual/PerguntaoSN.pdf):** Base de conhecimento oficial com as principais dúvidas e regras de enquadramento.
* **[Resolução CGSN nº 140/2018](https://www.in.gov.br/web/dou/-/resolucao-n-140-de-22-de-maio-de-2018-15742358):** Regulamentação detalhada sobre a tributação, apuração e recolhimento dos tributos do Simples Nacional.

* ## 🧪 Engenharia de Prompts e "Cicatrizes" (Troubleshooting)

Nesta etapa, foram testadas diferentes abordagens de perguntas para validar a precisão do assistente sobre o Simples Nacional.

#### Teste 1: Conceito Geral vs. Estrutura Prática
* **Prompt Inicial:** "O que é o Simples Nacional e quem pode participar?"
* **Resultado:** Resposta textual muito longa e completa, com todas as informações necessárias, mas com certo teor técnico que pode  prejudicar o leitor leigo no assunto.
* **Ajuste de Prompt (*Refinamento*):** "Com base nas fontes, explique o Simples Nacional em 3 tópicos diretos e liste os limites de faturamento anual para MEI, ME e EPP em formato de tabela."
* **Resultado Final:** A IA gerou uma tabela clara com os limites de R$ 81 mil, R$ 360 mil e R$ 4,8 milhões, citando a LC 123/2006. A resposta foi direta, deixando claro para qualquer leitor o assunto, sem informações e termos técnicos que prejudiquem o entendimento. 

#### Teste 2: Cruzamento de Regras e Exceções
* **Prompt Inicial:** "Quais atividades não podem ser do Simples Nacional?"
* **Resultado:** Retornou uma lista com as áreas que não podem ser do Simples Nacional, citou apenas a legislação sem fornecer a lei que determina.
* **Ajuste de Prompt (*Refinamento*):** "Consulte a Resolução CGSN nº 140/2018 e liste as 5 principais vedações ao Simples Nacional, indicando o artigo ou trecho da fonte para cada uma."
* **Resultado Final:** Resposta precisa com citações diretas aos trechos dos documentos oficiais carregados. Com a informação de onde tirou a citação direta da lei, sendo preciso na informação de quais eram as vedações a participação do Simples Nacional.

* **As maiores dificuldades encontradas para encontrar as melhores respostas são definir claramente o que se deseja, perguntas rasas e genêricas irão gerar respostas rasas e com conteúdo amplo. Para extrair o máximo do potencial é necessária que saiba o que está procurando e como procurar. Fornecendo o caminho correto a IA fornece respostas claras e diretas as dúvidas, isso pode desfavorecer usuários que não sabem como fazer perguntas e prompts bem extrurados, mas profissionais da área podem se beneficar muito dos resultados encontrados.

* # 📚 Miniguia de Estudo: Simples Nacional e Reforma Tributária

---

## 📝 Resumos Estruturados do Assunto

### 1. Conceito, Gestão e Unificação Tributária
* **Natureza Jurídica:** Criado pela Lei Complementar nº 123/2006, é um regime tributário unificado, favorecido e opcional voltado para Microempresas (ME) e Empresas de Pequeno Porte (EPP).
* **Gestão:** Administrado pelo Comitê Gestor do Simples Nacional (CGSN), vinculado ao Ministério da Fazenda, integrando representantes da União, Estados, DF e Municípios.
* **Mecanismo de Arrecadação:** Consolida até 8 tributos em uma guia única mensal — o Documento de Arrecadação do Simples Nacional (DAS).
* **Tributos Abrangidos:**
  * **Federais:** IRPJ, CSLL, PIS/Pasep, Cofins, IPI e CPP (Contribuição Patronal Previdenciária).
  * **Estadual:** ICMS.
  * **Municipal:** ISS.

### 2. Limites de Faturamento e Enquadramento
* **Microempreendedor Individual (MEI):** Receita bruta anual de até R$ 81.000,00.
* **Microempresa (ME):** Receita bruta anual de até R$ 360.000,00.
* **Empresa de Pequeno Porte (EPP):** Receita bruta anual de R$ 360.000,01 até R$ 4.800.000,00.
* **Sublimite de ICMS e ISS:** Fixado em R$ 3,6 milhões/ano. Faturamentos entre R$ 3,6 milhões e R$ 4,8 milhões mantêm o recolhimento federal no DAS, mas exigem o pagamento do ICMS e ISS "por fora" no regime normal.

| Categoria | Limite de Faturamento Anual |
| :--- | :--- |
| **MEI** | Até R$ 81.000,00 |
| **ME** | Até R$ 360.000,00 |
| **EPP** | De R$ 360.000,01 a R$ 4.800.000,00 |
| **Sublimite ICMS/ISS** | Até R$ 3.600.000,00 |

### 3. Requisitos e Vedações (Resolução CGSN nº 140/2018)
* **Estrutura Societária:** Exclusivamente pessoas físicas residentes no Brasil. Proibida a participação de pessoa jurídica (PJ) no capital social ou a participação da optante em outros CNPJs.
* **Regularidade Fiscal:** Proibida a opção ou permanência de empresas com débitos perante o INSS ou Fazendas Públicas (Federal, Estadual ou Municipal) sem exigibilidade suspensa (Art. 15, inc. V, Resolução CGSN nº 140/2018).
* **Atividades Vedadas:** Instituições financeiras, factoring, geração/transmissão de energia, cessão/locação de mão de obra (salvo exceções do Anexo IV), loteamento/incorporação imobiliária e locação de imóveis próprios.

### 4. Transição e Impactos da Reforma Tributária (IVA Dual)
* **Substituição de Tributos:** O PIS, Cofins, ICMS e ISS serão gradualmente substituídos pela Contribuição sobre Bens e Serviços (CBS - federal) e pelo Imposto sobre Bens e Serviços (IBS - subnacional).
* **Simples Híbrido vs. Puro:**
  * **Regime Puro:** A empresa recolhe IBS e CBS dentro do DAS com alíquota reduzida, porém transfere créditos tributários restritos ao valor efetivamente pago no DAS.
  * **Regime Híbrido:** A empresa opta por recolher IBS e CBS "por fora" do DAS pelo regime regular de débito e crédito, permitindo a geração de créditos integrais para seus clientes (PJ).

---

## 📖 Glossário de Conceitos Fundamentais

* **Anexo do Simples Nacional:** Tabela legislativa (Anexos I a V) que define as alíquotas progressivas e a partilha dos tributos conforme a atividade econômica (comércio, indústria ou serviços).
* **CGSN (Comitê Gestor do Simples Nacional):** Órgão colegiado responsável por regulamentar e gerir os aspectos tributários do Simples Nacional.
* **DAS (Documento de Arrecadação do Simples Nacional):** Guia unificada utilizada para o pagamento mensal consolidado de todos os impostos incidentes no regime.
* **Fator R:** Razão entre a folha de salários dos últimos 12 meses e a receita bruta do mesmo período. Se igual ou superior a 28%, permite que determinadas empresas de serviços tributem pelo Anexo III (alíquotas menores) em vez do Anexo V.
* **IBS/CBS (Imposto/Contribuição sobre Bens e Serviços):** Novos tributos do modelo de IVA Dual criados pela Reforma Tributária que substituirão a tributação tradicional sobre o consumo.
* **RBT12:** Receita Bruta Acumulada nos últimos 12 meses anteriores ao período de apuração, utilizada para calcular a alíquota efetiva do DAS.
* **Split Payment:** Mecanismo do novo sistema tributário em que o recolhimento do imposto é segregado e retido automaticamente na liquidação financeira da transação comercial.
* **Sublimite:** Teto estadual/municipal (R$ 3,6 milhões) que limita a apuração simplificada do ICMS e ISS dentro da guia do DAS.

---

## Prompts Reutilizáveis para Revisão

text
Prompt 1: Verificação de Elegibilidade e CNAE
"Atue como consultor tributário especializado no Simples Nacional. Analise o código CNAE [Inserir Código/Descrição] e informe: 1. Se a atividade é permitida ou impedida no regime segundo a Resolução CGSN nº 140/2018; 2. Em qual Anexo do Simples Nacional ela se enquadra; 3. Se está sujeita à regra do Fator R."

Prompt 2: Comparativo Estratégico (Simples Híbrido vs. Puro)
"Aprofunde a análise da escolha do regime no contexto da Reforma Tributária. Considere uma empresa optante pelo Simples Nacional da categoria B2B com faturamento de R$ [Valor] e custos com insumos de R$ [Valor]. Monte um quadro comparativo mostrando a atratividade comercial e financeira entre manter o IBS/CBS dentro do DAS (Puro) ou recolher por fora (Híbrido)."

Prompt 3: Simulação de Alíquota Efetiva e Fator R
"Com base em uma Receita Bruta acumulada dos últimos 12 meses (RBT12) de R$ [Valor] e uma receita no mês atual de R$ [Valor], calcule a alíquota efetiva do DAS para o Anexo [I a V]. Se aplicável, simule a folha de pagamento mínima necessária para atingir o Fator R de 28%."

## Link do gemini notebook LM: https://notebook.google.com/notebook/28d823c5-584b-41db-94d4-0a06a2ddf7b0
