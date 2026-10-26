Here is a full premium landing page for MATRIX AI Content Engine, ready to use inside a React app.

This landing page is built for:
- SaaS conversion
- polished AI brand feel
- high-trust product marketing
- premium dark theme
- CTA-focused layout

You can place it in:
- frontend/src/pages/LandingPage.tsx

and wire it in App.tsx as the first screen or as the default public page.

Landing page code

```tsx
import React from "react";

const metrics = [
  { label: "Workspaces", value: "12.4k+" },
  { label: "AI generated assets", value: "3.2M" },
  { label: "Avg. time saved", value: "8.4x" },
  { label: "Adopted by teams", value: "99.7%" }
];

const features = [
  {
    title: "Workspace-bound generation",
    text: "Create content securely inside each workspace with role-aware permissions and usage tracking."
  },
  {
    title: "Multi-format AI engine",
    text: "Generate product descriptions, reviews, SEO posts, social media copy, and ad variants in one platform."
  },
  {
    title: "Lightning-fast workflows",
    text: "Turn product data into quality marketing content with a single click and streamlined approval flows."
  },
  {
    title: "Usage-aware billing",
    text: "Track generation usage per workspace and connect billing logic directly to your consumption model."
  }
];

const steps = [
  "Connect your product catalog",
  "Choose a content format",
  "Generate and review output",
  "Publish or automate"
];

const testimonials = [
  {
    quote:
      "MATRIX helped us ship localized product copy and social assets across every campaign in half the time.",
    author: "Alicia R.",
    role: "Growth Lead"
  },
  {
    quote:
      "The workspace-bound setup gives our teams clean permissions and the AI output feels premium out of the box.",
    author: "Daniel K.",
    role: "Marketing Ops"
  }
];

const pricingPlans = [
  {
    name: "Starter",
    price: "$29",
    description: "For solo operators and early teams",
    features: ["5 workspaces", "Unlimited product drafts", "Basic SEO prompts", "Email support"]
  },
  {
    name: "Growth",
    price: "$99",
    description: "For scaling ecommerce and marketing teams",
    features: ["Unlimited workspaces", "Automation workflows", "Advanced templates", "Priority support"],
    featured: true
  },
  {
    name: "Enterprise",
    price: "Custom",
    description: "For multi-team operations and custom governance",
    features: ["Custom role policies", "SSO / governance", "Advanced automations", "White-glove onboarding"]
  }
];

const styles = {
  page: {
    background: "#0b1020",
    color: "#f8fafc",
    minHeight: "100vh",
    fontFamily: "Inter, system-ui, sans-serif"
  },
  container: {
    maxWidth: 1200,
    margin: "0 auto",
    padding: "0 24px"
  },
  nav: {
    display: "flex",
    alignItems: "center",
    justifyContent: "space-between",
    padding: "24px 0",
    gap: 20
  },
  logo: {
    display: "flex",
    alignItems: "center",
    gap: 12,
    fontWeight: 800,
    fontSize: 20,
    letterSpacing: 0.5
  },
  logoMark: {
    width: 28,
    height: 28,
    borderRadius: 10,
    background: "linear-gradient(135deg, #7c3aed, #3b82f6)",
    display: "flex",
    alignItems: "center",
    justifyContent: "center",
    fontSize: 16,
    boxShadow: "0 10px 25px rgba(124, 58, 237, 0.45)"
  },
  navLinks: {
    display: "flex",
    gap: 22,
    color: "#cbd5e1",
    fontSize: 15
  },
  navAction: {
    display: "flex",
    alignItems: "center",
    gap: 12
  },
  ghostButton: {
    background: "transparent",
    border: "1px solid rgba(148, 163, 184, 0.35)",
    color: "#f8fafc",
    borderRadius: 12,
    padding: "10px 16px",
    cursor: "pointer",
    fontWeight: 600
  },
  primaryButton: {
    background: "linear-gradient(135deg, #7c3aed, #3b82f6)",
    border: "none",
    color: "#fff",
    borderRadius: 12,
    padding: "12px 18px",
    fontWeight: 700,
    cursor: "pointer",
    boxShadow: "0 15px 30px rgba(124, 58, 237, 0.4)"
  },
  hero: {
    padding: "42px 0 50px",
    display: "grid",
    gridTemplateColumns: "1.2fr 0.8fr",
    gap: 28,
    alignItems: "center"
  },
  heroText: {
    maxWidth: 620
  },
  eyebrow: {
    display: "inline-flex",
    padding: "8px 12px",
    borderRadius: 999,
    border: "1px solid rgba(124, 58, 237, 0.35)",
    background: "rgba(124, 58, 237, 0.12)",
    color: "#d8b4fe",
    fontSize: 12,
    letterSpacing: "0.08em",
    textTransform: "uppercase" as const,
    fontWeight: 700
  },
  heading: {
    fontSize: "clamp(2.8rem, 5vw, 5rem)",
    lineHeight: 1.02,
    margin: "18px 0 18px",
    letterSpacing: "-0.06em"
  },
  subheading: {
    color: "#cbd5e1",
    lineHeight: 1.7,
    fontSize: 18,
    maxWidth: 620
  },
  heroActions: {
    display: "flex",
    gap: 14,
    marginTop: 28,
    flexWrap: "wrap"
  },
  heroPanel: {
    background: "linear-gradient(180deg, rgba(17, 24, 39, 0.8), rgba(15, 23, 42, 0.95))",
    border: "1px solid rgba(148, 163, 184, 0.22)",
    borderRadius: 24,
    padding: 18,
    boxShadow: "0 25px 60px rgba(15, 23, 42, 0.4)"
  },
  previewBox: {
    background: "linear-gradient(180deg, rgba(15, 23, 42, 0.95), rgba(18, 24, 38, 1))",
    border: "1px solid rgba(148, 163, 184, 0.18)",
    borderRadius: 18,
    padding: 18
  },
  chipRow: {
    display: "flex",
    gap: 10,
    flexWrap: "wrap",
    marginTop: 14
  },
  chip: {
    borderRadius: 999,
    padding: "7px 10px",
    background: "#0f172a",
    border: "1px solid rgba(148, 163, 184, 0.2)",
    color: "#cbd5e1",
    fontSize: 12,
    fontWeight: 600
  },
  section: {
    padding: "72px 0"
  },
  sectionTitle: {
    fontSize: 38,
    letterSpacing: "-0.04em",
    margin: 0
  },
  sectionLead: {
    color: "#cbd5e1",
    maxWidth: 620,
    lineHeight: 1.7,
    marginTop: 12
  },
  metricsGrid: {
    display: "grid",
    gridTemplateColumns: "repeat(4, minmax(0, 1fr))",
    gap: 18,
    marginTop: 26
  },
  metricCard: {
    background: "rgba(15, 23, 42, 0.8)",
    border: "1px solid rgba(148, 163, 184, 0.15)",
    borderRadius: 18,
    padding: 18
  },
  featureGrid: {
    display: "grid",
    gridTemplateColumns: "repeat(2, minmax(0, 1fr))",
    gap: 18,
    marginTop: 32
  },
  featureCard: {
    background: "rgba(15, 23, 42, 0.76)",
    border: "1px solid rgba(148, 163, 184, 0.18)",
    borderRadius: 20,
    padding: 24
  },
  featureIcon: {
    width: 42,
    height: 42,
    borderRadius: 12,
    background: "linear-gradient(135deg, rgba(124, 58, 237, 0.22), rgba(59, 130, 246, 0.22))",
    display: "flex",
    alignItems: "center",
    justifyContent: "center",
    marginBottom: 18,
    color: "#d8b4fe",
    fontWeight: 800
  },
  processGrid: {
    display: "grid",
    gridTemplateColumns: "repeat(4, minmax(0, 1fr))",
    gap: 18,
    marginTop: 26
  },
  processStep: {
    background: "rgba(15, 23, 42, 0.8)",
    border: "1px solid rgba(148, 163, 184, 0.18)",
    borderRadius: 18,
    padding: 18
  },
  numberBadge: {
    width: 34,
    height: 34,
    borderRadius: 10,
    display: "flex",
    alignItems: "center",
    justifyContent: "center",
    background: "linear-gradient(135deg, #7c3aed, #3b82f6)",
    fontWeight: 800,
    marginBottom: 16
  },
  testimonialGrid: {
    display: "grid",
    gridTemplateColumns: "repeat(2, minmax(0, 1fr))",
    gap: 18,
    marginTop: 32
  },
  testimonialCard: {
    background: "rgba(15, 23, 42, 0.8)",
    border: "1px solid rgba(148, 163, 184, 0.18)",
    borderRadius: 18,
    padding: 20
  },
  pricingGrid: {
    display: "grid",
    gridTemplateColumns: "repeat(3, minmax(0, 1fr))",
    gap: 18,
    marginTop: 32
  },
  priceCard: {
    background: "rgba(15, 23, 42, 0.8)",
    border: "1px solid rgba(148, 163, 184, 0.18)",
    borderRadius: 20,
    padding: 22
  },
  priceFeatured: {
    borderColor: "rgba(124, 58, 237, 0.7)",
    boxShadow: "0 22px 50px rgba(124, 58, 237, 0.18)"
  },
  cta: {
    background: "linear-gradient(135deg, rgba(124, 58, 237, 0.18), rgba(59, 130, 246, 0.12))",
    border: "1px solid rgba(124, 58, 237, 0.25)",
    borderRadius: 28,
    padding: "50px 24px",
    textAlign: "center" as const,
    marginTop: 20
  },
  footer: {
    padding: "28px 0 56px",
    color: "#9aa9ba"
  }
};

export default function LandingPage() {
  return (
    <div style={styles.page}>
      <div style={styles.container}>
        <nav style={styles.nav}>
          <div style={styles.logo}>
            <div style={styles.logoMark}>M</div>
            <span>MATRIX</span>
          </div>

          <div style={styles.navLinks}>
            <span>Platform</span>
            <span>Features</span>
            <span>Pricing</span>
            <span>Resources</span>
          </div>

          <div style={styles.navAction}>
            <button style={styles.ghostButton}>Log in</button>
            <button style={styles.primaryButton}>Get started</button>
          </div>
        </nav>

        <header style={styles.hero}>
          <div style={styles.heroText}>
            <div style={styles.eyebrow}>AI content engine</div>
            <h1 style={styles.heading}>
              Turn product data into conversion-winning content.
            </h1>
            <p style={styles.subheading}>
              MATRIX helps teams generate product descriptions, SEO content, reviews,
              social posts, and ads—inside secure workspace-scoped environments built for scale.
            </p>

            <div style={styles.heroActions}>
              <button style={styles.primaryButton}>Start free</button>
              <button style={styles.ghostButton}>Book a demo</button>
            </div>

            <div style={styles.chipRow}>
              <span style={styles.chip}>SEO</span>
              <span style={styles.chip}>Social</span>
              <span style={styles.chip}>Ads</span>
              <span style={styles.chip}>Reviews</span>
              <span style={styles.chip}>Automation</span>
            </div>
          </div>

          <div style={styles.heroPanel}>
            <div style={styles.previewBox}>
              <div
                style={{
                  display: "flex",
                  justifyContent: "space-between",
                  alignItems: "center",
                  marginBottom: 14
                }}
              >
                <div>
                  <div style={{ color: "#94a3b8", fontSize: 12, letterSpacing: "0.08em", textTransform: "uppercase" }}>
                    Generated result
                  </div>
                  <strong style={{ fontSize: 18 }}>Wireless Headphones</strong>
                </div>
                <div
                  style={{
                    background: "rgba(34, 197, 94, 0.12)",
                    border: "1px solid rgba(34, 197, 94, 0.25)",
                    borderRadius: 999,
                    padding: "6px 10px",
                    color: "#86efac",
                    fontSize: 12,
                    fontWeight: 700
                  }}
                >
                  Ready to publish
                </div>
              </div>

              <div
                style={{
                  background: "#0b1020",
                  borderRadius: 14,
                  border: "1px solid rgba(148, 163, 184, 0.18)",
                  padding: 18
                }}
              >
                <div style={{ fontSize: 28, fontWeight: 800, marginBottom: 12 }}>
                  Premium Wireless Audio, Redefined
                </div>
                <p style={{ lineHeight: 1.7, color: "#cbd5e1", margin: 0 }}>
                  Experience rich, immersive sound with deep bass, all-day battery life, and crystal-clear calls.
                  Designed for focus, comfort, and everyday performance.
                </p>

                <div style={styles.chipRow}>
                  <span style={styles.chip}>noise cancelling</span>
                  <span style={styles.chip}>bluetooth</span>
                  <span style={styles.chip}>audio</span>
                </div>
              </div>
            </div>
          </div>
        </header>

        <section style={styles.section}>
          <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-end", gap: 20, flexWrap: "wrap" }}>
            <div>
              <h2 style={styles.sectionTitle}>Built for AI-powered marketing teams</h2>
            </div>
          </div>

          <div style={styles.metricsGrid}>
            {metrics.map((item) => (
              <div key={item.label} style={styles.metricCard}>
                <div style={{ fontSize: 30, fontWeight: 800, marginBottom: 8 }}>{item.value}</div>
                <div style={{ color: "#94a3b8", fontSize: 14 }}>{item.label}</div>
              </div>
            ))}
          </div>
        </section>

        <section style={styles.section}>
          <h2 style={styles.sectionTitle}>Everything your content engine needs</h2>
          <p style={styles.sectionLead}>
            From product data to SEO content to social post generation, MATRIX gives your team a single AI workspace for marketing execution.
          </p>

          <div style={styles.featureGrid}>
            {features.map((feature) => (
              <div key={feature.title} style={styles.featureCard}>
                <div style={styles.featureIcon}>✦</div>
                <h3 style={{ margin: "0 0 10px", fontSize: 22 }}>{feature.title}</h3>
                <p style={{ margin: 0, color: "#cbd5e1", lineHeight: 1.7 }}>{feature.text}</p>
              </div>
            ))}
          </div>
        </section>

        <section style={styles.section}>
          <h2 style={styles.sectionTitle}>From product data to published content in 4 steps</h2>

          <div style={styles.processGrid}>
            {steps.map((step, index) => (
              <div key={step} style={styles.processStep}>
                <div style={styles.numberBadge}>{index + 1}</div>
                <p style={{ margin: 0, fontSize: 18, fontWeight: 600 }}>{step}</p>
              </div>
            ))}
          </div>
        </section>

        <section style={styles.section}>
          <h2 style={styles.sectionTitle}>Loved by modern growth teams</h2>

          <div style={styles.testimonialGrid}>
            {testimonials.map((item) => (
              <div key={item.author} style={styles.testimonialCard}>
                <div style={{ color: "#e2e8f0", fontSize: 18, lineHeight: 1.7, marginBottom: 22 }}>
                  “{item.quote}”
                </div>
                <div style={{ fontWeight: 700 }}>{item.author}</div>
                <div style={{ color: "#94a3b8", fontSize: 14 }}>{item.role}</div>
              </div>
            ))}
          </div>
        </section>

        <section style={styles.section}>
          <h2 style={styles.sectionTitle}>Simple pricing for every stage</h2>

          <div style={styles.pricingGrid}>
            {pricingPlans.map((plan) => (
              <div
                key={plan.name}
                style={{
                  ...styles.priceCard,
                  ...(plan.featured ? styles.priceFeatured : {})
                }}
              >
                <div style={{ color: "#d8b4fe", fontSize: 13, letterSpacing: "0.08em", textTransform: "uppercase", fontWeight: 700 }}>
                  {plan.name}
                </div>
                <div style={{ margin: "16px 0 12px", fontSize: 38, fontWeight: 800 }}>
                  {plan.price}
                  <span style={{ fontSize: 16, color: "#94a3b8" }}>{plan.price === "Custom" ? "" : "/mo"}</span>
                </div>
                <div style={{ color: "#cbd5e1", marginBottom: 18 }}>{plan.description}</div>

                <ul style={{ listStyle: "none", margin: 0, padding: 0, color: "#e2e8f0", display: "grid", gap: 10 }}>
                  {plan.features.map((feature) => (
                    <li key={feature}>✓ {feature}</li>
                  ))}
                </ul>

                <button
                  style={{
                    ...styles.primaryButton,
                    width: "100%",
                    marginTop: 18,
                    ...(plan.featured ? {} : { opacity: 0.9 })
                  }}
                >
                  {plan.featured ? "Start free trial" : "Choose plan"}
                </button>
              </div>
            ))}
          </div>
        </section>

        <section style={styles.section}>
          <div style={styles.cta}>
            <div style={{ fontSize: 12, letterSpacing: "0.08em", textTransform: "uppercase", color: "#d8b4fe", fontWeight: 700 }}>
              Ready to scale content?
            </div>
            <h2 style={{ fontSize: 42, margin: "18px 0 12px", letterSpacing: "-0.05em" }}>
              Build your AI content engine today.
            </h2>
            <p style={{ maxWidth: 700, margin: "0 auto 26px", color: "#cbd5e1", lineHeight: 1.7 }}>
              Launch faster, keep your content aligned to each workspace, and automate the content pipeline with a platform designed for modern teams.
            </p>
            <button style={styles.primaryButton}>Get started</button>
          </div>
        </section>

        <footer style={styles.footer}>
          <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", gap: 16, flexWrap: "wrap" }}>
            <div style={{ display: "flex", alignItems: "center", gap: 10 }}>
              <div style={styles.logoMark}>M</div>
              <span style={{ fontWeight: 700 }}>MATRIX</span>
            </div>
            <div>© 2026 MATRIX AI Content Engine</div>
          </div>
        </footer>
      </div>
    </div>
  );
}
```

