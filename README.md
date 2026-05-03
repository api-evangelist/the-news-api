# The News API

The News API provides free access to search worldwide news and top stories from over 40,000 sources in 50 countries. Search and filter live and historical articles by keyword, category, language, country, domain, and publication date. Supports advanced boolean search operators and similarity-based discovery.

**Website:** [thenewsapi.com](https://www.thenewsapi.com/)  
**Documentation:** [thenewsapi.com/documentation](https://www.thenewsapi.com/documentation)  
**Sign Up:** [thenewsapi.com/register](https://www.thenewsapi.com/register)

---

## APIs

| API | Description |
|-----|-------------|
| [The News API](https://www.thenewsapi.com/) | Worldwide news search and discovery API |

---

## OpenAPI Specifications

| Spec | File |
|------|------|
| The News API | [openapi/the-news-api-openapi.yml](openapi/the-news-api-openapi.yml) |

**Endpoints:**
- `GET /news/headlines` — Get latest headlines by category
- `GET /news/top` — Get top stories with filtering
- `GET /news/all` — Search full historical archive
- `GET /news/similar/{uuid}` — Find similar articles
- `GET /news/uuid/{uuid}` — Get article by UUID
- `GET /news/sources` — List available sources

---

## Naftiko Capabilities

### Workflow Capabilities

| Workflow | File | Description |
|----------|------|-------------|
| News Monitoring | [capabilities/news-monitoring.yaml](capabilities/news-monitoring.yaml) | Headlines + top stories + archive search + similar articles for news monitoring |

### Shared Per-API Definitions

| API | File |
|-----|------|
| The News API | [capabilities/shared/the-news-api.yaml](capabilities/shared/the-news-api.yaml) |

---

## Spectral Rules

| Ruleset | File |
|---------|------|
| News API Rules | [rules/the-news-api-rules.yml](rules/the-news-api-rules.yml) |

---

## JSON Schemas

| Schema | File |
|--------|------|
| Article | [json-schema/the-news-api-article-schema.json](json-schema/the-news-api-article-schema.json) |

---

## JSON Structure

| Structure | File |
|-----------|------|
| Article | [json-structure/the-news-api-article-structure.json](json-structure/the-news-api-article-structure.json) |

---

## JSON-LD

| Context | File |
|---------|------|
| News API Context | [json-ld/the-news-api-context.jsonld](json-ld/the-news-api-context.jsonld) |

---

## Examples

| Example | File |
|---------|------|
| Top Stories Search | [examples/the-news-api-top-stories-example.json](examples/the-news-api-top-stories-example.json) |

---

## Vocabulary

| Vocabulary | File |
|------------|------|
| News API Vocabulary | [vocabulary/the-news-api-vocabulary.yml](vocabulary/the-news-api-vocabulary.yml) |

---

## Authentication

Pass your API token as a query parameter on every request:

```
?api_token=YOUR_API_TOKEN
```

Obtain a token by registering at [thenewsapi.com/register](https://www.thenewsapi.com/register).

---

## Search Operators

The `search` parameter supports advanced boolean operators:

| Operator | Example | Meaning |
|----------|---------|---------|
| `+` | `+openai +gpt` | AND — both terms required |
| `\|` | `openai\|anthropic` | OR — either term |
| `-` | `AI -crypto` | NOT — exclude term |
| `"..."` | `"machine learning"` | Exact phrase |
| `*` | `artific*` | Prefix wildcard |
| `()` | `(AI\|ML) +regulation` | Grouping |

---

## Maintainers

**FN:** Kin Lane  
**Email:** kin@apievangelist.com

---

*Profile generated 2026-05-03*
