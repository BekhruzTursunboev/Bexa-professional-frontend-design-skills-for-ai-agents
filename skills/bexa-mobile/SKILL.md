---
name: bexa-mobile
description: >
  Premium mobile UI skill for React Native and Expo apps.
  Enforces native-grade interaction patterns, platform-specific motion,
  gesture physics, and non-generic visual systems for iOS and Android.
version: 1.2.0
---

# FORGE MOBILE — Native-Grade Mobile Design Skill

> Designing for a human holding glass with their thumbs.
> Every decision — padding, font, tap target, animation — must honor that physical reality.

---

## DIAL CONFIGURATION

```
NATIVE_FIDELITY:  8   (1=Web-wrapper / 10=Indistinguishable from OS)
GESTURE_DEPTH:    7   (1=Tap only / 10=Physics swipe, pinch, long-press)
VISUAL_RICHNESS:  6   (1=Minimal / 10=Rich depth layers)
```

---

## SECTION 1 — MOBILE-FIRST CONSTRAINTS

**Thumb Zone:** Primary actions in bottom 40% of screen. Destructive actions top. NO hamburger menus.

**Touch Targets:**
- Minimum: 44×44pt (iOS) / 48×48dp (Android)
- Visual can be smaller; hitbox must be padded to minimum
- Min 8pt gap between adjacent targets

**Safe Areas:** Always use `SafeAreaView`. Bottom: 34pt for home indicator. Never place critical content in top 59pt (Dynamic Island zone).

---

## SECTION 2 — TYPOGRAPHY MOBILE SCALE

| Level | Size (pt/sp) | Weight |
|---|---|---|
| Display | 34 | 700 |
| Title 1 | 28 | 700 |
| Title 2 | 22 | 600 |
| Headline | 17 | 600 |
| Body | 17 | 400 |
| Footnote | 13 | 400 |
| Caption | 12 | 400 |

**Font selection:** `Sora` + `DM Sans` for iOS feel. `Plus Jakarta Sans` + `Geist` for Android feel. Never system defaults only.

---

## SECTION 3 — GESTURE PHYSICS

When `GESTURE_DEPTH >= 5`: use `react-native-reanimated` + `react-native-gesture-handler`. Never `PanResponder`.

**Spring configuration:**
```js
// Premium iOS-like spring
const spring = { damping: 15, stiffness: 150, mass: 0.8 };
// Snappy confirmation
const snap   = { damping: 20, stiffness: 300, mass: 0.5 };
```

**Haptics:** Every state change triggers haptic feedback.
- Button press → `ImpactFeedbackStyle.Light`
- Success → `NotificationFeedbackType.Success`
- Error → `NotificationFeedbackType.Error`
- Drag threshold → `ImpactFeedbackStyle.Medium`

---

## SECTION 4 — PLATFORM MOTION

**iOS:** Sheets slide up from bottom with spring. Navigation push slides at 85% finger speed. Action completion scales to 0.95 → overshoot release.

**Android:** Material You ripple on all pressables. `BottomSheetModal` with snapPoints `['40%','70%','95%']`. Shared element transitions on list→detail.

**Universal:**
- Loading: shimmer skeleton matching exact content layout
- Pull-to-refresh: liquid droplet — NOT a spinner
- Scroll: honor platform physics, never hard-stop

---

## SECTION 5 — COLOR SYSTEM (MOBILE)

```
Light — Surface: hsl(220 14% 98%) | Card: hsl(0 0% 100%)
Dark  — Surface: hsl(220 20%  8%) | Card: hsl(220 20% 12%)
OLED  — Background: hsl(0 0% 0%) | Cards remain hsl(220 20% 8%)
```

Accent: same rules as FORGE core (1 accent, sat ≤ 75%, no AI purple).

---

## SECTION 6 — PERFORMANCE MANDATES

- **Images:** `expo-image` or `FastImage`. Never plain `<Image>` in lists.
- **Lists:** `FlashList` with `estimatedItemSize`. `FlatList` only for < 50 items.
- **Animations:** `useSharedValue` + `useAnimatedStyle` (Reanimated 3). JS thread animations = BANNED.
- **Re-renders:** `React.memo` all list items. `useCallback` all handlers passed as props.
- **Network:** Cache responses. Show stale data + refresh indicator, never blank screen.
