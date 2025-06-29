# Ticket Generating System

This project is a Ticket Generating System designed to streamline the process of creating, managing, and tracking support tickets using AI-powered triage and assignment.

## Features

- Create new tickets with title and description
- **Automatic ticket triage and assignment:** Uses the Google Gemini API to analyze ticket content, estimate priority, extract required skills, and assign tickets to the most suitable moderator based on their skills
- Track ticket status (TODO, IN_PROGRESS, etc.)
- **Agent dashboard:** Moderators and admins can view, update, and track the status of tickets assigned to them in real time
- Ticket history and helpful AI-generated notes for each ticket
- User authentication and authorization (admin, moderator, user roles)
- Admin panel for managing users and their skills

## Technologies Used

- Node.js (backend)
- Express.js (web framework)
- MongoDB (database, via Mongoose)
- React (frontend, with Vite and Tailwind CSS)
- Google Gemini API (for ticket analysis and skill extraction)
- Inngest (event-driven workflow)
- Nodemailer (email notifications)

## How It Works

- When a new ticket is created, the backend sends the ticket details to the Google Gemini API using a custom AI agent.
- The Gemini API analyzes the ticket, summarizes the issue, estimates its priority, provides helpful notes, and extracts relevant technical skills.
- The system matches the extracted skills to moderators in the database and assigns the ticket to the best-fit moderator (or an admin if no match is found).
- The assigned moderator receives an email notification about the new ticket.
- Moderators and admins can log in to their dashboard to view all tickets assigned to them, update ticket statuses, and review AI-generated notes and ticket history.
- All status changes and updates are tracked for each ticket.

## Getting Started

1. **Clone the repository:**
   ```sh
   git clone https://github.com/yourusername/ticket_generating_system.git
   cd ticket_generating_system
   ```

2. **Install backend dependencies:**
   ```sh
   cd ai-ticket-assistant
   npm install
   ```

3. **Install frontend dependencies:**
   ```sh
   cd ../ai-ticket-frontend
   npm install
   ```

4. **Set up environment variables:**
   - Copy `.env.example` to `.env` in `ai-ticket-assistant` and fill in your MongoDB URI, JWT secret, Gemini API key, and mail credentials.

5. **Run the backend:**
   ```sh
   npm run dev
   # or for Inngest local dev
   npm run inngest-dev
   ```

6. **Run the frontend:**
   ```sh
   npm run dev
   ```

7. **Access the application:**
   - Frontend: [http://localhost:5173](http://localhost:5173) (default Vite port)
   - Backend API: [http://localhost:3000](http://localhost:3000)

## Contributing

Contributions are welcome! Please open issues or submit pull requests for improvements or bug fixes.

## License

This project is licensed under the MIT