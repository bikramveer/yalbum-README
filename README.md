# YALBUM - Private Photo Sharing Platform

A secure, invitation-only photo sharing application for private groups to collaboratively organize and share memories.

<div align="center">
  
[![iOS App Store](https://img.shields.io/badge/Download-App%20Store-0D96F6?logo=apple&logoColor=white&style=for-the-badge)](https://apps.apple.com/us/app/yalbum-photo-albums/id6760424577)
[![Web App](https://img.shields.io/badge/Try-Web%20App-14B8A6?logo=google-chrome&logoColor=white&style=for-the-badge)](https://yalbum.netlify.app/)
<!-- [![Android](https://img.shields.io/badge/Coming%20Soon-Google%20Play-gray?logo=google-play&logoColor=white&style=for-the-badge)](#) -->

<!-- **Or try the [Web App](https://your-app-url.com) →** -->

</div>

---

## Demo Account

**Try it out with read-only access:**
- Email: `test@test.com`
- Password: `123456`

*Note: Demo accounts can view all features but cannot upload photos or create albums. [Sign up for free](#) to try full functionality.*

## Features

### Security & Privacy
- Row-level security (RLS) policies across all database tables
- Private storage buckets with cryptographically signed URLs
- JWT-based authentication with automatic session refresh
- Album members can only view photos from albums they're invited to

### Photo Management
- Upload multiple photos from device gallery
- Organize photos into custom folders with color-coding
- Bulk operations: select, move, download, and delete multiple photos
- Smart downloads: individual files (1-9 photos) or automatic ZIP bundling (10+)
- Pull-to-refresh to update photo grid

### Collaboration
- Create unlimited private albums with custom themes
- Generate secure 6-character invite codes (7-day expiry)
- Role-based permissions (owners vs. members)
- Real-time commenting system with nested replies
- See who uploaded each photo with timestamps

### User Experience
- Responsive mobile-first design
- Custom confirmation modals and toast notifications
- Automatic photo refresh when returning to albums
- Remove photos from upload queue before submitting

## Tech Stack

**Frontend:**
- Next.js 14 (App Router)
- TypeScript
- Tailwind CSS
- React Hooks

**Backend:**
- Supabase (PostgreSQL database)
- Supabase Auth (JWT authentication)
- Supabase Storage (S3-compatible)

**Mobile:**
- React Native with Expo
- Same Supabase backend
- Native photo picker integration

## Architecture Highlights

- **Multi-tenant data isolation** through PostgreSQL RLS policies
- **Secure file storage** with private buckets and signed URLs (24-hour expiry)
- **Pre-generated signed URLs** during batch fetches (60% reduction in API calls)
- **Optimized database queries** with eager-loaded user profiles
- **Invite code system** with expiry tracking and usage limits

## Development Journey

This project involved:
- Architecting comprehensive RLS policies to prevent unauthorized data access
- Debugging complex authentication failures by isolating JWT validation and session management
- Implementing intelligent download logic that adapts based on selection size
- Building a React Native mobile app that shares the same backend infrastructure

## Deployment

- **Web App:** Deployed on Netlify with automatic CI/CD
- **Database:** Hosted on Supabase cloud platform
- **Mobile App:** Built with Expo EAS, available on TestFlight

## Screenshots

## License

MIT

## Contact

Bikramveer Gill - [LinkedIn](https://www.linkedin.com/in/bikramveer-gill/)
