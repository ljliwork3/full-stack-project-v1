# Project context (for Claude)

- API: .NET 8 Web API in `apps/api`, Kestrel on http://localhost:3001 (HTTPS 3002)
- Web: Next.js in `apps/web`, dev on http://localhost:3000
- Run both in VS Code: Run & Debug → "Run API + Web"
- Visual Studio: open `apps/api/Api.sln`, use the "Kestrel" profile
- Env files:
  - Web: `apps/web/.env.local`
  - API: `apps/api/appsettings.Development.json` (or user-secrets)
- Conventions:
  - Return errors as `{ code, message, details? }`
  - Keep DTOs in `apps/api/Contracts`
- Future:
  - Expose Swagger at `/swagger/v1/swagger.json`
  - Generate TS SDK into `packages/ts-sdk` and import from web