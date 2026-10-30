---
keywords: mobile-first, ux-design, ui-design, performance, best-practices, responsive
---

mobile-design
When to use: Mobile-first design thinking for iOS/Android apps, React Native, or Flutter. Touch interaction, platform conventions, performance patterns.

Core Philosophy
Touch-first. Battery-conscious. Platform-respectful. Offline-capable. Mobile is NOT a small desktop.

ALWAYS Ask Before Assuming
Platform target? (iOS / Android / both)
Framework? (React Native / Flutter / native)
Offline support required?
Performance constraints?
Touch Interaction Principles
Minimum touch target: 44×44px (iOS HIG) / 48×48dp (Material)
Thumb zone: bottom 2/3 of screen is comfortable reach
Swipe vs tap: use tap for primary actions, swipe for secondary
Haptics: light for selections, medium for confirmations, heavy for errors
No hover-dependent interactions (hover doesn't exist on touch)
Platform Conventions
iOS: Back gesture (swipe right), bottom tab bar, SF Pro font, system colors Android: Bottom navigation or nav drawer, Roboto/Google Sans, Material You dynamic color

Performance Rules
60fps minimum (16ms frame budget)
Lists: FlatList with getItemLayout and keyExtractor; virtualization always on
Images: cache aggressively, use resizeMode, never load full-resolution unnecessarily
JS thread vs UI thread — heavy ops belong on background threads
Bundle splitting for large apps
Reference Files (read before implementing)
For deep implementation detail, reference files in the mobile-design skill:

mobile-design-thinking.md — forces intentional thinking over defaults
touch-psychology.md — Fitts' Law, gestures, haptics
platform-ios.md / platform-android.md — platform-specific patterns
mobile-performance.md — 60fps, memory management