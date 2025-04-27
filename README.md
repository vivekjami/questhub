# QuestHub

**QuestHub** is a decentralized platform built on Solana, designed to onboard users to cryptocurrency through interactive, user-generated challenges and contests. Users can create and participate in a variety of challenges—ranging from gaming and creative tasks to real-world activities—while earning token rewards. The platform integrates AI to provide personalized challenge recommendations, enhancing user engagement and making crypto education fun and accessible.

This project is developed for the [Solana Breakout Hackathon](https://www.colosseum.org/breakout) in the **Consumer** track, sponsored by [MagicBlock](https://www.magicblock.gg/), with a focus on building the next generation of mobile and web products to onboard billions of users to crypto.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Technical Stack](#technical-stack)
- [AI Integration](#ai-integration)
- [Development Timeline (19 Days)](#development-timeline-19-days)
- [Setup Instructions](#setup-instructions)
- [Development Steps](#development-steps)
- [Deployment](#deployment)
- [Testing](#testing)
- [Submission Requirements](#submission-requirements)
- [Additional Resources](#additional-resources)

## Project Overview
QuestHub combines user-generated content, gamification, and blockchain rewards to create an engaging platform for crypto newcomers. By leveraging Solana’s fast and low-cost transactions, QuestHub ensures a seamless experience for users to create, participate in, and earn from challenges. The integration of AI personalizes the user journey, recommending challenges based on interests and skill levels, making it easier for users to learn and interact with crypto concepts.

### Key Objectives
- Onboard users to crypto through interactive challenges.
- Enable users to create and participate in diverse challenges (gaming, creative, real-world).
- Provide token rewards on Solana’s devnet for transparency and fairness.
- Use AI to personalize challenge recommendations and enhance user engagement.
- Build a mobile-responsive web app to compete for the Solana Mobile Award.

## Features
1. **User-Generated Challenges**:
   - Users can create challenges in categories like gaming (e.g., "Score 100 points in this mini-game"), creative tasks (e.g., "Design a digital artwork"), or real-world activities (e.g., "Take a photo of a landmark").
   - Challenge creators define the rules, submission criteria, and reward amounts.

2. **Challenge Participation**:
   - Users browse and participate in challenges, submitting their entries (e.g., scores, images, text).
   - Winners are determined by community voting or predefined criteria (e.g., highest score).

3. **Token Rewards**:
   - Winners earn SOL or custom tokens on Solana’s devnet.
   - Transparent reward distribution using Solana’s blockchain.

4. **AI-Personalized Recommendations**:
   - AI suggests challenges based on user interests, past activity, and skill level.
   - Example: Beginners receive easier challenges, while advanced users get more complex tasks.

5. **Community Voting**:
   - For creative or subjective challenges, the community votes on the best submissions.
   - Voting is incentivized with small token rewards.

6. **Mobile-Responsive Design**:
   - Optimized for mobile devices to compete for the $25,000 Solana Mobile Award.

## Technical Stack
| **Component** | **Technology** | **Rationale** |
|---------------|----------------|---------------|
| **Frontend**  | React, Next.js, Tailwind CSS | Responsive, modern UI for web and mobile. |
| **Backend**   | Django, PostgreSQL | Robust API and database for challenge management. |
| **Blockchain**| Solana Web3.js | Fast, low-cost transactions for rewards. |
| **AI**        | Hugging Face (rule-based or simple ML) | Quick integration for personalized recommendations. |
| **Authentication** | Auth0 | Secure user login and management. |
| **Development** | Replit | Collaborative prototyping for rapid development. |
| **Deployment** | Vercel (frontend), Railway (backend) | Reliable, free hosting for demo purposes. |

## AI Integration
AI enhances QuestHub by providing personalized challenge recommendations, making the platform more engaging and user-friendly. The AI system will:
- Analyze user profiles, past challenge completions, and preferences.
- Recommend challenges that match the user’s skill level and interests.
- Use a rule-based system or simple machine learning (e.g., clustering users by activity) for quick implementation.

**Example**:
- A user who frequently participates in gaming challenges will receive recommendations for similar tasks.
- Beginners are suggested introductory challenges, while experienced users get advanced ones.

**Implementation**:
- Use [Hugging Face](https://huggingface.co/) for pre-trained models or a custom rule-based system.
- Integrate AI logic in the Django backend to generate recommendations.

## Development Timeline (19 Days)
Given the hackathon deadline on May 16, 2025, and the current date being April 27, 2025, you have 19 days to complete the project. Below is a structured timeline:

| **Phase**          | **Days**       | **Tasks**                                      |
|--------------------|----------------|------------------------------------------------|
| **Setup & Design** | Days 1–2 (Apr 27–28) | Initialize repo, design wireframes, set up Replit. |
| **Core Development** | Days 3–10 (Apr 29–May 6) | Build frontend, backend, blockchain integration, AI. |
| **Testing & Iteration** | Days 11–15 (May 7–11) | Deploy, test, gather feedback, refine UI. |
| **Presentation & Submission** | Days 16–19 (May 12–15) | Record video, finalize documentation, submit. |

## Setup Instructions
1. **GitHub Repository**:
   - Create a public repository on [GitHub](https://github.com/) named `QuestHub`.
   - Initialize with a `README.md`, `.gitignore`, and license.

2. **Replit Setup**:
   - Create a new project on [Replit](https://replit.com/) with Python (for Django) and JavaScript (for Next.js).
   - Invite collaborators if working in a team.

3. **Local Development (Optional)**:
   - Clone the repo locally: `git clone https://github.com/yourusername/QuestHub.git`
   - Install dependencies:
     - Frontend: `cd frontend && npm install`
     - Backend: `cd backend && pip install -r requirements.txt`

4. **Environment Variables**:
   - Set up `.env` files for sensitive data (e.g., API keys, Solana wallet secrets).
   - Use [Auth0](https://auth0.com/) for authentication; configure in both frontend and backend.

## Development Steps
### Step 1: Design Wireframes (Day 1)
- Use [Figma](https://www.figma.com/) to create wireframes for:
  - Homepage with challenge list.
  - Challenge creation form.
  - User profile with completed challenges and rewards.
  - Mobile-responsive layouts.

### Step 2: Backend Development (Days 3–6)
- **Models**:
  - `User`: Profile, wallet address, challenge history.
  - `Challenge`: Title, description, category, reward, creator, participants.
  - `Submission`: User submissions (text, images, scores).
  - `Vote`: Community votes on submissions.
- **APIs**:
  - CRUD operations for challenges and submissions.
  - Reward distribution logic using Solana Web3.js.
- **Database**:
  - Use PostgreSQL for relational data.
  - Set up migrations and seed initial data.

### Step 3: Blockchain Integration (Days 7–8)
- **Solana Setup**:
  - Use [Solana Web3.js](https://solana-labs.github.io/solana-web3.js/) for wallet integration (e.g., Phantom).
  - Implement functions to mint and transfer tokens on devnet.
- **Reward Logic**:
  - When a challenge is completed, trigger a token transfer to the winner’s wallet.
  - Use Solana’s fast transactions to ensure real-time rewards.

### Step 4: Frontend Development (Days 9–10)
- **Components**:
  - `ChallengeList`: Display available challenges.
  - `ChallengeForm`: Form to create new challenges.
  - `ProfilePage`: Show user stats, completed challenges, and rewards.
- **UI/UX**:
  - Use Tailwind CSS for styling, ensuring mobile responsiveness.
  - Integrate Auth0 for secure login.

### Step 5: AI Integration (Days 11–12)
- **Recommendation Logic**:
  - Implement a rule-based system in Django to suggest challenges based on user activity.
  - Example: If a user completes a gaming challenge, recommend similar challenges.
- **Optional ML**:
  - Use Hugging Face’s [Transformers](https://huggingface.co/transformers/) for simple user clustering if time permits.

### Step 6: Testing and Iteration (Days 13–15)
- **Unit Tests**:
  - Test backend APIs with Django’s test framework.
  - Test frontend components with Jest or React Testing Library.
- **User Feedback**:
  - Share a beta version on X (Twitter) to gather feedback.
  - Fix bugs and refine the UI based on responses.

### Step 7: Deployment (Day 16)
- **Frontend**:
  - Deploy on [Vercel](https://vercel.com/) for free, fast hosting.
- **Backend**:
  - Deploy on [Railway](https://railway.app/) with PostgreSQL add-on.
- **Blockchain**:
  - Ensure Solana devnet is used for all transactions.

## Deployment
1. **Vercel (Frontend)**:
   - Connect GitHub repo to Vercel.
   - Set environment variables for API URLs and Auth0.
   - Deploy with `vercel --prod`.

2. **Railway (Backend)**:
   - Create a new project, link GitHub repo.
   - Add PostgreSQL database service.
   - Set environment variables for database and Solana keys.
   - Deploy with `railway up`.

3. **Solana Devnet**:
   - Use [Solana CLI](https://docs.solana.com/cli) to manage tokens and accounts.
   - Fund devnet wallets for testing rewards.

## Testing
- **Functional Testing**:
  - Create and complete a challenge, ensuring rewards are distributed.
  - Test AI recommendations by completing challenges and checking suggestions.
- **Performance Testing**:
  - Simulate multiple users creating and voting on challenges.
  - Ensure Solana transactions process quickly.
- **Security Testing**:
  - Use Auth0’s security features to prevent unauthorized access.
  - Validate user inputs to prevent SQL injection or XSS attacks.

## Submission Requirements
- **GitHub Repository**: Public, with a detailed README.
- **Video Demo**: 3-minute video using [Loom](https://www.loom.com/) covering:
  - Team background and expertise.
  - QuestHub’s purpose and features.
  - Market opportunity and user onboarding strategy.
  - Live demo of challenge creation, participation, and rewards.
- **Submission Portal**: Submit via [Colosseum’s hackathon portal](https://www.colosseum.org/breakout) by May 16, 2025.

## Additional Resources
- [Solana Documentation](https://docs.solana.com/)
- [Next.js Documentation](https://nextjs.org/docs)
- [Django Documentation](https://docs.djangoproject.com/)
- [Hugging Face Transformers](https://huggingface.co/transformers/)
- [Auth0 Documentation](https://auth0.com/docs)
- [MagicBlock Documentation](https://docs.magicblock.gg/)
