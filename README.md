# 📊 Dataholds – Power BI

## 📌 Descrição
Projeto Power BI **Dataholds**, desenvolvido como parte de um **treinamento prático** com **dados de vendas simulados**, representando cenários reais de uma empresa fictícia de dados corporativos (*Dataholds*).

O projeto foi estruturado em formato **.pbip**, com separação entre *Relatório* e *Modelo Semântico*, permitindo **versionamento, rastreabilidade e controle de alterações** durante o ciclo de desenvolvimento e publicação.

---

## 🗂 Estrutura do Repositório
- **Dataholds.Report/** → Relatórios (páginas, visuais e layouts).
- **Dataholds.SemanticModel/** → Modelo semântico (medidas DAX, relacionamentos e pastas de medidas).
- **Dataholds.pbip** → Arquivo principal que referencia o relatório e o modelo semântico.
- **.gitignore** → Regras de versionamento e exclusão de arquivos desnecessários.
- **README.md** → Documento de referência e boas práticas do projeto.

---

## 🔄 Como Modificar (Branch de Nova Modificação)
1. Criar sempre uma *branch nova* com o nome da modificação:
   ```bash
   git checkout -b ajuste-margem-lucro
   ```
2. Realizar as alterações necessárias no `.pbip`, `Report` ou `SemanticModel`.
3. *Publicar primeiro em ambiente DEV* no Power BI Service.
4. Validar em DEV se:
   - As medidas e cálculos estão corretos.
   - Os filtros e visuais estão funcionando adequadamente.
   - Não houve impacto em outras páginas ou componentes.
5. Após a validação, abrir um *Pull Request* para merge na branch `main`.
6. Atualizar a seção **Última Modificação** deste README com data, responsável e breve descrição da alteração.

---

## 📝 Padrão de Commits

Os commits devem seguir um padrão claro, descritivo e consistente:

**Formato:**
```
[tipo]: descrição breve da alteração
```

**Tipos recomendados:**
- **feat** → nova funcionalidade (ex.: nova medida, nova página)
- **fix** → correção (ex.: ajuste em medida, filtro ou cálculo)
- **refactor** → melhoria sem alteração de resultado (ex.: renomeação, reorganização)
- **chore** → manutenção do projeto (ex.: ajustes em README, estrutura, documentação)
- **style** → alterações visuais (ex.: layout, cores, tipografia)

**Exemplos:**
```bash
git commit -m "fix: corrigida medida Margem de Lucro no modelo Dataholds"
git commit -m "feat: adicionada análise de Vendas por Região no relatório principal"
git commit -m "refactor: reorganização das pastas em Fatos e Dimensões"
git commit -m "chore: atualização do README com checklist de publicação"
```

---

## ⚠️ Checklist Antes de Publicar

Antes de publicar no ambiente **DEV** ou aprovar merge para **main**, certifique-se de:

- ✅ RLS (Row Level Security) configurado corretamente.
- ✅ Visuais seguem o padrão de **identidade visual da Dataholds**.
- ✅ Resultados conferidos e validados com as fontes simuladas.
- ✅ Colunas de data estão no tipo **"Data"** (sem texto ou número).
- ✅ Filtros sem **valores em branco** inesperados.
- ✅ Nenhuma **medida/coluna não utilizada** permanece no modelo.
- ✅ Nomenclatura das medidas é **clara e organizada em pastas**.
- ✅ Separação correta de **Fatos** e **Dimensões**.
- ✅ Tipagem das colunas coerente (numérico, texto, data, booleano).
- ✅ ETL realizado preferencialmente **no banco de dados**, não no Power BI.
- ✅ **Query Folding** ativo nas transformações (quando aplicável).

---

## 🔖 Controle de Versões (Tags)

Após validar que a versão em **desenvolvimento** está correta, será criada uma **tag** para registrar o **nível atual do projeto** — seja uma versão estável, de melhoria ou intermediária.

As tags permitem **controlar a evolução do projeto** e, se necessário, **retornar para uma versão anterior** com segurança e rastreabilidade.

### ⚙️ Exemplo de Uso
```bash
git tag -a v1.0.0 -m "versão estável inicial do projeto"
git push origin v1.0.0
```

> 🔹 As tags devem ser criadas **após validação completa** e representam marcos importantes do ciclo de desenvolvimento.

