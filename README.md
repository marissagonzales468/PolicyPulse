🌎 PolicyPulse: AI Debate Arena

Understand the policy. Hear both sides. Make your voice count.

PolicyPulse is an interactive AI-powered debate platform designed to make environmental policies easier to understand, explore, and discuss.

By bringing two AI agents together to debate environmental propositions, PolicyPulse transforms complicated policy discussions into engaging conversations. Users can hear arguments for and against a proposal, understand its real-world consequences, and vote on which position they support.

Our mission is to make policy accessible to everyone — because environmental decisions don’t just affect future generations. They affect our communities, our livelihoods, our economy, and the world we live in today.

⸻

🌱 The Problem

Environmental policies can be difficult to understand. Government proposals are often filled with technical language, complicated regulations, and information scattered across different sources.

More importantly, environmental issues are often presented as problems for the future, when their effects are already being experienced today.

These decisions influence:

* Communities: Public health, pollution exposure, housing, transportation, and quality of life.
* Private Sector: Business operations, energy costs, innovation, regulations, and employment.
* Public Sector: Government spending, infrastructure, public services, and environmental protections.
* The Economy: Consumer prices, economic growth, industry transitions, and job opportunities.
* Future Generations: Sustainability, natural resources, climate resilience, and long-term environmental health.

People deserve more than headlines. They deserve an opportunity to understand the reasoning behind policies and how those decisions affect their everyday lives.

💡 Our Solution

PolicyPulse creates an AI-powered debate arena where two intelligent agents explore opposing perspectives on environmental policies.

Think of it as having your own personal policy representatives: two AI agents presenting the arguments, explaining the consequences, and helping you understand the bigger picture.

Instead of simply telling users what to think, we encourage them to listen, question, compare, and decide for themselves.

⚡ Core Features

1. AI-Powered Policy Debates

* Enter an environmental proposition or policy topic.
* Two AI agents debate the proposal.
* One agent argues in favor (PRO).
* The other agent argues against it (CON).
* Agents generate arguments, counterarguments, and rebuttals using Google Gemini.

2. AI Voice Integration

* Bring AI agents to life with voice-powered debate.
* Give each agent a distinct voice.
* Connect generated arguments to voice playback through the voice integration (Vapi/LMNT, depending on the configured provider).

3. Community Voting & Polls

After each debate, users can vote on the proposition or the arguments presented.

Voting options can include:

* YES — Support the environmental policy.
* NO — Oppose the environmental policy.
* DRAW — Neither side made a stronger case.

Votes are collected to provide a picture of how participating users feel about different environmental policies.

4. Leaderboard & Voting Statistics

Explore voting results and see how different policies compare.

The leaderboard is designed to display:

* Total votes per policy.
* YES versus NO voting percentages.
* Number of DRAW votes.
* Overall community sentiment.
* Most supported and most opposed propositions.

5. Trending Environmental Topics

Discover which environmental policies are attracting the most attention.

Trending topics can be ranked by:

* Total votes.
* Recent voting activity.
* Community engagement.
* Changes in voting sentiment.

6. AI-Generated Debate Summaries

Receive a concise summary of each debate, including:

* Main arguments supporting the policy.
* Main arguments opposing the policy.
* Key points of disagreement.
* Potential community and economic consequences.

⸻

🧠 Technology Stack

Technology	Purpose
Python	Backend logic
FastAPI	API development and integration
React	Frontend interface
Vite	Frontend development and build tooling
TypeScript	Frontend development
Google Gemini	AI debate agents and summaries
Vapi / LMNT	Voice integration
Tailwind CSS	Styling and responsive interface
Java	Optional logic integration
Git & GitHub	Collaboration and version control

The exact voice provider and optional Java integration depend on the team’s final implementation.

🏗️ System Architecture

PolicyPulse follows a frontend-to-backend architecture.

1. The user enters an environmental policy.
2. React sends the policy to the FastAPI backend.
3. FastAPI coordinates the AI agents.
4. Google Gemini generates arguments and counterarguments.
5. The voice integration converts generated content into speech.
6. The frontend displays and plays the debate.
7. Users submit their votes.
8. FastAPI records voting data.
9. The leaderboard and trending topics display aggregated results.

Architecture Overview

flowchart TD
    A[User] --> B[React + Vite Frontend]
    B --> C[FastAPI Backend]
    C --> D[Gemini PRO Agent]
    C --> E[Gemini CON Agent]
    D --> C
    E --> C
    C --> F[Vapi / LMNT Voice Integration]
    F --> B
    B --> G[User Voting]
    G --> C
    C --> H[Voting Database / Storage]
    H --> I[Leaderboard]
    H --> J[Trending Topics]
    H --> K[Poll Statistics]

📂 Project Structure

The following is the intended organization. Actual filenames may differ depending on the current repository.

