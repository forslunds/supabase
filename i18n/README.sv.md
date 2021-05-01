<p align="center">
<img width="300" src="https://gitcdn.xyz/repo/supabase/supabase/master/web/static/supabase-light.svg"/>
</p>

---

# Supabase

[Supabase](https://supabase.io) är ett öppen källkod alternativ till Firebase. Vi bygger funktionerna i Firebase med hjälp av företagsklassad öppen källkodsverktyg.

- [x] Hosted Postgres Database
- [x] Realtime subscriptions
- [x] Authentication and authorization
- [x] Auto-genererade APIn
- [x] Dashboard
- [x] Utrymme
- [ ] Funktioner (Kommer snart)

## Dokumentation

För komplett dokumentation, besök [supabase.io/docs](https://supabase.io/docs)

## Community & Support

- [Community Forum](https://github.com/supabase/supabase/discussions). Bäst för: hjälp med kodning, diskussioner om bästa strategi för databasen.
- [GitHub Issues](https://github.com/supabase/supabase/issues). Bäst för: Buggar och fel ni upptäcker med Supabase.
- [Email Support](https://supabase.io/docs/support#business-support). Bäst för: problem med er database eller infrastrukturen.

## Status

- [x] Alpha: We are testing Supabase with a closed set of customers
- [x] Öppen Alpha: Anyone can sign up over at [app.supabase.io](https://app.supabase.io). But go easy on us, there are a few kinks.
- [x] Öppen Beta: Stable enough for most non-enterprise use-cases
- [ ] Publikt: Production-ready

We are currently in Public Beta. Watch "releases" of this repo to get notified of major updates.

<kbd><img src="https://gitcdn.link/repo/supabase/supabase/master/web/static/watch-repo.gif" alt="Watch this repo"/></kbd>

---

## Hur det fungerar

Supabase är en kombination av verktyg för öppen källkod. Vi bygger funktionerna i Firebase med hjälp av öppen källkodsprodukter av företagsklass. Om verktygen och gemenskaperna finns, med en MIT, Apache 2 eller motsvarande öppen licens, kommer vi att använda och stödja det verktyget. Om verktyget inte finns, bygger vi och öppnar det själva. Supabase är inte en 1-till-1-mappning av Firebase. Vårt mål är att ge utvecklare en Firebase-liknande utvecklarupplevelse med hjälp av open source-verktyg.

**Current architecture**

Supabase is a [hosted platform](https://app.supabase.io). You can sign up and start using Supabase without installing anything. We are still creating the local development experience - this is now our core focus, along with platform stability.

![Architecture](https://supabase.io/assets/images/supabase-architecture-9050a7317e9ec7efb7807f5194122e48.png)

- [PostgreSQL](https://www.postgresql.org/) is an object-relational database system with over 30 years of active development that has earned it a strong reputation for reliability, feature robustness, and performance.
- [Realtime](https://github.com/supabase/realtime) is an Elixir server that allows you to listen to PostgreSQL inserts, updates, and deletes using websockets. Supabase listens to Postgres' built-in replication functionality, converts the replication byte stream into JSON, then broadcasts the JSON over websockets.
- [PostgREST](http://postgrest.org/) is a web server that turns your PostgreSQL database directly into a RESTful API
- [Storage](https://github.com/supabase/storage-api) provides a RESTful interface for managing Files stored in S3, using Postgres to manage permissions.
- [postgres-meta](https://github.com/supabase/postgres-meta) is a RESTful API for managing your Postgres, allowing you to fetch tables, add roles, and run queries etc.
- [GoTrue](https://github.com/netlify/gotrue) is an SWT based API for managing users and issuing SWT tokens.
- [Kong](https://github.com/Kong/kong) is a cloud-native API gateway.

#### Client libraries

Our client library is modular. Each sub-library is a standalone implementation for a single external system. This is one of the ways we support existing tools.

- **`supabase-{lang}`**: Combines libraries and adds enrichments.
  - `postgrest-{lang}`: Client library to work with [PostgREST](https://github.com/postgrest/postgrest)
  - `realtime-{lang}`: Client library to work with [Realtime](https://github.com/supabase/realtime)
  - `gotrue-{lang}`: Client library to work with [GoTrue](https://github.com/netlify/gotrue)

| Repo                  | Official                                         | Community                                                                                                                                                                                                                  |
| --------------------- | ------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **`supabase-{lang}`** | [`JS`](https://github.com/supabase/supabase-js)  | [`C#`](https://github.com/supabase/supabase-csharp) \| [`Dart`](https://github.com/supabase/supabase-dart) \| [`Python`](https://github.com/supabase/supabase-py) \| `Rust`                                                |
| `postgrest-{lang}`    | [`JS`](https://github.com/supabase/postgrest-js) | [`C#`](https://github.com/supabase/postgrest-csharp) \| [`Dart`](https://github.com/supabase/postgrest-dart) \| [`Python`](https://github.com/supabase/postgrest-py) \| [`Rust`](https://github.com/supabase/postgrest-rs) |
| `realtime-{lang}`     | [`JS`](https://github.com/supabase/realtime-js)  | [`C#`](https://github.com/supabase/realtime-csharp) \| [`Dart`](https://github.com/supabase/realtime-dart) \| [`Python`](https://github.com/supabase/realtime-py) \| `Rust`                                                |
| `gotrue-{lang}`       | [`JS`](https://github.com/supabase/gotrue-js)    | [`C#`](https://github.com/supabase/gotrue-csharp) \| [`Dart`](https://github.com/supabase/gotrue-dart) \| [`Python`](https://github.com/supabase/gotrue-py) \| `Rust`                                                      |

## Translations

- [German](https://github.com/supabase/supabase/blob/master/i18n/README.de.md)
- [Japanese](https://github.com/supabase/supabase/blob/master/i18n/README.jp.md)
- [English](https://github.com/supabase/supabase)
- [Turkish](https://github.com/supabase/supabase/blob/master/i18n/README.tr.md)

---

## Sponsors

[![New Sponsor](https://user-images.githubusercontent.com/10214025/90518111-e74bbb00-e198-11ea-8f88-c9e3c1aa4b5b.png)](https://github.com/sponsors/supabase)