This is the full premium landing page.

If you want, the next step is:
- a full SaaS dashboard design in React
- a product management page
- a full data model and seeded sample products
- a premium landing page plus login/register flow integrated together in one app

If you want a final full app bundle, I can generate the complete React code for:
- App.tsx
- LandingPage.tsx
- AuthPage.tsx
- DashboardPage.tsx
- Sidebar.tsx
- ProductCard.tsx
- ContentGeneratorPanel.tsx
- all CSS in a single theme file

I can give you that next.#!/usr/bin/env bash
set -euo pipefail

mkdir -p .github/workflows \
  backend/src/config backend/src/controllers backend/src/middleware \
  backend/src/models backend/src/routes backend/src/scripts backend/src/services \
  backend/src/types backend/src/utils \
  frontend/src/pages

git init
git checkout -b feature/matrix-ai-content-engine

cat > .gitignore <<'EOF'
node_modules
dist
build
coverage
.env
.env.*
!.env.example
.DS_Store
npm-debug.log*
yarn-debug.log*
yarn-error.log*
EOF

cat > .env.example <<'EOF'
NODE_ENV=development
PORT=5000
MONGODB_URI=mongodb://localhost:27017/matrix
JWT_SECRET=super_secret_change_this
OPENAI_API_KEY=your_openai_api_key
CLIENT_URL=http://localhost:5173
EOF

cat > docker-compose.yml <<'EOF'
version: "3.9"

services:
  mongo:
    image: mongo:7
    container_name: matrix-mongo
    restart: unless-stopped
    ports:
      - "27017:27017"
    environment:
      MONGO_INITDB_DATABASE: matrix
    volumes:
      - mongo_data:/data/db

volumes:
  mongo_data:
EOF

cat > README.md <<'EOF'
# MATRIX AI Content Engine

A workspace-bound AI content generation platform for product-driven content creation and automation.

## Features
- Workspace-bound multi-tenant generation
- Product-based AI copy generation
- Supported content types:
  - description
  - review
  - seo
  - social
  - ad
- OpenAI-powered generation
- JWT auth
- Role enforcement:
  - owner
  - admin
  - editor
  - viewer
- Login + registration UI
- Premium SaaS dashboard
- Usage metering hooks
- MongoDB integration
- Docker + CI

## Setup

### 1) Install dependencies
```bash
npm --prefix backend install
npm --prefix frontend install