PolicyPulse/
│
├── backend/
│   ├── main.py
│   ├── agents/
│   │   ├── pro_agent.py
│   │   └── con_agent.py
│   ├── services/
│   │   ├── gemini_service.py
│   │   └── voice_service.py
│   ├── routes/
│   │   ├── debate.py
│   │   ├── voting.py
│   │   └── leaderboard.py
│   ├── requirements.txt
│   └── .env.example
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   │   ├── Leaderboard.tsx
│   │   │   └── TrendingTopics.tsx
│   │   ├── App.tsx
│   │   └── main.tsx
│   ├── package.json
│   └── vite.config.ts
│
├── README.md
└── .gitignore

🚀 Getting Started

Prerequisites

Install the following before running the application:

* Python 3.10+
* Node.js and npm
* Git
* Google Gemini API key
* Vapi credentials and/or LMNT API credentials if using those services

1. Clone the Repository

git clone YOUR_GITHUB_REPOSITORY_URL
cd PolicyPulse

2. Start the Backend

Navigate to the backend:

cd backend

Create a virtual environment:

python -m venv venv

Activate it on macOS/Linux:

source venv/bin/activate

Install dependencies:

pip install -r requirements.txt

Configure your environment variables using the provided .env.example file.

Start FastAPI:

uvicorn main:app --reload

Backend documentation:

http://127.0.0.1:8000/docs

3. Start the Frontend

Open a second terminal:

cd frontend

Install dependencies:

npm install

Start the development server:

npm run dev

Open the local URL provided by Vite, usually:

http://localhost:5173

🔑 Environment Variables

Create a .env file inside the backend directory.

Example:

GEMINI_API_KEY=your_gemini_api_key
VAPI_API_KEY=your_vapi_api_key
LMNT_API_KEY=your_lmnt_api_key

Only configure credentials for integrations actually being used.

Important: Never upload API keys, passwords, or private credentials to GitHub. Keep .env in .gitignore.

🔌 API Endpoints

The following are the planned core API operations. Their exact paths and request formats should match the implemented backend.

Endpoint	Method	Purpose
/api/initiate-debate	POST	Start a debate using a submitted policy
/api/next-argument	POST	Generate the next AI argument
/api/text-to-speech	POST	Generate voice audio
/api/summarize-debate	POST	Summarize the debate
/api/submit-vote	POST	Record a user’s vote
/api/leaderboard	GET	Retrieve aggregated voting statistics
/api/trending	GET	Retrieve trending policy topics

📊 Our Vision for Public Opinion

One of PolicyPulse’s most important features is making public participation visible.

We want users to see more than just which AI agent won a debate. We want them to understand how people feel about the actual policy.

For example:

Proposition: Should governments increase renewable energy requirements?

Voting response	Example votes
YES	650
NO	250
DRAW	100
Total	1,000

These are illustrative numbers, not actual polling results.

This allows users to explore how participating users respond to different policies and compare community sentiment across topics.

Our goal: Make policy discussions more transparent, accessible, and participatory.

Note: Platform voting represents participating users, not necessarily the majority opinion of an entire country. Nationally representative conclusions require properly sampled public opinion research.

🌍 Social Impact

PolicyPulse is built around one central belief:

Environmental policy is not just about protecting the planet. It’s about protecting the people who live on it.

We want to encourage people to think beyond political headlines and consider the broader consequences of policy decisions.

By presenting opposing arguments and making voting statistics accessible, we hope to:

* Encourage critical thinking.
* Increase environmental policy awareness.
* Make complex government proposals easier to understand.
* Highlight the connection between environmental protection and economic opportunity.
* Encourage meaningful public participation.
* Help people make more informed decisions.

🔮 Future Development

Potential future improvements include:

* More AI agents representing different perspectives.
* Real-time government policy and legislative data.
* Research-backed citations for AI-generated arguments.
* Interactive charts and data visualizations.
* AI-generated images to support debate arguments.
* Geographic breakdowns of participating users’ votes, with appropriate privacy protections.
* Community discussions and shared debates.
* Accessibility features, including captions and transcripts.

👥 Team & Contributions

PolicyPulse is a collaborative project. We welcome contributions across:

* Frontend development
* Backend development
* AI agent development
* Voice integration
* Data visualization
* Voting and analytics
* UI/UX design

To contribute:

1. Fork or clone the repository.
2. Create a feature branch.
3. Make your changes.
4. Test your implementation.
5. Submit a pull request for review.

❤️ Our Mission

We created PolicyPulse because understanding environmental policy shouldn’t require a law degree, hours of research, or navigating complicated government documents.

Everyone deserves the opportunity to understand the decisions shaping their communities.

We believe that when people hear both sides, examine the evidence, and have a voice in the conversation, they become better informed participants in society.

PolicyPulse — Hear Both Sides. Understand the Impact. Make Your Voice Count.