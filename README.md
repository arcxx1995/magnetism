# Magnestism – Your AI Wingperson with Emotional Intelligence

Magnetism is an iOS app that acts as your AI wingperson, combining emotional intelligence, personalized dating advice, and real-time chat analysis to help you navigate the world of modern dating.

---

## 🚀 Core Features

### 1. User Onboarding & Profile Creation
- Register/login (Sign in with Apple, Firebase Auth)
- Set up your dating goals, experience, and preferences

### 2. Target Persona Builder
- Input detailed traits for your ideal match (habits, personality, communication style, etc.)
- Save and manage multiple personas

### 3. Custom GPT Dating Assistant
- Analyze chat screenshots or pasted text
- Detect mood, tone, and intent (e.g., playful, cold, stressed)
- Suggest replies in various tones (funny, flirty, chill, deep)
- Highlight cues (e.g., sarcasm, mirroring)
- "Ftana Predicts": Are they interested or losing interest?

### 4. Mood & Intent Analysis
- Analyze message frequency, emoji use, delays, and tone changes
- Visual cues: Interested, Playing it cool, Mixed signals, Losing interest, Ghost mode

### 5. Rizz Coach
- Daily prompt to practice your flirting
- "Rizz Workout": Craft replies and get AI feedback
- Flirt phrase vault by style
- Past conversation analysis and improvement suggestions

### 6. Bonus Features
- "Crush Meter" – real-time interest score
- "Don’t Text Her Yet" alert
- Wingman Mode – share convos anonymously for peer review

---

## 🛠️ Tech Stack
- **Frontend:** SwiftUI (iOS native)
- **Backend:** Firebase (Auth, Firestore, Storage)
- **AI:** OpenAI GPT API (via Firebase Cloud Functions)
- **Other:** Apple Sign In, Accessibility, App Store compliance

---

## 📱 App Structure
- Onboarding & Authentication
- Profile & Persona Management
- Chat Analysis & Suggestions
- Rizz Coach & Flirt Vault
- Settings, Peer Review, and More

---

## ⚡ Getting Started

1. **Clone the Project**
   ```
   git clone <your-repo-url>
   ```
2. **Open in Xcode**
   - Open `Ftana.xcodeproj` in Xcode (15+ recommended)
3. **Configure Firebase**
   - Create a Firebase project
   - Download `GoogleService-Info.plist` and add to Xcode project
   - Enable Auth (Apple Sign In, Email/Password)
   - Set up Firestore and Storage
4. **Set Up OpenAI API**
   - Deploy provided Cloud Function (see `/cloud-functions`)
   - Add your OpenAI API key to the function environment
5. **Run the App**
   - Build and run on simulator or device

---

## 📂 Project Structure
- `/Ftana/` – SwiftUI app source code
- `/cloud-functions/` – Firebase functions for OpenAI integration
- `/Resources/` – Assets, icons, etc.
- `README.md` – This document

---

## 📝 Roadmap
- [ ] Onboarding & Auth screens
- [ ] Persona builder UI
- [ ] Chat analysis integration
- [ ] Rizz Coach module
- [ ] Animations & accessibility polish
- [ ] App Store prep

---

## 💡 Contributing
Pull requests welcome! For major changes, open an issue first to discuss your ideas.

---

## 📫 Contact
Questions, feedback, or want to collaborate? Reach out at [your-email@example.com]

---

## 📄 License
MIT License. See LICENSE file for details.
