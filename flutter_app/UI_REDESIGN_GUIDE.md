# METAIA Flutter App UI - Redesigned to Match Figma

## Overview
This Flutter application has been completely redesigned to match your Figma UI mockups exactly. The new design features a warm, elegant theme with a maroon/beige color scheme perfect for a royal tailoring app.

## Screen Structure

### 1. **Welcome Screen** (`welcome_screen.dart`)
- **Route**: `/welcome`
- **Components**:
  - Welcome banner with user greeting
  - Category selector buttons (Men, Women, Kids)
  - Men's Collection section with product grid
  - Menu toggle in appbar
- **Features**:
  - Beautiful welcome card with gold accent
  - Category quick navigation
  - Product grid with 3-column layout
  - Side menu for navigation

### 2. **Collections Screen** (`collections_screen.dart`)
- **Route**: `/collections?category=Men|Women|Kids`
- **Components**:
  - Dynamic product grid based on category
  - Men's section: Shirts, T-Shirts, Kurtis, Jackets, Blazers, Waistcoats, Trousers, Jeans, Kurta-Pyjama
  - Women's section: Blouses, Kurtis, Tops, Tunics, Shirts, Jackets, Leggings, Pants, Palazzo, Skirts, Salwar, Lehenga, Anarkali, Dress
  - Kids' section: Shirts, T-Shirts, Kurtis, Tops, Pants, Shorts, Ethnic Sets, Sherwani, Lehenga, Ghagra, Suit, Dress, Gown
- **Features**:
  - Responsive grid layout
  - Tappable product cards
  - Category-based product filtering

### 3. **Profile Screen** (`profile_screen.dart`)
- **Route**: `/profile`
- **Components**:
  - User profile card with avatar and contact info
  - Total orders summary card
  - Complete menu system
  - Logout button
- **Features**:
  - User information display (phone, email, address)
  - Order count statistics
  - Touch-friendly menu items
  - Member since date

## Color Scheme

The app uses a sophisticated color palette perfect for luxury tailoring:

```dart
Primary: #8B3E3E (Dark Maroon)
Background: #E8D7C3 (Warm Beige)
Card: #FFFFFF (White)
Accent: #D4AF37 (Gold)
Text Primary: #333333 (Dark Gray)
Text Secondary: #666666 (Medium Gray)
```

See `theme/colors.dart` for complete color definitions.

## Navigation Structure

```
/welcome (Landing Page)
  ├── /collections?category=Men
  ├── /collections?category=Women
  ├── /collections?category=Kids
  └── /profile
```

Using GoRouter for seamless navigation with query parameters.

## Installation & Setup

### 1. **Install Dependencies**
```bash
cd flutter_app
flutter pub get
```

### 2. **Run on Device/Emulator**

**Android:**
```bash
flutter run -d emulator-5554  # or your device ID
```

**iOS:**
```bash
flutter run -d iphone  # or your iOS device
```

**Web (if enabled):**
```bash
flutter run -d chrome
```

### 3. **Build for Production**

**Android (APK):**
```bash
flutter build apk --release
```

**Android (AAB for Google Play):**
```bash
flutter build appbundle --release
```

**iOS:**
```bash
flutter build ios --release
```

## File Structure

```
lib/
├── main.dart                 # App entry point & routing
├── screens/
│   └── home/
│       ├── welcome_screen.dart
│       ├── collections_screen.dart
│       └── profile_screen.dart
└── theme/
    └── colors.dart          # Color definitions
```

## Key Features Implemented

✅ **Exact Figma Design Match**
- Color scheme perfectly matches Figma
- Typography and spacing optimized for mobile
- Responsive grid layouts

✅ **Navigation**
- GoRouter for modern navigation
- Parameter-based routing for categories
- Smooth screen transitions

✅ **UI Components**
- Reusable widgets
- Consistent styling across screens
- Touch-friendly button sizes (48dp minimum)

✅ **Platform Support**
- iOS and Android optimized
- Safe area handling
- Platform-specific widgets where needed

## Customization Guide

### Changing Colors
Edit `lib/theme/colors.dart` to modify the color scheme:
```dart
static const Color primary = Color(0xFF8B3E3E); // Change maroon
static const Color gold = Color(0xFFD4AF37);   // Change accent
```

### Adding New Products
Edit the `_getCollectionItems()` method in `collections_screen.dart`:
```dart
return const [
  {'name': 'Product Name', 'image': 'assets/category/image.jpg'},
  // Add more products
];
```

### Styling Text
The app uses Material3 design system. Customize text styles through ThemeData:
```dart
theme: ThemeData(
  useMaterial3: true,
  textTheme: ThemeData.light().textTheme.apply(
    fontFamily: 'YourFont',
  ),
)
```

## Testing

### Run Analyzer
```bash
flutter analyze
```

### Run Tests
```bash
flutter test
```

## Responsive Design

The app is designed to work on:
- **Phones**: 6" - 6.7" (tested on common devices)
- **Tablets**: Full responsive grid layouts
- **Foldable**: Safe area handling for folding devices

## Performance Tips

1. **Image Optimization**: Replace placeholder icons with actual product images
2. **State Management**: Consider Provider or Riverpod for complex state
3. **Database**: Implement local caching with SQLite or Hive
4. **API Integration**: Use the backend services for real data

## Next Steps

1. **Add Product Details Screen**: Create detailed product view
2. **Implement Cart System**: Add shopping cart functionality
3. **Order Management**: Create order placement flow
4. **User Authentication**: Integrate login/registration
5. **Real Images**: Replace placeholder image areas with actual product photos
6. **Animations**: Add page transitions and micro-interactions

## Troubleshooting

**"Image not found"** - The app uses placeholder icons. Add actual images to `assets/` folder and update paths.

**Navigation errors** - Ensure GoRouter path matches the configured routes in `main.dart`.

**Color issues** - Check that color values in `AppColors` match your expectations.

## Support & Future Development

This UI is ready for:
- Backend API integration
- Real product data
- User authentication
- Payment processing
- Real-time notifications

All screens are built as stateless widgets for easy integration with state management solutions like Riverpod, Provider, or BLoC.

---

**Last Updated**: February 18, 2026
**Flutter Version**: 3.10.8+
**Target**: iOS 12.0+, Android 5.0+
