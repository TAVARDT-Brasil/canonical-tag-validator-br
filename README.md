# Validador e Auditor de Tag Canonica e Consolidacao de URLs

[![Validador Tag Canonica](https://img.shields.io/badge/TAVARDT-Canonical-5b3cf5.svg)](https://tools.tavardt.com/br/validador-tag-canonica/)
[![Jurisdicao](https://img.shields.io/badge/Jurisdicao-Brasil-00C853.svg)](https://ag.tavardt.com/br/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)

Auditoria de tags canonicas, deteccao de duplicidade, rotas absolutas e prevencao de canibalizacao de indexacao.

Desenvolvido e mantido pela divisao de arquitetura semantica e infraestrutura de busca da **[TAVARDT Brasil](https://ag.tavardt.com/br/)**.

---

## Capacidades de Auditoria de Tag Canonica

* **Inspecao de Declaracao Canonica**: Identifica a presenca de tags `<link rel="canonical">` no `<head>` HTML e cabecalhos HTTP `Link`.
* **Deteccao de Duplicidade de Tags**: Sinaliza erros graves de multiplas tags canonicas conflitantes em um unico documento.
* **Validacao de URLs Absolutas vs Relativas**: Garante que o apontamento utilize caminhos absolutos com protocolo HTTPS completo.
* **Verificacao de Resposta do Destino**: Checa se a URL canonica de destino retorna codigo de status HTTP 200 OK, prevenindo apontamento para paginas 404, 301 ou 500.
* **Indice de Consolidacao e Higiene de URL**: Pontuacao tecnica quantitativa de 0 a 100 com alertas classificados por severidade.

---

## Instalacao e Execucao

Requer Python 3.8 ou superior sem necessidade de pacotes externos adicionais.

```bash
git clone https://github.com/TAVARDT-Brasil/canonical-tag-validator-br.git
cd canonical-tag-validator-br
python canonical_validator.py https://empresa.com.br
```

Para gerar a saida em formato estruturado JSON para esteiras de integracao continua:

```bash
python canonical_validator.py https://empresa.com.br --json
```

---

## Diagnostico Completo na Web

Para auditoria visual aprofundada de consolidacao canonica:

* **[Validador de Tag Canonica Oficial](https://tools.tavardt.com/br/validador-tag-canonica/)**
* **[Portal Corporativo TAVARDT Brasil](https://ag.tavardt.com/br/)**

---

## Consultoria em Arquitetura de Indexacao e SEO

Para estruturacao avancada de clusters de paginas e conformidade com Diretrizes de SEO Tecnico e W3C, contate a equipe da **[TAVARDT Brasil](https://ag.tavardt.com/br/contato/)**.
