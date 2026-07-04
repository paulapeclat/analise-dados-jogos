# 🎮📊 Análise de Dados de Jogos na Educação

> Como dados de sessões de criação de jogos podem informar decisões pedagógicas — um caderno Jupyter reproduzível, com dados sintéticos.

**Autora:** [Paula Peclat](https://github.com/paulapeclat) · [APedê Digital](https://paulapeclat.com.br)

Quando crianças criam jogos (GDevelop, Roblox Studio, microStudio...), cada sessão gera vestígios: quanto tempo se envolveram, quantas etapas concluíram, quando pediram ajuda. Este repositório mostra um fluxo simples de análise desses vestígios **a serviço da pedagogia** — não da vigilância.

## O que tem aqui

- [`analise-sessoes.ipynb`](analise-sessoes.ipynb) — caderno completo: carga, exploração, visualização e **leitura pedagógica** dos resultados
- [`dados/sessoes_exemplo.csv`](dados/sessoes_exemplo.csv) — dataset **sintético** de 90 sessões de aula (nenhuma criança real)

## Como rodar

```bash
pip install pandas matplotlib jupyter
jupyter notebook analise-sessoes.ipynb
```

Ou abra direto no navegador pelo próprio GitHub (o notebook renderiza na página).

## Dicionário de dados

| Coluna | Descrição |
|---|---|
| `aluno` | Identificador anônimo (A01, A02...) |
| `idade` | Idade em anos (8–13) |
| `regiao` | Região do Brasil (aulas online) |
| `ferramenta` | Ferramenta da sessão: Code.org, GDevelop, microStudio ou Roblox Studio |
| `sessao_num` | Número da sessão daquele aluno na ferramenta (1ª, 2ª, 3ª...) |
| `minutos` | Duração do engajamento ativo na sessão |
| `etapas_concluidas` | Etapas do roteiro concluídas (0–6) |
| `pediu_ajuda` | 1 se pediu ajuda ao educador durante a sessão |

## ⚖️ Nota ética (leia antes de usar com dados reais)

Dados de crianças são dados **sensíveis por natureza**. Se você adaptar este fluxo para sua turma:

1. **LGPD, art. 14** — o tratamento de dados de crianças exige consentimento específico de ao menos um dos pais/responsável e deve atender ao melhor interesse da criança.
2. **Anonimize na coleta**, não depois — nunca registre nomes, apenas códigos.
3. **Finalidade pedagógica explícita** — analise para ajustar a aula, não para ranquear crianças.
4. **Transparência** — crianças e famílias têm direito de saber o que é registrado e por quê.

## Licença

[MIT](LICENSE) para o código; dados sintéticos em domínio público.
