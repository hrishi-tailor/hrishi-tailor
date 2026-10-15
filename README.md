<h1 align="center">Hi, I'm Hrishi 👋</h1>

<p align="center">
  Computer Science (Co-op) at the University of Waterloo · Founder of <a href="https://tailorcards.com">Tailor Cards</a>

<p align="center">
  <a href="https://hrishitailor.com"><img alt="Website" src="https://img.shields.io/badge/hrishitailor.com-222222?style=flat"></a>
  <a href="https://linkedin.com/in/hrishitailor"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat"></a>
  <a href="mailto:htailor@uwaterloo.ca"><img alt="Email" src="https://img.shields.io/badge/htailor@uwaterloo.ca-EA4335?style=flat&logo=gmail&logoColor=white"></a>

I run a trading-card business and write the software behind it. Most of what I build is backend Java: APIs, data models and the parts that have to be correct when money is involved. I also like building with LLMs, as long as the model never gets the final say on anything that matters.

## Featured projects

### [Tailor Cards](https://github.com/hrishi-tailor/Tailor-Cards) · [tailorcards.com](https://tailorcards.com)

The full-stack store for my card business. The site is live and takes real orders, and the AI buylist is in a private beta with repeat customers.

- **Stack:** Java 21, Spring Boot 4, React 19 + TypeScript, PostgreSQL with Flyway, Stripe Checkout
- **AI buylist:** customers list cards by chat, CSV or phone camera. Claude identifies the cards; every price is calculated in plain Java, and the server rejects any price the model tries to set
- **No double-selling:** optimistic locking plus a stock re-check when the Stripe payment lands, so a one-of-a-kind card can't sell twice
- **Testing:** 350+ unit and integration tests in GitHub Actions, plus a 40-case evaluation suite that checks the assistant against a saved baseline every week

### Matching Engine

A limit order book with price-time priority, plus a market data pipeline that feeds it.

- **Order book:** `TreeMap` price levels with `LinkedHashMap` queues, giving FIFO time priority and O(1) cancels by order ID
- **Concurrency:** one thread owns the book and producers submit through a `BlockingQueue`, so the matching logic needs no locks
- **Market data:** live Coinbase WebSocket feed, rolling VWAP, moving average and volatility, and price-spike detection
- **Event bus:** pluggable, in-memory for local runs or Kafka for separate consumers

## Tools I use

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=springboot&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat&logo=apachekafka&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=flat&logo=stripe&logoColor=white)
![Claude API](https://img.shields.io/badge/Claude_API-D97757?style=flat&logo=anthropic&logoColor=white)
