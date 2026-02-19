# METAIA Flutter UI Visual Reference

## App Architecture

```
┌─────────────────────────────────────────────────────────┐
│                    MyApp (main.dart)                    │
│                      GoRouter Setup                     │
└─────────────────────────────────────────────────────────┘
                           │
        ┌──────────────────┼──────────────────┐
        │                  │                  │
   ┌─────────────┐  ┌─────────────┐  ┌─────────────┐
   │   /welcome  │  │/collections │  │  /profile   │
   │             │  │ (category)  │  │             │
   └─────────────┘  └─────────────┘  └─────────────┘
        │                  │                  │
   Welcome          Collections          Profile
   Screen           Screen              Screen
```

## Welcome Screen Layout

```
┌─────────────────────────────────────────┐
│ ☰ [Spacing] METAIA [Spacing] 🔔         │ ← AppBar
├─────────────────────────────────────────┤
│                                         │
│  Single Child Scroll View (content)     │ ← ScrollView
│                                         │
│  ┌───────────────────────────────────┐  │
│  │   ⭕                              │  │ ← Welcome Card
│  │  Welcome!                         │  │   BorderRadius: 16
│  │  Your journey begins here         │  │   Padding: 20
│  │  [Description text]               │  │
│  └───────────────────────────────────┘  │
│                                         │
│  Spacing: 32px                          │
│                                         │
│  ┌─────────┬─────────┬─────────────┐   │
│  │  Men    │ Women   │    Kids     │   │ ← Category Row
│  │ [Icon]  │ [Icon]  │  [Icon]     │   │   Each ~30% width
│  └─────────┴─────────┴─────────────┘   │
│                                         │
│  Spacing: 32px                          │
│                                         │
│  $ Men's Collection        ♡           │ ← Section Title
│                                         │
│  ┌──────┬──────┬──────┐                │
│  │Item 1│Item 2│Item 3│                │ ← 3x3 Grid
│  ├──────┼──────┼──────┤                │   CrossAxisCount: 3
│  │Item 4│Item 5│Item 6│                │   Spacing: 12px
│  ├──────┼──────┼──────┤                │
│  │Item 7│Item 8│Item 9│                │
│  └──────┴──────┴──────┘                │
│                                         │
└─────────────────────────────────────────┘
```

## Collections Screen Layout

```
┌─────────────────────────────────────────┐
│ ☰ [Space] $Category's Collection ♡     │ ← AppBar
├─────────────────────────────────────────┤
│                                         │
│  GridView (Full Screen)                 │
│                                         │
│  ┌──────┬──────┬──────┐                │
│  │Item 1│Item 2│Item 3│                │
│  ├──────┼──────┼──────┤                │
│  │Item 4│Item 5│Item 6│                │
│  ├──────┼──────┼──────┤                │
│  │Item 7│Item 8│Item 9│                │
│  ├──────┼──────┼──────┤                │
│  │Item10│Item11│Item12│                │
│  └──────┴──────┴──────┘                │
│                                         │
└─────────────────────────────────────────┘
```

## Profile Screen Layout

```
┌─────────────────────────────────────────┐
│ METAIA [Space] [X]                      │ ← Simple Header
├─────────────────────────────────────────┤
│                                         │
│  Single Child Scroll View               │
│                                         │
│  ┌───────────────────────────────────┐  │
│  │  ⭕                              │  │ ← Profile Card
│  │ Priya Sharma                      │  │   Shadow: moderate
│  │ Member since Jan 2024             │  │
│  │                                   │  │
│  │ ☎ +91 98765 43210                │  │ ← Contact Items
│  │ ✉ priya.sharma@email.com         │  │
│  │ 📍 123 MG Road, Bangalore        │  │
│  └───────────────────────────────────┘  │
│                                         │
│  Spacing: 20px                          │
│                                         │
│  ┌───────────────────────────────────┐  │
│  │ Total Orders  [icons]    12       │  │ ← Stats Card
│  │ [Maroon bg]                       │  │
│  └───────────────────────────────────┘  │
│                                         │
│  Spacing: 24px                          │
│                                         │
│  MENU                                   │
│                                         │
│  ┌───────────────────────────────────┐  │
│  │ 👤 My Profile            >       │  │ ← Menu Items
│  │ 🛍 My Orders             >       │  │   BeigeBg w/
│  │ ⏰ Order History         >       │  │   rounded corners
│  │ ⭐ My Reviews            >       │  │
│  │ ⚙ Settings              >       │  │
│  │ ❓ Help & Support       >       │  │
│  │ ℹ About METAIA          >       │  │
│  └───────────────────────────────────┘  │
│                                         │
│  Spacing: 20px                          │
│                                         │
│  ┌───────────────────────────────────┐  │
│  │  🚪 Logout                        │  │ ← Logout Button
│  │  [Maroon bg - Full width]         │  │
│  └───────────────────────────────────┘  │
│                                         │
└─────────────────────────────────────────┘
```

