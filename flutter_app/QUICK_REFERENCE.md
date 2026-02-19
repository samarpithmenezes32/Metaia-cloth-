# METAIA Flutter UI - Quick Reference

## 🚀 Quick Start

```bash
# Navigate to project
cd flutter_app

# Get dependencies
flutter pub get

# Run on device
flutter run
```

## 📱 Routes

| Route | Screen | Purpose |
|-------|--------|---------|
| `/welcome` | Welcome | Landing page with categories |
| `/collections?category=Men` | Collections | Men's products |
| `/collections?category=Women` | Collections | Women's products |
| `/collections?category=Kids` | Collections | Kids' products |
| `/profile` | Profile | User profile & menu |

## 🎨 Colors Quick Ref

```dart
AppColors.primary        // #8B3E3E (Dark Maroon) - Main color
AppColors.background    // #E8D7C3 (Beige) - Background
AppColors.cardBackground// #FFFFFF (White) - Card bg
AppColors.gold          // #D4AF37 - Accent
AppColors.textPrimary   // #333333 - Main text
```

## 📦 Key Files

| File | Purpose |
|------|---------|
| `main.dart` | App entry point & routing |
| `screens/home/welcome_screen.dart` | Welcome/landing page |
| `screens/home/collections_screen.dart` | Product grid |
| `screens/home/profile_screen.dart` | User profile |
| `theme/colors.dart` | All colors defined |

## 💡 Widget Structure

### WelcomeScreen
- Welcome card
- Category buttons (Men/Women/Kids)
- Horizontal menu in appbar
- Product grid

### CollectionsScreen
- Appbar with back button
- 3-column grid
- All products per category
- Tappable cards

### ProfileScreen
- Profile header card
- Contact info
- Order stats card
- Menu items list
- Logout button

## 🔄 Navigation Example

```dart
// From welcome to collections
context.go(
  '/collections',
  extra: {'category': 'Men'},
);

// From any screen to profile
context.go('/profile');

// Back
context.pop();
```

## 🎯 Important Notes

1. **No Images**: Replace `Icon(Icons.image)` with actual product images
2. **Mock Data**: Product names are hardcoded - connect to API later
3. **Stateless**: All screens are stateless - perfect for state management
4. **No Authentication**: Add auth in integration phase
5. **No Backend**: Mock data only - ready for API integration

## ⚡ Common Customizations

### Change Primary Color
```dart
// In colors.dart
static const Color primary = Color(0xFF8B3E3E);  // Change this hex
```

### Add New Product
```dart
// In collections_screen.dart
return const [
  {'name': 'New Item', 'image': 'assets/path.jpg'},
  // ...
];
```

### Modify Text Style
```dart
Text(
  'Hello',
  style: TextStyle(
    fontSize: 16,
    fontWeight: FontWeight.bold,
    color: AppColors.primary,
  ),
)
```

## 📊 Screen Breakdown

### Welcome Screen
- Navigation: Menu + Profile link
- Content: Welcome card + Category buttons + Product grid
- Actions: Browse by category

### Collections Screen
- Navigation: Back button
- Content: Category header + 3-column product grid
- Actions: Select product (ready for detail screen)

### Profile Screen
- Navigation: Back button
- Content: User info + Stats + Menu + Logout
- Actions: Menu navigation + Logout

## 🛠 Development Tips

1. **Grid Layout**: Use `GridView.builder` for dynamic grids
2. **Navigation**: GoRouter provides named routes
3. **Styling**: All colors in `AppColors` class
4. **Spacing**: Use 8px multiples (8, 12, 16, 20, 24)
5. **Icons**: Material Icons available by default

## ⚠️ Limitations (by Design)

- No backend API integration yet
- No user authentication
- No cart/checkout flow
- No real images
- No animations/transitions
- No database storage

## 📈 Next Phase

Add these to complete the app:

1. ✅ UI Complete
2. 🔴 Product details screen
3. 🔴 Shopping cart
4. 🔴 Checkout flow
5. 🔴 User authentication
6. 🔴 Backend integration
7. 🔴 Payment processing
8. 🔴 Order tracking
9. 🔴 Real product images
10. 🔴 Animations

## 🧪 Testing

```bash
# Check code quality
flutter analyze

# Run tests
flutter test

# Build APK
flutter build apk --release
```

## 📞 Documentation

- Full guide: See `UI_REDESIGN_GUIDE.md`
- Summary: See `REDESIGN_SUMMARY.md`
- Code: Comments in each screen file

---

**Made for METAIA** - Premium Tailoring App  
**Version**: 1.0.0 | **Updated**: Feb 2026
