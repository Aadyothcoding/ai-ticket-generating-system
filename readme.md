# Ticket Generating System

This project is a Ticket Generating System designed to streamline the process of creating, managing, and tracking tickets for various issues or requests.

## Features

- Create new tickets with relevant details
- **Automatic ticket assignment:** Uses the Google Gemini API to analyze ticket content and intelligently assign tickets to the most appropriate users or teams
- Track ticket status (open, in progress, closed, etc.)
- **Agent dashboard:** Agents can view, update, and track the status of tickets assigned to them in real time
- View ticket history and comments
- User authentication and authorization

## Technologies Used

- Python (or specify your backend language)
- Flask/Django/FastAPI (specify your framework)
- Google Gemini API for ticket classification and assignment
- Frontend: React/Angular/Vue (specify if applicable)
- Database: PostgreSQL/MySQL/SQLite (specify your DB)
- Other tools/libraries as needed

## How It Works

- When a new ticket is created, the system sends the ticket details to the Google Gemini API.
- The Gemini API analyzes the ticket's content and determines the most suitable user or team to handle the ticket.
- The ticket is automatically assigned based on the API's recommendation.
- Agents can log in to their dashboard to view all tickets assigned to them, update ticket statuses (open, in progress, closed), and add comments or notes.
- The system tracks all status changes and maintains a history for each ticket.

## Getting Started

1. **Clone the repository:**
   ```sh
   git clone https://github.com/yourusername/ticket_generating_system.git
   cd ticket_generating_system
   ```

2. **Install dependencies:**
   ```sh
   pip install -r requirements.txt
   ```

3. **Set up the database:**
   - Update your database configuration in the settings file.
   - Run migrations if required.

4. **Configure Google Gemini API:**
   - Add your Gemini API credentials to the environment or configuration file.

5. **Run the application:**
   ```sh
   python app.py
   ```

6. **Access the application:**
   - Open your browser and go to `http://localhost:8000` (or the port specified).

## Contributing

Contributions are welcome! Please open issues or submit pull requests for improvements or bug fixes.

## License

This project is licensed under the