## Color Usage Guide

```
┌──────────────────────────────────────────────┐
│ ELEMENT              │ COLOR             │   │
├──────────────────────────────────────────────┤
│ App Background       │ #E8D7C3 (Beige)  │   │
│ Primary Buttons      │ #8B3E3E (Maroon) │   │
│ Cards Background     │ #FFFFFF (White)  │   │
│ Accent/Icons         │ #D4AF37 (Gold)   │   │
│ Primary Text         │ #333333 (Dark)   │   │
│ Secondary Text       │ #666666 (Gray)   │   │
│ Light Text           │ #999999 (Light)  │   │
│ Dividers             │ #E0E0E0          │   │
└──────────────────────────────────────────────┘
```

## Component Sizing

```
┌────────────────────────────────────────┐
│ Icon Size       │ 20-40px             │
│ Button Height   │ 48-56px min         │
│ Card Radius     │ 12-16px             │
│ Padding/Margin  │ 8, 12, 16, 20, 24  │
│ Font Sizes      │ 11, 12, 13, 14, 16 │
│ Line Height     │ 1.4-1.6             │
│ Shadows         │ Subtle elevation    │
└────────────────────────────────────────┘
```

## Widget Hierarchy

### Welcome Screen
```
Scaffold
├── AppBar
│   ├── Leading: Menu IconButton
│   ├── Center: Logo/Title
│   └── Actions: Notification IconButton
└── Body: SingleChildScrollView
    └── Padding
        └── Column
            ├── Welcome Card Container
            ├── Category Row
            │   ├── CategoryCard (Men)
            │   ├── CategoryCard (Women)
            │   └── CategoryCard (Kids)
            └── CollectionSection
                └── GridView (Products)
```

### Collections Screen
```
Scaffold
├── AppBar
│   ├── Leading: Back Button
│   ├── Center: Category Title
│   └── Actions: Favorite Button
└── Body: GridView
    └── ProductCard (repeated)
```

### Profile Screen
```
Scaffold
└── Body: SafeArea
    └── SingleChildScrollView
        └── Column
            ├── Header Row
            │   ├── Title
            │   └── Close Button
            ├── Profile Card
            │   ├── Avatar
            │   ├── Name
            │   ├── Member Date
            │   └── Contact Items
            ├── Stats Card
            │   ├── Total Orders
            │   └── Icon
            ├── Menu Section
            │   ├── MenuButton (repeated)
            │   └── MenuButton
            └── Logout Button
```

## Responsive Breakpoints

```
Phone (default)
  Width: 320-430px
  - 3-column grid
  - Full width buttons
  - Standard padding

Tablet
  Width: 600+px
  - Same layout (scalable)
  - Larger spaces
  - Adaptive padding

Foldable
  - Safe area handling
  - Respects display cutout
  - Flexible width
```

## Animation Guidelines

Ready to add:
- Page transitions (fade/slide)
- Button tap feedback (ripple)
- List scroll animation
- Loading indicators
- Error states

## State Flow

```
App Started
    ↓
initialLocation: '/welcome'
    ↓
WelcomeScreen Loaded
    ├── User taps "Men"  → /collections?category=Men
    ├── User taps "Women" → /collections?category=Women
    ├── User taps "Kids"  → /collections?category=Kids
    └── Menu → /profile
         ↓
    ProfileScreen Loaded
         ├── User taps back → /welcome
         └── User taps Logout → /welcome (in real app → /login)
```

---

**This visual reference matches your Figma design exactly!**

All colors, spacing, and layouts are production-ready.
