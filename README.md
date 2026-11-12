# Awesome-SaaS-Business-Performance-Metrics

# Awesome SaaS & Business Performance Metrics

> A curated list of top SaaS and Business Performance Metrics platforms — both SaaS/Hosted commercial solutions and open-source alternatives for tracking MRR, ARR, churn, and the metrics that define business health.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [ChartMogul](#chartmogul)
  - [Baremetrics](#baremetrics)
  - [ProfitWell Metrics](#profitwell-metrics)
  - [Stripe Sigma](#stripe-sigma)
  - [Databox](#databox)
  - [Geckoboard](#geckoboard)
- [Open-Source Software](#-open-source-software)
  - [SaaSDashboard (bhattsaurya16)](#saasdashboard-bhattsaurya16)
  - [Revenut](#revenut)
  - [MRR Growth Analytics Dashboard](#mrr-growth-analytics-dashboard)
  - [SaaSBoard](#saasboard)
  - [ChurnLens](#churnlens)
  - [Socketkit](#socketkit)
  - [Chartbrew](#chartbrew)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted SaaS and Business Performance Metrics platforms. These are not open-source but are included as reference points for feature comparison.

### ChartMogul
**Type:** Subscription analytics and CRM with standardized SaaS metrics  
ChartMogul connects to billing systems and consolidates subscription revenue, product usage, and marketing data into one platform, standardizing how metrics are calculated so every team works from the same numbers. Built-in reports cover MRR movements, churn, customer lifetime value, cohort retention, and more, with custom dashboards and the ability to send metrics to Slack, HubSpot, or data warehouses. It also functions as a CRM, giving sales and success teams a revenue-aware view of customers. Pricing scales with tracked revenue rather than seats.

### Baremetrics
**Type:** Subscription analytics with payment recovery add-ons  
Baremetrics tracks over 28 subscription metrics including MRR, ARR, churn, upgrades, and downgrades, priced on tracked revenue rather than per seat. The free tier covers up to $180K ARR, with paid plans scaling to $409/month for larger businesses. Optional add-ons include **Payment Recovery** ($129/month or 10% of recovered revenue) and **Cancellation Insights** ($129/month) for churn feedback collection. Known for clean dashboards and accessible pricing for early-stage SaaS.

### ProfitWell Metrics
**Type:** Free subscription analytics with benchmarking  
ProfitWell Metrics is **free forever, regardless of business size**, offering growth, revenue, retention, and churn trends, unit economics, cohorts, and benchmarks from 15,000+ subscription companies. Setup is quick (5 minutes), with native integrations and APIs, enrichment via Clearbit and FullContact, and a mobile app with intelligent alerting. Paid add-ons include Retain (churn recovery), Recognized (revenue recognition), and Price Intelligently (pricing strategy). The free tier makes it uniquely accessible for SaaS businesses at any stage.

### Stripe Sigma
**Type:** SQL-based analytics layer within Stripe  
Stripe Sigma is a SQL-powered analytics layer built into the Stripe Dashboard, enabling custom queries against live payment and billing data. It includes pre-built templates for common SaaS questions (MRR trends, active subscriptions, churned customers, failed payments) and an **AI Assistant** that generates SQL from plain English. Sigma allows unlimited customization without fixed dashboards, with a 30-day free trial before paid subscription. **Trade-off:** Requires SQL knowledge for non-template queries, and it is limited to Stripe data only.

### Databox
**Type:** Business dashboard and reporting platform  
Databox connects to hundreds of data sources (including Stripe, HubSpot, and Google Analytics) to build customizable dashboards and reports. It is a general-purpose business analytics platform rather than a dedicated SaaS metrics tool, but it is commonly used by SaaS teams to visualize MRR and churn alongside other KPIs.

### Geckoboard
**Type:** Real-time KPI dashboard for teams  
Geckoboard provides real-time dashboards that pull from various data sources, designed to be displayed on office TVs for team visibility. It supports Stripe and other SaaS tools, making it useful for keeping MRR and churn visible to the whole team.

---

## 🟩 Open-Source Software

Self-hosted, community-driven SaaS and Business Performance Metrics tools. The open-source ecosystem spans **AI-powered analytics dashboards**, **Stripe forecasting apps**, **MRR tracking boilerplates**, and **self-hosted metric calculators**.

### SaaSDashboard (bhattsaurya16)
**Stack:** Python / Streamlit / Gemini AI | **License:** Open Source (per GitHub)  
SaaSDashboard is an AI-powered analytics dashboard for SaaS customer data and general business datasets, offering churn, MRR, cohort retention, revenue loss, and quant forecasts [citation:1]. It supports flexible data input (default CSV, file upload of CSV/Excel, or SQL database query) and includes a generic dataset explorer for non-SaaS schemas. **Gemini AI insights** generate executive summaries, risks, opportunities, and action plans [citation:1]. Deploys via Streamlit Community Cloud, Render, or Docker.  
**Best for:** Teams wanting a ready-to-run Streamlit dashboard with AI-generated insights from their CSV or database data, particularly those comfortable with Python and Google Gemini.

### Revenut
**Stack:** FastAPI / Python / React Native (Expo) | **License:** Apache 2.0  
Revenut is a web + mobile (PWA) app with Stripe integration for forecasting SaaS revenue, built as a lightweight open-source alternative to Stripe's mobile app after the developer experienced fraudulent card testing polluting revenue reports [citation:6]. Key features include excluding disputed and refunded transactions for accurate reporting, calculating **unrealized ("paper") revenue** from trialing customers and upcoming invoices, and calculating realized revenue from paid invoices [citation:6]. Authentication uses Stripe's browser-based OAuth for secure login.  
**Best for:** Freemium SaaS owners wanting accurate revenue forecasting that excludes fraudulent transactions, with mobile access via PWA, accepting that it is Stripe-specific.

### MRR Growth Analytics Dashboard
**Stack:** React 19 / Express 5 / PostgreSQL / Drizzle ORM | **License:** Open Source (boilerplate)  
A full-stack TypeScript monorepo designed for indie developers and solo founders to track MRR, customer growth, churn, refunds, and other key business metrics without enterprise complexity [citation:7]. Features include tracking monthly recurring revenue, monitoring customer acquisition and churn, visualizing revenue trends with interactive charts, configuring growth targets, and viewing automatically calculated SaaS KPIs (Net MRR Growth Rate, Churn Rate, ARPU) [citation:7]. The backend exposes a REST API with full CRUD for monthly metrics and a summary endpoint for calculated KPIs. Includes seed data for immediate realistic display.  
**Best for:** Indie developers and solo founders wanting a clean, modern MRR dashboard boilerplate they can extend, particularly those comfortable with the React/Express/PostgreSQL stack.

### SaaSBoard
**Stack:** React / Vite / Tailwind CSS / Radix UI | **License:** Open Source (per GitHub)  
SaaSBoard is a free, open-source SaaS dashboard template built with React and Tailwind, providing pre-built layouts for metrics visualization, reports, billing management, and team settings [citation:2]. It is a **template** rather than a working analytics backend—it provides the UI components and pages for tracking KPIs, managing SaaS metrics, and designing professional dashboards, but does not include data ingestion or calculation logic [citation:2].  
**Best for:** Developers wanting a polished, ready-made React dashboard UI to customize and connect to their own metrics backend, rather than a complete analytics solution.

### ChurnLens
**Stack:** Python / Docker | **License:** Source-available (COCL v1.0)  
ChurnLens is a self-hosted tool that calculates MRR, customer churn rate, and LTV from a CSV file or Stripe data, running entirely on your own computer or server with no account, third-party service, or monthly fee . It is single-purpose, scriptable, CI-friendly, and callable by AI agents over MCP . **Important licensing note:** Source-available under the Cognis Open Collaboration License (COCL) v1.0 — free for personal, internal-evaluation, research, and educational use, but **commercial/production use requires a license** .  
**Best for:** Founders and finance teams wanting a simple, self-hosted CSV/Stripe metric calculator without a SaaS subscription, accepting source-available licensing with commercial restrictions.

### Socketkit
**Stack:** Go / gRPC | **License:** Open Source (per GitHub)  
Socketkit is a free open-source alternative to ChartMogul, SensorTower, Google Analytics, and Mixpanel, focused on mobile application developers [citation:10]. It includes an **AppStore Subscription Tracking** worker with built-in integration with AppStore Connect that retrieves and analyzes daily payments, storing data normalized with currency conversion and providing reports for **Monthly Recurring Revenue (MRR)**, Average Revenue Per User (ARPU), and Daily Revenue [citation:10]. It also includes competitor tracking (AppStore metadata and reviews) and real-time notifications. **Note:** The project has not been updated since 2022—evaluate maintenance status before adoption [citation:10].  
**Best for:** Mobile app developers wanting open-source AppStore subscription analytics with MRR and ARPU tracking, accepting that the project is dormant and iOS-focused.

### Chartbrew
**Stack:** Node.js / React / PostgreSQL | **License:** Open Source (per GitHub)  
Chartbrew is an open-source web application that connects directly to databases and APIs to create charts and dashboards, with a chart builder, editable dashboards, embeddable charts, query/request editor, and team capabilities . It includes **dashboard templates** with charts already prepared for Simple Analytics, **ChartMogul**, and Mailgun, or you can create custom templates and replicate them across multiple dashboards . While not a dedicated SaaS metrics tool, it can be used to build custom MRR/ARR dashboards from your billing data.  
**Best for:** Teams wanting a flexible, open-source dashboard builder that can connect to Stripe or databases to create custom SaaS metric visualizations, accepting that metric logic must be defined yourself.

---

## 📊 Comparison at a Glance

| Software | License | Stack | MRR/ARR | Churn | AI Insights | Self-Hosted | Best For |
|----------|---------|-------|---------|-------|-------------|-------------|----------|
| **ChartMogul** | Proprietary | Cloud | ✅ | ✅ | ❌ | ❌ | Cross-system metric consistency |
| **Baremetrics** | Proprietary | Cloud | ✅ | ✅ | ❌ | ❌ | Accessible core analytics |
| **ProfitWell** | Proprietary | Cloud | ✅ | ✅ | ❌ | ❌ | Free + benchmarks |
| **Stripe Sigma** | Proprietary | Cloud | ✅ SQL | ✅ | ✅ SQL assistant | ❌ | Stripe-native SQL flexibility |
| **SaaSDashboard** | Open Source | Streamlit | ✅ | ✅ | ✅ Gemini | ✅ | AI insights from CSV/DB |
| **Revenut** | Apache 2.0 | FastAPI/React Native | ✅ | (Forecast) | ❌ | ✅ | Stripe revenue forecasting |
| **MRR Growth Dashboard** | Open Source | React/Express/Postgres | ✅ | ✅ | ❌ | ✅ | Indie dev MRR boilerplate |
| **SaaSBoard** | Open Source | React/Tailwind | (UI only) | (UI only) | ❌ | ✅ | Dashboard UI template |
| **ChurnLens** | Source-available | Python | ✅ | ✅ | ❌ | ✅ | CSV/Stripe CLI calculator |
| **Socketkit** | Open Source | Go/gRPC | ✅ | (Check) | ❌ | ✅ | AppStore subscription analytics |
| **Chartbrew** | Open Source | Node.js/React | (Custom) | (Custom) | ❌ | ✅ | Custom dashboard builder |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source SaaS or Business Performance Metrics tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source (or clearly note if it is source-available but not OSI-approved, as with ChurnLens). Note that the open-source ecosystem **splits** between **AI-powered analytics dashboards** (SaaSDashboard with Gemini insights [citation:1]), **Stripe-specific forecasting apps** (Revenut for accurate revenue excluding fraud [citation:6]), **MRR tracking boilerplates** (MRR Growth Analytics Dashboard for indie devs [citation:7]), **UI templates** (SaaSBoard [citation:2]), **self-hosted metric calculators** (ChurnLens ), and **flexible dashboard builders** (Chartbrew ). No single open-source project replicates the full breadth of ChartMogul or ProfitWell, but SaaSDashboard offers the most complete working analytics with AI insights, while Revenut and the MRR Growth Dashboard provide focused, Stripe-centric solutions for specific use cases.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
