# Risk Management System

A risk management and incident tracking application with an ASP.NET Core API and a React web interface.

## Components

- `QM-master/`: ASP.NET Core backend, Entity Framework Core data access, and SQL Server persistence.
- `react-risk-system/`: React and TypeScript frontend.

The system supports role-scoped workflows for submitting and reviewing risk records, tracking actions, and recording changes. See the backend's [application documentation](QM-master/APP_DOCUMENTATION.md) and [workflow scenarios](QM-master/WORKFLOWS_AND_SCENARIOS.md) for details.

## Requirements

- .NET SDK 8 or later
- Node.js 18 or later and npm
- SQL Server (Developer, Express, or LocalDB), or Docker with Docker Compose

## Run locally

1. Configure the backend database connection and any required authentication or mail settings in the backend's configuration. Keep secrets out of source control.
2. Start the API from the backend project directory:

   ```bash
   dotnet run
   ```

3. Install and start the frontend from `react-risk-system/`:

   ```bash
   npm install
   npm start
   ```

The frontend is configured for a local API at `https://localhost:7002/api`; adjust its API configuration if the backend uses a different address. Check each component's configuration before deployment.

## Docker

Dockerfiles are included for the backend and frontend. Review their environment and port settings, then build and run them with your preferred Docker Compose configuration.

## Further documentation

- [Backend application documentation](QM-master/APP_DOCUMENTATION.md)
- [Functional requirements](QM-master/FUNCTIONAL_REQUIREMENTS.md)
- [Workflow scenarios](QM-master/WORKFLOWS_AND_SCENARIOS.md)
- [Change notes](CHANGES.md)
