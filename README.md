SkillBridge-Cybersecurity-E-Learning-Platform

  Overview

  The SkillBridge-Cybersecurity-E-Learning-Platform is an interactive educational platform that offers courses in
  cybersecurity, data structures & algorithms, cryptography, and networking. The portal features secure Google
  authentication, interactive visualizations, and a structured learning experience.

  Technology Stack

  - Backend: Django
  - Frontend: HTML, CSS, JavaScript, Bootstrap
  - Database: Google Firestore
  - Storage: Google Cloud Storage
  - Authentication: Google OAuth 2.0 with JWT token management
  - Payment Integration: Razorpay

  Key Features

  Authentication System

  - Google OAuth 2.0 integration for secure login
  - JWT token management for persistent sessions
  - In-app browser detection to prevent OAuth flow issues

  Interactive Learning Modules

  Data Structures & Algorithms

  - Binary Search: Step-by-step visualization with complexity analysis
  - Linear Search: Interactive search algorithm demonstration
  - Sorting Algorithms: Bubble sort and selection sort with animated steps
  - Linked List: Canvas-based implementation with add, delete, and search operations
  - Stack: Comprehensive visualization of push, pop, and peek operations

  Cryptography

  - Substitution Cipher: Interactive encryption with key selection
  - Rail Fence Cipher: Visual demonstration of transposition techniques
  - Row-Column Cipher: Matrix-based encryption visualization
  - Vigenere Cipher: Polyalphabetic substitution demonstration
  - AES-ECB Mode: Block cipher visualization

  Networking

  - TCP Three-Way Handshake: Animated demonstration of connection establishment
  - UDP Communication: Visualization of connectionless communication

  SkillBridge Program

  - Structured learning paths for comprehensive skill development
  - Progress tracking and certification
  - Hands-on projects and assessments

  Course Management

  - Self-paced courses with progress tracking
  - Live and on-demand workshop categories
  - Free resources section for beginners
  - Certificate generation for completed courses

  Architecture

  The application follows a Django-based MVC architecture with:
  - Views handling request processing and template rendering
  - Firebase Firestore for data storage
  - Google Cloud Storage for file storage
  - Client-side JavaScript for interactive visualizations

  Setup and Installation

  Prerequisites

  - Python 3.8+
  - Django 4.2+
  - Google Cloud Platform account with Firestore enabled
  - Google OAuth credentials

  Environment Variables

  GOOGLE_TOKEN_ENDPOINT=https://oauth2.googleapis.com/token
  GOOGLE_USERINFO_ENDPOINT=https://www.googleapis.com/oauth2/v1/userinfo
  REDIRECT_URI=<your-redirect-uri>
  OAUTH_CLIENT_ID=<your-client-id>
  OAUTH_CLIENT_SECRET=<your-client-secret>
  GCP_PROJECT_ID=<your-gcp-project-id>
  RAZORPAY_KEY=<your-razorpay-key>
  RAZORPAY_SECRET=<your-razorpay-secret>
  BUCKET_NAME=<your-gcs-bucket-name>
  SKILLBRIDGE_APPLICATIONS_BUCKET=<your-applications-bucket-name>

  Installation Steps

  1. Clone the repository
  2. Install dependencies: pip install -r requirements.txt
  3. Set up environment variables
  4. Run migrations: python manage.py migrate
  5. Start the server: python manage.py runserver

  Implementation Details

  Authentication Flow

  1. User clicks "Sign in with Google" button
  2. Frontend initiates OAuth flow via Google's authentication endpoint
  3. On successful authentication, Google redirects to the callback URL with an authorization code
  4. Backend exchanges the code for access token via Google Token API
  5. User information is retrieved from Google's UserInfo endpoint
  6. JWT token is generated for the user and stored as a cookie
  7. User session is maintained via JWT verification on subsequent requests

  Interactive Visualizations

  All visualizations use vanilla JavaScript for DOM manipulation and animations:
  - Canvas-based rendering for complex visualizations (linked list)
  - CSS transitions for smooth animation effects
  - Dynamic content generation based on user input
  - Step-by-step execution with variable speed control

  Contributors

  - Cyberforge Academy Development Team

  License

  This project is proprietary and confidential.

  ---
  Note: This platform is designed to make learning technical subjects more engaging and effective through
  visualization and hands-on practice.
