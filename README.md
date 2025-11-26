# WorkWise Recruitment Platform

A modern, responsive React application for BPO and Virtual Assistant recruitment in the Philippines. WorkWise connects job seekers with employers through free training programs, job listings, and direct application processes.

## Features

- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Multi-Section Navigation**: Home, Job Board, Free Training, Events, and Application
- **Splash Screen**: Engaging loading animation
- **Job Listings**: Browse available BPO and VA positions with detailed information
- **Free Training Programs**: Access to skill development courses
- **Event Calendar**: Upcoming recruitment drives and workshops
- **Application Form**: Direct application submission
- **Modern UI**: Clean, professional design with smooth animations

## Tech Stack

- **Frontend**: React 18 with Hooks
- **Styling**: Tailwind CSS
- **Icons**: Lucide React
- **Build Tool**: Create React App

## Installation

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn

**Windows PowerShell Setup**: If you encounter script execution errors, enable PowerShell script execution:
  ```powershell
  Set-ExecutionPolicy RemoteSigned -Scope Process
  ```
  This sets the execution policy for the current process session.

### Setup

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd workwise-frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm start
   ```

4. Open [http://localhost:3000](http://localhost:3000) in your browser and On Your Network:  http://192.168.1.57:3000

### Build for Production

```bash
npm run build
```

This creates an optimized production build in the `build` folder.

## Usage

The application consists of five main sections:

### Home
- Hero section with call-to-action buttons
- Key statistics and features overview
- Background images and gradient overlays

### Job Board
- Browse available job openings
- Filter by work type (WFH, On-site)
- View salary ranges, locations, and requirements
- Direct application links

### Free Training
- Access to WorkWise Academy courses
- Course details including duration, level, and start dates
- Enrollment buttons linking to application

### Events
- Calendar view of upcoming events
- Event types: Recruitment, Training, Networking
- Location and time details

### Apply Now
- Application form with required fields
- Resume upload instructions
- Privacy policy acknowledgment

## Customization Guide

### Content Customization

All content is currently hardcoded in `src/WorkWise.jsx`. To customize the application:

#### 1. Job Listings

Edit the `JOBS` array (lines 21-58):

```javascript
const JOBS = [
  {
    id: 1,
    title: "Your Job Title",
    type: "BPO - Voice", // or "WFH - VA", "BPO - Chat/Email", etc.
    location: "Location / Hybrid",
    salary: "Salary Range",
    tags: ["Tag1", "Tag2"], // e.g., ["Night Shift", "HMO Day 1"]
    description: "Job description text"
  },
  // Add more jobs...
];
```

#### 2. Training Courses

Edit the `COURSES` array (lines 60-88):

```javascript
const COURSES = [
  {
    id: 1,
    title: "Course Name",
    duration: "Duration", // e.g., "2 Weeks"
    level: "Beginner", // Beginner, Intermediate, All Levels
    dates: "Start dates", // e.g., "Every Monday"
    image: "bg-color-class", // Tailwind background class
    desc: "Course description"
  },
  // Add more courses...
];
```

#### 3. Events

Edit the `EVENTS` array (lines 90-118):

```javascript
const EVENTS = [
  {
    id: 1,
    day: "15", // Day of month
    month: "NOV", // Month abbreviation
    title: "Event Title",
    time: "Time range", // e.g., "9:00 AM - 5:00 PM"
    location: "Location",
    type: "Recruitment" // Recruitment, Training, Networking
  },
  // Add more events...
];
```

#### 4. Hero Section Content

Edit the hero section in `HomeView` (lines 178-211):

- Change the main heading
- Update subtitle text
- Modify call-to-action button text
- Replace background image URL

#### 5. Statistics Section

Edit the stats array in `HomeView` (lines 226-239):

```javascript
{ title: "Your Stat", sub: "Description", icon: <IconComponent /> }
```

#### 6. Footer Information

Edit footer content (lines 525-557):

- Company description
- Contact information
- Quick links

#### 7. Branding

- **Logo/Icon**: Change the briefcase icon or add custom logo
- **Colors**: Modify Tailwind classes for color scheme
- **Typography**: Adjust font sizes and weights

### Styling Customization

#### Tailwind Configuration

Edit `tailwind.config.js` to customize the design system:

```javascript
module.exports = {
  theme: {
    extend: {
      colors: {
        // Add custom colors
      },
      fontFamily: {
        // Add custom fonts
      }
    }
  }
}
```

#### CSS Classes

- Use Tailwind utility classes throughout the component
- Custom animations are defined using Tailwind's animation utilities
- Responsive breakpoints: `sm:`, `md:`, `lg:`

### Adding New Sections

1. Add new navigation item to `navItems` array
2. Create new view component (e.g., `NewView`)
3. Add conditional rendering in the main component
4. Update navigation handlers

### Images and Assets

- Background images are currently from Unsplash
- Replace with local assets by placing images in `public/` folder
- Update image paths in the component

### Data Integration

For production use, consider:

1. **API Integration**: Replace hardcoded data with API calls
2. **State Management**: Use Redux or Context API for complex state
3. **Database**: Connect to a backend service for dynamic content

## Development

### Available Scripts

- `npm start` - Start development server
- `npm test` - Run tests
- `npm run build` - Create production build
- `npm run eject` - Eject from Create React App (irreversible)

### Project Structure

```
workwise-frontend/
├── public/
│   ├── index.html          # Main HTML template
│   └── ...                 # Static assets
├── src/
│   ├── WorkWise.jsx        # Main application component
│   ├── index.jsx           # Application entry point
│   ├── index.css           # Global styles
│   └── ...                 # Additional components
├── package.json            # Dependencies and scripts
├── tailwind.config.js      # Tailwind configuration
└── README.md              # This file
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

© 2024 WorkWise Philippines. All rights reserved.

## Support

For support or inquiries:
- Email: careers@workwise.ph
- Phone: (02) 8123-4567
- Address: Ayala Ave, Makati City