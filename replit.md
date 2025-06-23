# MeritMint - Mobile Student Engagement Platform

## Overview

MeritMint is a React Native mobile MVP for a points-based student engagement platform designed specifically for Indian colleges. The app gamifies student behavior through academic achievements, attendance tracking, cultural activities, sports, and volunteering. It supports three user roles: students, faculty, and administrators, with intuitive mobile-first design following principles from "Don't Make Me Think", "Building a StoryBrand", and "The Design of Everyday Things".

## System Architecture

### Mobile Frontend Architecture
- **Framework**: React Native with TypeScript
- **Platform**: Expo (deployable to iOS and Android)
- **UI Framework**: React Native Elements/NativeBase for mobile-optimized components
- **Styling**: StyleSheet with responsive design and accessibility
- **State Management**: React Query for server state + React Context for app state
- **Navigation**: React Navigation for mobile navigation patterns
- **Forms**: React Hook Form with mobile-optimized inputs

### Backend Architecture (API Server)
- **Runtime**: Node.js with Express.js framework serving as API backend
- **Language**: TypeScript with ES modules
- **Session Management**: Express sessions with PostgreSQL storage
- **Authentication**: Token-based authentication for mobile clients with bcrypt password hashing
- **API Design**: RESTful APIs optimized for mobile consumption with role-based access control

### Database Architecture
- **Database**: PostgreSQL with Neon serverless driver
- **ORM**: Drizzle ORM with TypeScript-first schema definitions
- **Schema Location**: Shared schema in `/shared/schema.ts` for type consistency
- **Migrations**: Drizzle Kit for database migrations and schema management

## Key Mobile App Features

### Student App Features (Complete Implementation)
- **Secure Authentication**: Login/signup with college email validation
- **Dashboard Overview**: Total points breakdown by category (Academic/Cultural/Sports/Volunteering)
- **Points History**: Detailed transaction history with filtering by category
- **Reward Catalog**: Browse and redeem rewards with real-time inventory
- **Profile Management**: View achievements, badges, and account settings
- **Notifications**: Real-time updates for points earned and system messages

### Faculty App Features (Complete Implementation)
- **Faculty Dashboard**: Overview of students, points assigned, and pending approvals
- **Assign Points**: Intuitive form to award points with category selection and guidelines
- **Student Management**: Browse and search all department students
- **Point Guidelines**: Built-in recommendations for fair point distribution
- **Activity Tracking**: View recent point assignments and student progress

### Admin Panel Features (Complete Implementation)
- **System Dashboard**: Overview of total users, points awarded, and platform usage
- **User Management**: Add/remove students and faculty with role-based permissions
- **Reward Management**: Create, edit, and manage reward catalog with inventory
- **Department Analytics**: View statistics by department and user activity
- **System Administration**: Platform configuration and user oversight

### Mobile-First Design Principles
- **Intuitive UX**: Following "Don't Make Me Think" principles with clear navigation
- **Clear User Journey**: Implementing "Building a StoryBrand" framework for engagement
- **Usable Feedback**: Every interaction provides immediate visual feedback
- **Clean UI**: Minimal design inspired by "The Futur" with education-focused branding

## Mobile App Data Flow

1. **Authentication Flow**: User opens app → Login/signup screen → Token stored locally → Role-based navigation
2. **Points Assignment**: Faculty selects student → Chooses category → Enters details → API call → Real-time updates
3. **Reward Redemption**: Student browses catalog → Selects reward → Point balance verified → Redemption confirmed
4. **Real-time Sync**: React Query handles API calls → AsyncStorage for offline persistence → Automatic UI updates

## Mobile App Dependencies

### Core Mobile Dependencies
- **expo**: React Native development platform and build system
- **react-native**: Cross-platform mobile framework
- **@react-navigation/native**: Mobile navigation system with stack and tab navigators
- **@tanstack/react-query**: Server state management optimized for mobile
- **axios**: HTTP client for API communication
- **@react-native-async-storage/async-storage**: Local storage for authentication tokens

### Mobile UI Dependencies
- **react-native-elements**: Mobile UI component library
- **react-native-paper**: Material Design components for React Native
- **react-native-vector-icons**: Icon system for mobile interfaces
- **react-native-gesture-handler**: Touch gesture system
- **react-native-reanimated**: High-performance animations

### Backend API Dependencies
- **@neondatabase/serverless**: PostgreSQL database connection
- **drizzle-orm**: TypeScript ORM for data management
- **express**: API server framework
- **bcrypt**: Password hashing for security

## Deployment Strategy

### Mobile App Development
- **Development**: `cd mobile && expo start` for local development with Expo CLI
- **iOS Deployment**: `expo build:ios` for App Store distribution
- **Android Deployment**: `expo build:android` for Google Play Store
- **Expo Platform**: Deployable to both iOS and Android via Expo managed workflow

### Backend API Server
- **Development**: `npm run dev` - Express API server with hot reload
- **Database**: Neon PostgreSQL with environment-based configuration
- **Port**: 5000 (API endpoint for mobile app)
- **Production**: `npm run start` - Optimized API server for mobile clients

### Integration Architecture
- **Mobile App**: React Native Expo app consuming REST APIs
- **API Backend**: Express server providing mobile-optimized endpoints
- **Database**: Shared PostgreSQL database via Drizzle ORM
- **Authentication**: Token-based auth suitable for mobile platforms

### Replit Configuration
- **Primary**: Mobile app development environment
- **Backend**: API server running on port 5000
- **Database**: PostgreSQL-16 for data persistence
- **Deployment**: Expo managed workflow for app stores

## Changelog

```
Changelog:
- June 23, 2025. Complete transformation to React Native mobile MVP
  * Built comprehensive React Native mobile app structure with Expo
  * Implemented multi-role authentication system for mobile (Student/Faculty/Admin)
  * Created role-specific mobile screens with intuitive navigation
  * Built student features: dashboard, points history, rewards catalog, profile
  * Built faculty features: dashboard, point assignment, student management
  * Built admin features: system dashboard, user management, reward management
  * Implemented mobile-optimized UI with touch-friendly interactions
  * Added React Navigation with bottom tabs and stack navigation
  * Created theme context and responsive mobile design system
  * Added notification system and mobile-first user experience
  * Successfully transformed from web platform to mobile-first architecture
```

## User Preferences

```
Preferred communication style: Simple, everyday language.
```