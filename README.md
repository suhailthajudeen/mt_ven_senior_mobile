# Flutter 5-Minute Coding Challenge

## Task: Implement Core Design Patterns

Implement these three essential Flutter patterns:
1. A `UserPreferences` singleton
2. A `PreferencesProvider` InheritedWidget 
3. Basic content filtering logic

```dart
import 'package:flutter/material.dart';

// Pre-defined model
enum ContentType { image, text, video }

class ContentItem {
  final String title;
  final ContentType type;
  final bool isExplicit;
  ContentItem({required this.title, required this.type, required this.isExplicit});
}

// TODO 1: Complete the UserPreferences singleton
class UserPreferences {
  // Make this a singleton (private constructor + static instance)
  static final UserPreferences _instance = UserPreferences._();
  factory UserPreferences() => _instance;
  UserPreferences._();
  
  // Add these properties:
  // 1. Set<ContentType> for allowed types (default: all types)
  // 2. bool for allowing explicit content (default: false)
  
  // Add these methods:
  // 1. toggleType(ContentType type)
  // 2. toggleExplicit()
}

// TODO 2: Complete the PreferencesProvider InheritedWidget
class PreferencesProvider extends InheritedWidget {
  // Add constructor with preferences and child
  
  // Expose the preferences
  
  // Implement updateShouldNotify
  
  // Add static 'of' method to access from context
}

// TODO 3: Complete the ContentFilter logic
class ContentFilter {
  // Complete this method to filter content based on preferences
  // Do NOT use built-in filter functions
  static List<ContentItem> filter(List<ContentItem> items, UserPreferences prefs) {
    final result = <ContentItem>[];
    
    // Filter content by:
    // 1. Content type must be in prefs.allowedTypes
    // 2. If content is explicit, prefs.allowExplicit must be true
    
    return result;
  }
}
```

**Evaluation Criteria:**
- Implementation of singleton pattern
- Correct InheritedWidget setup
- Working filtering logic
