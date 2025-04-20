# Magnetism – Project Specification & Architecture

## 1. Overview
Magnetism is an iOS app that acts as an AI-powered wingperson, blending emotional intelligence, personalized dating advice, and chat analysis to help users navigate dating conversations and build confidence.

---

## 2. User Flow & Core Screens

### 2.1. Onboarding & Authentication
- Welcome screen with app intro
- Sign in with Apple (Firebase Auth)
- Profile setup: name, age, dating goals, experience level

### 2.2. Persona Builder
- Multi-step form for target persona traits:
  - Name/nickname, age range
  - Habits (smoking, drinking, health, gym, etc.)
  - Political views, MBTI/vibe/personality
  - Love language, relationship history
  - Humor style, communication style
  - Green/red flags, interests
  - Situational questions
- Save/load multiple personas (Firestore)

### 2.3. Chat Analysis
- Paste chat text or upload screenshot
- AI analysis (mood, tone, cues, intent)
- Suggested replies (with tone options)
- "Magnetism Predicts" (interest/intent cues)
- Rizz Coach (daily prompt, feedback, phrase vault)

### 2.4. Bonus Features
- Crush Meter (interest score)
- Don’t Text Her Yet alert
- Wingman Mode (anonymous sharing)

---

## 3. Technical Architecture

### 3.1. Frontend (iOS App)
- **SwiftUI** for UI, navigation, and animations
- **Combine** or **Swift Concurrency** for async data flows
- **Accessibility**: VoiceOver, Dynamic Type, color contrast

### 3.2. Backend (Firebase)
- **Auth**: Sign in with Apple, email/password
- **Firestore**: Store user profiles, personas, chat logs
- **Storage**: Store uploaded screenshots (optional)
- **Cloud Functions**: Proxy for OpenAI API (secure API key, process chat analysis)

### 3.3. AI Integration
- **OpenAI GPT API**: For chat analysis, reply suggestions, mood/intent detection
- **Cloud Function Flow**:
  1. App sends chat data to Firebase Function
  2. Function calls OpenAI API
  3. Function returns results to app
- **On-device**: Use Apple Vision for basic screenshot text extraction (privacy-friendly)

---

## 4. Data Model (Firestore)
- **Users**: uid, profile info, onboarding status
- **Personas**: personaId, userId, traits, timestamps
- **Chats**: chatId, userId, personaId, messages, AI analysis, timestamps
- **RizzCoach**: userId, dailyPrompts, feedback, history

---

## 5. Security & Compliance
- All sensitive AI calls via Cloud Functions (never expose OpenAI key in app)
- Store minimal user data; comply with Apple privacy guidelines
- User consent for screenshot uploads and analytics

---

## 6. App Store Readiness
- Accessibility: VoiceOver, Dynamic Type, haptic feedback
- Privacy: Clear onboarding, privacy policy, permission dialogs
- Polish: App icon, splash, micro-animations, error handling

---

## 7. Next Steps
1. Scaffold SwiftUI app structure
2. Set up Firebase project & integrate SDKs
3. Build persona builder UI & Firestore logic
4. Implement chat analysis flow (Cloud Function + OpenAI)
5. Add polish, accessibility, and compliance features

---

## 8. References
- [SwiftUI Documentation](https://developer.apple.com/xcode/swiftui/)
- [Firebase for iOS](https://firebase.google.com/docs/ios/setup)
- [OpenAI API Docs](https://platform.openai.com/docs/api-reference)

---

*This document is a living specification. Update as features evolve.*
