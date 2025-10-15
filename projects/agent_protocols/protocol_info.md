# Agent Commerce Protocols - Research Report

**Report Date**: October 15, 2025  
**Purpose**: Deep analysis of competing agentic commerce standards for webinar preparation

## Executive Summary

Three major protocol frameworks are competing to standardize how AI agents conduct transactions: Google's AP2 (cryptographic consent), OpenAI/Stripe's ACP (merchant integration), and Visa's Intelligent Commerce (payment infrastructure). Each represents fundamentally different approaches to trust, identity, and consumer control in autonomous transactions.

---

## Protocol Profiles

### 1. Google Agent Payments Protocol (AP2)

**Vision**: Cryptographically-verifiable user consent through "intent mandates"  
**Status**: Work-in-progress, 60+ partners committed  
**License**: Apache 2.0 (open source)

**Technical Architecture**:
- Two-stage approval: "intent mandate" (user tells AI what they want) + "cart mandate" (final purchase approval)
- Built on verifiable credentials and cryptographic signatures for "tamper-proof" proof of user intent
- Extension of Agent2Agent (A2A) protocol and Model Context Protocol (MCP)
- Agent-to-agent negotiation - shopping agent talks to merchant agent, not just merchant APIs
- Payment-agnostic: supports traditional cards, bank transfers, AND stablecoins/cryptocurrency

**Key Partners**: Mastercard, American Express, PayPal, Coinbase, Etsy, Intuit, Stripe, Lightspark, Anthropic, Microsoft, Shopify, Salesforce, Cloudflare, Dell, and 60+ organizations

**Scope**: Both consumer AND enterprise commerce workflows - autonomous procurement, dynamic software licensing, marketplace transactions, complex multi-party transactions

**Critical Gap**: Does NOT solve how shopping agents discover merchant agents - requires new registration/search infrastructure

### 2. OpenAI/Stripe Agentic Commerce Protocol (ACP)

**Vision**: AI agents as checkout facilitators for existing merchant infrastructure  
**Status**: Production-ready with reference implementations  
**License**: Apache 2.0 (open source)

**Technical Architecture**:
- Standard REST API with JSON, HTTPS required
- Merchant implements 5 endpoints: create, update, retrieve, complete, cancel checkout sessions
- Simple token delegation for payment credentials with strict usage constraints
- All monetary amounts in integer minor units (e.g., $4.30 = 430 cents)
- Includes idempotency for safe retries and request signing for security
- Merchants remain system of record for orders and payments

**Key Partners**: OpenAI (ChatGPT integration), Stripe network merchants, Shopify, Salesforce, e-commerce platforms

**Scope**: Consumer checkout focused, works with existing merchant e-commerce infrastructure

**Architecture Advantage**: No technical lock-in, no proprietary protocols, merchant-centric design allows implementation without OpenAI/Stripe dependency

### 3. Visa Intelligent Commerce Platform

**Vision**: AI-ready payment infrastructure with built-in fraud protection  
**Status**: Live production system (launched April 2025)  
**License**: Proprietary API platform

**Technical Architecture - Five Integrated APIs**:
1. **AI-Ready Tokenized Credentials**: Agent-specific payment tokens replacing card details
2. **Authentication with Passkeys**: Identity verification and step-up authentication
3. **Spending Controls & User Instructions**: User-defined limits and conditions
4. **Transaction Enforcement & Commerce Signals**: Real-time authorization controls via VisaNet
5. **AI-Powered Personalization**: Consent-based purchase insights and recommendations

**Scale**: 4.8 billion payment credentials, 150 million merchant locations, 14,500+ financial institutions across 200+ countries

**Key Partners**: Anthropic (MCP integration), IBM, Microsoft, Mistral AI, OpenAI, Perplexity, Samsung, Stripe

**Fraud Protection**: Built on 30 years of Visa AI fraud detection (blocked $40B fraud in 2024)

