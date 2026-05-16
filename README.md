# Okana 🌲🍷

**Your AI Concierge for the Okanagan Valley**  
*The one local who actually knows everything.*

Okana is an intelligent tourism agent that feels like chatting with a super-knowledgeable Okanagan local. On the surface: one friendly, conversational interface. Under the hood: a coordinated team of specialized AI agents handling wineries, trails, bookings, farms, events, and more.

Built for visitors, locals, and businesses who want personalized, real-time experiences in British Columbia’s Okanagan region.

---

## ✨ Features

- **Single Point of Contact** — One natural chat interface for everything Okanagan
- **Multi-Agent Orchestration** — Specialized agents collaborate behind the scenes:
  - 🍷 **Sommelier** – Winery tours, tasting notes, pairings & reservations
  - 🏞️ **Outdoor Guide** – Hiking, biking, kayaking, trails, golf, seasonal activities
  - 🌾 **Farm & Food** – Markets, agritourism, pick-your-own, farm-to-table
  - 🏨 **Bookings & Logistics** – Accommodations, rentals (cars, bikes, boats), tours, real-time availability
  - 🎉 **Events & Culture** – Festivals, markets, Indigenous experiences, hidden gems
  - ☀️ **Live Insights** – Weather-aware planning, road conditions, last-minute options
- **Personalized Itineraries** — Multi-day plans tailored to group size, budget, interests & season
- **Real-time Integration** — Connects to local APIs, calendars, and booking systems
- **Memory & Continuity** — Remembers your preferences across conversations

---

## 🏗️ Architecture

Okana uses a **hierarchical multi-agent system**:

```
User → Okana (Orchestrator)
          ↓
   Specialist Agents + Tools
          ↓
   Shared Knowledge Base + Live Data
```

- **Orchestrator** routes requests intelligently and synthesizes responses
- **CrewAI / LangGraph** powers agent coordination
- **RAG** over local guides, winery data, trail maps, and menus
- **Tool calling** for bookings, maps, weather, and availability

---

## 🛠️ Tech Stack

- **Frontend**: SvelteKit + Tailwind (streaming chat UI)
- **Backend/Agents**: TypeScript + Node.js (CrewAI-compatible)
- **Database & Auth**: Supabase
- **Vector Store**: Supabase pgvector (for RAG)
- **LLMs**: Grok / Claude 3.5 / GPT-4o (tool calling)
- **Deployment**: Vercel (frontend) + Railway / Fly.io (agents)
- **Maps**: Google Maps / Mapbox

---

## 🚀 Getting Started

### Prerequisites
- Node.js 20+
- Supabase project
- OpenAI / Anthropic / xAI API keys

### 1. Clone & Install
```bash
git clone https://github.com/LegionsBoom/okana.git
cd okana
npm install
```

### 2. Environment Variables
Copy `.env.example` → `.env` and fill in:
```env
SUPABASE_URL=
SUPABASE_ANON_KEY=
OPENAI_API_KEY=            # or ANTHROPIC_API_KEY, etc.
MAPBOX_TOKEN=
```

### 3. Run Locally
```bash
# Start frontend
npm run dev

# Start agent backend (in another terminal)
cd agents
npm run dev
```

### 4. Seed Knowledge Base
```bash
npm run seed
```

---

## 📍 Roadmap

- [ ] MVP Chat Interface + 4 core agents
- [ ] Real-time booking integrations
- [ ] Voice mode (mobile-friendly)
- [ ] Business dashboard for wineries & tour operators
- [ ] Mobile PWA + iOS/Android apps
- [ ] Multi-language support
- [ ] Analytics & recommendation engine

---

## 🤝 Contributing / Access

Internal project — access restricted to authorized team members only.

---

**Made with ❤️ for the Okanagan**  
*From trails to tasting rooms — one conversation at a time.*

---

**Questions or partnerships?**  
Reach out directly (wineries, tourism operators, Destination BC, etc. welcome for collaboration).