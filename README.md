# ANVIX — Trust Scanner

**Anvix Trust Scanner** is a web application designed to help users investigate suspicious job offers, messages, and payment requests. It aims to help users identify potential scams and make more informed decisions using trust-analysis tools and AI-powered features.

Built with **TanStack Start, React, Supabase, and Lovable AI Gateway**, Anvix combines a modern web interface with backend authentication, database integration, and intelligent scam-analysis capabilities.

## Features

- **Suspicious Offer Analysis:** Investigate potentially fraudulent job offers, messages, and payment requests.
- **AI-Powered Investigation:** Analyze suspicious content using AI-assisted investigation tools.
- **Trap-Reply Assistance:** Access tools designed to help users evaluate suspicious conversations and potential scam interactions.
- **Verdict Summaries:** Present analysis results in a more understandable format.
- **Authentication:** Support user authentication through Supabase.
- **Database Integration:** Store and manage application data through Supabase, with Row Level Security (RLS) where configured.
- **Responsive Interface:** Provide a modern interface built with React, Tailwind CSS, and shadcn/ui.

## Tech Stack

| Technology         | Purpose                                        |
| ------------------ | ---------------------------------------------- |
| TanStack Start     | Full-stack React application framework         |
| React 19           | User interface development                     |
| TypeScript         | Type-safe application development              |
| Tailwind CSS v4    | Styling and responsive layouts                 |
| shadcn/ui          | Reusable interface components                  |
| Supabase           | Authentication, database, and backend services |
| Lovable AI Gateway | AI-powered application features                |
| Bun / npm          | Dependency management and development scripts  |

## Run Locally

### Prerequisites

- Node.js and npm, or Bun
- A Supabase project
- Git

### 1. Clone the Repository
```
git clone https://github.com/swathi-pr7/anvix-trust-scan-main.git
cd anvix-trust-scan-main
```

### 2. Install Dependencies

Using Bun:
```
bun install
```

Or using npm:
```
npm install
```

### 3. Configure Environment Variables

Create a file named `.env` in the project root directory.

Add your own Supabase configuration using the following template:
```
VITE_SUPABASE_URL="YOUR_SUPABASE_URL"
VITE_SUPABASE_PUBLISHABLE_KEY="YOUR_SUPABASE_PUBLISHABLE_KEY"
VITE_SUPABASE_PROJECT_ID="YOUR_SUPABASE_PROJECT_ID"

SUPABASE_URL="YOUR_SUPABASE_URL"
SUPABASE_PUBLISHABLE_KEY="YOUR_SUPABASE_PUBLISHABLE_KEY"
SUPABASE_PROJECT_ID="YOUR_SUPABASE_PROJECT_ID"

# Add these only if required by the application
# LOVABLE_API_KEY=YOUR_LOVABLE_API_KEY
# SUPABASE_SERVICE_ROLE_KEY=YOUR_SUPABASE_SERVICE_ROLE_KEY
# ANVIX_SIGNAL_PEPPER=YOUR_RANDOM_SECRET_VALUE
```

Replace the placeholders with the appropriate values from your own Supabase project. Only configure variables that your application actually uses.

**Security considerations:**

- Never commit your local `.env` file or private credentials to GitHub.
- Use `.env.example` to document required environment variables with placeholder values.
- Use publishable Supabase keys only for intended client-side access, with appropriate database permissions and RLS policies.
- Keep service-role keys, AI API keys, and other privileged secrets exclusively in server-side configuration.
- Never expose privileged credentials through variables prefixed with `VITE_`.

### 4. Start the Development Server

Using Bun:
```
bun dev
```

Or using npm:
```
npm run dev
```

Open the local URL printed in your terminal. If the application uses the default development port, visit:

[http://localhost:3000](http://localhost:3000)

### 5. Configure Authentication and AI Features

**Authentication:** Configure the required authentication providers and redirect URLs in your Supabase project. Email and password authentication may be used for local development if enabled.

**AI-powered features:** Features such as Ask ANVIX, Trap-Reply, and investigation summaries may require the appropriate Lovable AI Gateway configuration. Set the necessary credentials in the environment expected by the application.

**Database:** The application requires the appropriate Supabase database schema, authentication configuration, and RLS policies. Use the project's existing backend configuration and migrations, if provided.

## Project Structure

The application is organized around its frontend, backend integration, and supporting configuration.

- `src/` — Application source code and user interface.
- `public/` — Static assets, if present.
- `package.json` — Dependencies and project scripts.
- `README.md` — Project documentation.
- `.env` — Local environment configuration; excluded from version control.
- `.env.example` — Environment-variable template for developers.

*The exact directory structure may vary depending on the repository.*

## Security

Anvix is intended to help users assess potentially suspicious content. Its analysis results should be treated as guidance rather than a guarantee that a message, job offer, or payment request is safe or fraudulent.

Security depends on correct environment configuration, secure server-side handling of privileged credentials, and appropriate Supabase Row Level Security policies.

Do not submit passwords, access tokens, financial credentials, or other sensitive personal information when analyzing suspicious content.

## Future Enhancements

Potential improvements include:

- More comprehensive scam-detection and risk-analysis workflows.
- Enhanced explanations for suspicious-message verdicts.
- Improved usability and accessibility.
- Expanded automated testing and security validation.
- Additional reporting and investigation capabilities.

## Contributing

Contributions, bug reports, and suggestions are welcome. Fork the repository, create a feature branch, test your changes, and submit a pull request describing the proposed improvement.

## License

A license has not been specified. Add an appropriate `LICENSE` file before distributing the project under a particular open-source license.

## Author

Developed as a project focused on identifying suspicious digital interactions and improving awareness of potential online scams. i will paste this as it as