**Differentiation**: Embeds payment capabilities directly into existing AI agents rather than requiring new protocol layer

---

## Secondary Protocols & Players

### Model Context Protocol (MCP)
- **Creators**: Anthropic (primary), with Visa and Microsoft as key partners
- **Function**: Enterprise payment platforms, agent workflow providers, fintech compliance
- **Integration**: Visa's MCP Server allows direct API connection to Intelligent Commerce

### Mastercard Agent Pay
- **Creators**: Mastercard
- **Partners**: Microsoft, IBM, SRC standards alliance, major banks, retailers
- **Focus**: Enterprise and retail agent payment processing

### Additional Standards
- **x402 Protocol**: Industry-wide open standards (Orium leadership)
- **Agentic Entity Objects (AEO/GEO)**: Orium-led agent identity standards
- **Secure Remote Commerce (SRC) Extensions**: Visa/Mastercard collaborative effort for AI agents

---

## Competitive Analysis

| Aspect | Google AP2 | OpenAI/Stripe ACP | Visa Intelligent Commerce |
|--------|------------|-------------------|---------------------------|
| **Philosophy** | Cryptographic proof of consent | Merchant integration simplicity | Payment infrastructure security |
| **Implementation** | Requires all 4 agent types present | Merchants implement REST API | Direct integration with existing agents |
| **Scope** | Enterprise + consumer workflows | Consumer checkout focused | Payment rails + fraud protection |
| **Discovery** | Unsolved problem | Silent on agent discovery | Works with existing platforms |
| **Readiness** | Work-in-progress | Production ready | Live production system |
| **Interoperability** | Agent-to-agent communication | Merchant API compatibility | Platform-agnostic integration |

---

## Critical Questions for Panel Discussion

### Technical Architecture
1. **Interoperability**: Can these protocols coexist or are they mutually exclusive?
2. **Discovery Problem**: How do agents find merchants/services to transact with?
3. **Identity Standards**: What authentication mechanisms ensure agent legitimacy?
4. **Fraud Prevention**: How do cryptographic proofs compare to network-level fraud detection?

### Business & Legal Implications
1. **Liability Models**: Who is responsible when agents make unauthorized purchases?
2. **Consumer Protection**: How do spending controls and consent mechanisms protect users?
3. **Market Concentration**: Do these standards favor incumbent platforms or enable competition?
4. **Regulatory Compliance**: How do protocols address PCI DSS, GDPR, and financial regulations?

### Ecosystem Dynamics
1. **Adoption Incentives**: What drives merchants to implement multiple protocol standards?
2. **Network Effects**: Which approach creates stronger ecosystem lock-in?
3. **Innovation Barriers**: Do these standards enable or constrain new payment methods?

---

## Key Industry Players by Role

**Protocol Developers**: Google, OpenAI/Stripe, Visa, Anthropic, Mastercard  
**Payment Processors**: PayPal, Coinbase, Lightspark, Braintree, American Express  
**E-commerce Platforms**: Shopify, Salesforce, Etsy  
**Technology Infrastructure**: Microsoft, IBM, Cloudflare, Dell  
**Identity & Security**: Skyfire, Ory, Forter, Basis Theory

---

## Research Gaps & Next Steps Required

### Technical Deep Dives Needed
- Detailed protocol specifications and API documentation analysis
- Security model comparisons and vulnerability assessments  
- Performance and scalability benchmarking
- Cross-protocol integration possibilities

### Business Intelligence Required
- Adoption metrics and merchant implementation timelines
- Revenue sharing models and fee structures
- Competitive positioning and partnership strategies
- Regulatory response and compliance frameworks

### Market Analysis Needed
- Consumer trust and acceptance research
- Developer ecosystem feedback and adoption barriers
- International regulatory landscape assessment
- Use case analysis and success stories

---

**Status**: Foundation research complete. Ready for targeted deep-dive investigation.
**Next Phase**: Execute comprehensive research queries to fill knowledge gaps and prepare panel talking points.