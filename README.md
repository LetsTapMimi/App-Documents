Buzz Catcher

Data-driven drinking decisions

A Flutter app designed for adults who want to socialize and drink responsibly while staying in control.

Core Features

Drink Tracking

Quick-log common drinks (beer, wine, cocktails, shots)
Cocktail selector with categorized options:
Classic Cocktails (Margarita, Martini, Old Fashioned, Mojito, etc.)
Simple Mixed Drinks (Vodka Soda, Rum & Coke, Gin & Tonic, etc.)
Strong Cocktails (Long Island, Negroni, Strong Martini)
Frozen Cocktails (Frozen Margarita, Daiquiri, Piña Colada)
Shot selector with single/double option:
Standard spirits (Tequila, Vodka, Whiskey, Rum, Gin)
Specialty shots (Jägermeister, Jägerbomb, Fireball)
Canned & Bottled selector for pre-packaged drinks:
Seltzer, Beer, Cider, Cocktail RTD, Wine/Cooler
Custom Drink builder with:
Quick entry (ABV % + volume)
Strength selector (Light/Regular/Strong/My usual)
Build your drink (base spirit + mixer + pour level)
Save as preset for quick logging
"Your drinks" section showing saved favorites
Automatic BAC (Blood Alcohol Content) calculation using the Widmark formula
Real-time tracking of session duration and drink count
Vibe Status

Live "Current Vibe" display showing your status
Visual BAC level indicator with personalized advice
Progressive warnings as BAC increases:
Glowing & in control
Feeling the vibe
Peak zone - stay here
Consider slowing down
Time to hydrate & coast
Cognitive Mini-Test

Optional reaction time test to check cognitive function
5-round tap test that measures reflexes
Provides feedback on whether to slow down on drinks
Emotion Check-In

Track how you're feeling during the night
Select from 8 emotions: happy, confident, relaxed, anxious, tired, energetic, social, overwhelmed
Energy level slider (1-5)
Optional notes
Morning Check-In

Next-day wellness tracking:
Sleep quality
Hangover level
Fatigue level
Overall mood
Optional notes for future insights
Design Philosophy

Tone: Youthful, modern, confident, non-judgmental. Not childish, not preachy.

Visual Style:

Muted neon color palette (pink, purple, cyan)
Soft gradients and rounded corners
Clean typography with Material 3 design
Minimal clutter, wellness-meets-nightlife aesthetic
Microcopy: Friendly and supportive without being condescending

"Data-driven drinking decisions"
"Looking sharp!" / "Consider slowing down"
"Rest well! "
Technical Architecture

State Management

Provider pattern for session state
SessionProvider manages:
Active drinking sessions
Drink logs
Emotion check-ins
Cognitive test results
Morning check-ins
Data Models

Drink: Individual drink with type, ABV, volume, timestamp
DrinkingSession: Complete session with drinks, check-ins, and tests
EmotionCheckin: Emotion tracking with energy level
CognitiveTest: Reaction time test results
MorningCheckin: Next-day wellness data
UserProfile: User preferences and physical stats for BAC calculation
CustomDrinkPreset: Saved custom drinks with ABV, volume, and standard drinks
Key Components

Reusable Widgets:

DrinkLoggingCard - Quick drink entry with 2x2 grid
CustomDrinkSheet - Comprehensive custom drink builder
VibeStatusCard - Current status display with gradient
EmotionCheckinSheet - Bottom sheet for feelings
CognitiveTestModal - Reaction time game
PremiumBadge - Premium feature indicator
PremiumLockOverlay - Blur overlay for locked features
Screens:

HomeScreen - Main dashboard with all features
MorningCheckinScreen - Post-session wellness check
HistoryScreen - Past sessions with insights
SessionDetailsScreen - Detailed session breakdown
ProfileScreen - User settings and preferences
OnboardingFlow - First-time user setup
AgeVerificationScreen - Legal age gate
HarmReductionDisclaimerScreen - App disclaimer
PaywallScreen - Premium subscription offer
BAC Estimation

Uses the Widmark formula:

BAC = (A × 5.14 / W × r) - 0.015 × H
Where:

A = liquid ounces of alcohol consumed
W = weight in pounds
r = alcohol distribution ratio (0.73 for male bodies, 0.66 for female bodies)
H = hours since drinking began
Future Features (TODO)

 User profile with weight and gender settings
 Custom drink builder
 Session history view
 Cocktail and shot categorization
 Premium/Free tier system
 Age verification and harm reduction disclaimer
 Buzz Profiles - Save successful drinking patterns
 Monthly Insights - Pattern analysis and recommendations
 On-device ML profile blurbs (iOS)
 Drink type analytics
 Session history with detailed breakdowns
 Export session data (Premium)
 Notifications for check-in reminders
 Water tracking between drinks
 Friend tracking / social features (optional)
 Predictive alerts (Premium)
 Cloud sync across devices
Getting Started

Prerequisites

Flutter SDK (3.10.0-290.4.beta or higher)
Dart SDK
Installation

Clone the repository
Install dependencies:
flutter pub get
Run the app:
flutter run
Dependencies

provider: ^6.1.2 - State management
intl: ^0.20.2 - Date/time formatting
shared_preferences: ^2.2.2 - Local data persistence
cupertino_icons: ^1.0.8 - iOS-style icons
Project Structure

lib/
├── main.dart                              # App entry point with theme
├── models/
│   ├── drink.dart                         # Drink data model
│   ├── session.dart                       # Session & check-in models
│   ├── user_profile.dart                  # User profile model
│   ├── custom_drink_preset.dart           # Saved custom drinks
│   └── back_calculator.dart               # BAC estimation logic
├── providers/
│   └── session_provider.dart              # State management
├── services/
│   └── subscription_service.dart          # Premium subscription logic
├── config/
│   └── feature_gate.dart                  # Premium feature configuration
├── screens/
│   ├── home_screen.dart                   # Main dashboard
│   ├── history_screen.dart                # Past sessions
│   ├── session_details.dart               # Session breakdown
│   ├── morning_checkin_screen.dart        # Morning survey
│   ├── profile_screen.dart                # User settings
│   ├── onboarding_profile.dart            # First-time setup
│   ├── age_verification_screen.dart       # Legal age gate
│   ├── harm_reduction_disclaimer_screen.dart  # App disclaimer
│   └── paywall_screen.dart                # Premium subscription
└── widgets/
    ├── drink_logging_card.dart            # Quick drink entry 2x2 grid
    ├── custom_drink_sheet.dart            # Custom drink builder
    ├── vibe_status_card.dart              # Status display
    ├── emotion_checkin_sheet.dart         # Emotion tracking
    ├── cognitive_test_modal.dart          # Reaction test
    ├── premium_badge.dart                 # Premium indicator
    └── premium_lock_overlay.dart          # Feature lock overlay
Contributing

This app implements comprehensive drink tracking with custom drink builder, premium features, and harm reduction tools. Ready for integration with payment systems and advanced analytics.

License

Private project - not for distribution

Remember: This app is for harm reduction and self-awareness, not medical advice. Always drink responsibly and never drive under the influence.
