# FileFlowPro

FileFlowPro is a comprehensive file analysis and visualization platform that allows users to upload, analyze, and generate interactive charts from various file formats, particularly Excel files. The application features user authentication, role-based access control (user, admin, super-admin), and a modern React-based interface.

## Features

- **File Upload & Analysis**: Support for Excel and other file formats
- **Interactive Charts**: Generate and customize charts using Recharts
- **User Management**: Authentication with Passport.js and role-based permissions
- **Database Storage**: PostgreSQL with Drizzle ORM for persistent data
- **Real-time Updates**: WebSocket support for live data updates
- **Responsive UI**: Built with React, Tailwind CSS, and Radix UI components

## Tech Stack

- **Frontend**: React 18, TypeScript, Tailwind CSS, Radix UI
- **Backend**: Node.js, Express, TypeScript
- **Database**: PostgreSQL with Drizzle ORM
- **Authentication**: Passport.js with local strategy
- **Charts**: Recharts
- **File Processing**: XLSX library

## Installation

### Prerequisites

- Node.js (v18 or higher)
- npm or yarn
- PostgreSQL database (local or cloud)

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/Vigneshwaran2502/Excelanalysis.git
   cd Excelanalysis
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   - Copy `.env.example` to `.env` (if available) or create `.env`
   - Configure your database connection:
     ```env
     DATABASE_URL="postgresql://username:password@hostname/database"
     SESSION_SECRET="your-secret-key"
     ```

4. **Set up the database**
   - Follow the [Database Setup Guide](DATABASE_SETUP.md)
   - Or run the automated setup:
     ```bash
     npm run db:setup
     ```

5. **Build the application**
   ```bash
   npm run build
   ```

## Usage

### Development

Start the development server:
```bash
npm run dev
```

This will start both the backend server and the frontend development server.

### Production

Build and start the production server:
```bash
npm run build
npm start
```

### Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm start` - Start production server
- `npm run check` - Type check with TypeScript
- `npm run db:push` - Push database schema
- `npm run db:generate` - Generate migrations
- `npm run db:migrate` - Run migrations

## Database Schema

The application uses the following main tables:

- **users**: User accounts and authentication
- **files**: Uploaded file metadata and data
- **charts**: Chart configurations and metadata
- **admin_requests**: Admin role requests

## API Endpoints

- `GET /api/files` - List uploaded files
- `POST /api/files` - Upload a new file
- `GET /api/charts` - List charts
- `POST /api/charts` - Create a new chart
- `POST /api/auth/login` - User login
- `POST /api/auth/register` - User registration

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run tests
5. Submit a pull request

## License

MIT License - see LICENSE file for details

## Support

For issues and questions:
1. Check the [Database Setup Guide](DATABASE_SETUP.md)
2. Review server logs for error messages

3. Ensure your DATABASE_URL is correctly configured

