Student Email Lookup

A simple and secure web application that allows students to retrieve their school email address by providing their personal details and class.

Features

- Student first-name, other-name, and last-name lookup
- Class dropdown selection
- Secure lookup through Supabase
- Returns the student's email when a unique match is found
- Handles multiple matching students safely
- Displays a "not found" response when no match exists
- Responsive web interface

How It Works

The student provides:

1. First Name
2. Other Name
3. Last Name
4. Class

The application sends the information to a Supabase database function.

A student is returned as Found when exactly one matching record is identified.

If more than one student matches, the application returns Multiple without exposing an email.

If no student matches, the application returns Not Found.

Technology

- HTML / CSS / JavaScript
- Supabase
- PostgreSQL
- GitHub

Database Security

The student table has Row Level Security (RLS) enabled.

The application uses a controlled Supabase database function rather than exposing the student table directly to the website.

The database function uses "SECURITY DEFINER" and returns only the information required by the application.

Important Security Note

Only the Supabase publishable key should be used in the client-side application.

Never expose:

- Supabase service-role keys
- Database passwords
- Secret API keys
- ".env" files containing sensitive credentials

Project Status

Working and tested.

The database lookup, class dropdown, and student email retrieval have been tested successfully.

Future Improvements

Possible future additions include:

- Student password/account verification
- Email verification
- Admin dashboard
- Student record management
- Improved duplicate-student handling
- Usage monitoring and rate limiting

License

This project is intended for educational and institutional use.
