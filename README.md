# EduMerge

A React + Tailwind CSS web application for curating, organizing, and playing distraction-free YouTube educational playlists.

## Features

- **Curated Playlist Management:** Create, edit, and delete topic-based video playlists (`CreatePlaylist`, `EditPlaylist`, `DeletePlaylist`).
- **Drag-and-Drop Reordering:** Reorder video links inside a playlist using `react-beautiful-dnd`.
- **Custom YouTube Player:** Sequential video playback powered by the YouTube IFrame Player API with next/previous navigation, playback speed controls, and a synced playlist queue (`VideoPlayer`).
- **Authentication & Account Controls:** Sign up, log in, update profile details, change password, and delete account (`/auth`, `/user/*`).

## Tech Stack

- **Frontend:** React 18, React Router v6, Tailwind CSS
- **HTTP & State:** Axios, `localStorage` session handling
- **UI & Media:** YouTube IFrame Player API, `react-beautiful-dnd`, `react-icons`, GSAP, AOS, Typed.js
- **Testing:** React Testing Library, Jest (`react-scripts test`)

## Project Structure

```text
src/
├── App.js                  # BrowserRouter routes & global scroll/progress components
├── auth.jsx                # localStorage-based auth check (isAuthenticated)
└── components/
    ├── AuthForm.jsx        # Login & registration form
    ├── Landingpage/        # Landing page sections (Hero, About, Features, Testimonials, CTA)
    └── dashboard/          # UserDashboard, Create/Edit/DeletePlaylist, VideoPlayer, Account settings
```

## Routes

| Path | Component | Description |
| :--- | :--- | :--- |
| `/` | `LandingPage` | Public marketing and overview page |
| `/auth` | `AuthForm` | User sign-in and registration |
| `/user/dashboard` | `UserDashboard` | Main playlist dashboard |
| `/user/create-playlist` | `CreatePlaylist` | Create and reorder a new playlist |
| `/edit-playlist/:playlistId` | `EditPlaylist` | Update an existing playlist |
| `/delete-playlist/:playlistId` | `DeletePlaylist` | Delete a playlist |
| `/video-player/:playlistId` | `VideoPlayer` | YouTube IFrame playlist player |
| `/user/update-profile` | `UpdateProfile` | Edit user profile details |
| `/user/change-password` | `ChangePassword` | Update account password |
| `/user/delete-account` | `DeleteAccount` | Permanently delete user account |

## Getting Started

### Prerequisites

- Node.js 18+ and npm

### Installation & Local Development

```bash
git clone [https://github.com/Akshith8978/EduMerge.git](https://github.com/Akshith8978/EduMerge.git)
cd EduMerge
npm install
npm start
```

The app runs on port `3000` in development mode and connects to the hosted backend API.

### Available Scripts

- `npm start` — Run the development server
- `npm test` — Launch the Jest / React Testing Library runner
- `npm run build` — Build the production bundle to `build/`

## License

MIT