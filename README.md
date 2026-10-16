# Event Platform API

Backend for an Eventbrite-style ticketing platform: organizers create events and sell tickets, attendees buy them and get a unique ticket code.

**Stack:** ASP.NET Core (.NET 10) · Entity Framework Core · PostgreSQL

## Structure

- `Controllers/` HTTP endpoints
- `BLL/` business rules
- `DAL/` data access (`AppDbContext`)
- `Entities/` database entities (scaffolded, database-first)
- `ViewModel/` request and response models

## Run locally

1. Create a PostgreSQL database named `eventplatform` and run the SQL script in `database/`.
2. Set the connection string in user secrets:
   `dotnet user-secrets set "ConnectionStrings:Default" "Host=localhost;Port=5432;Database=eventplatform;Username=...;Password=..."`
3. Start the app with the `http` profile and open `/scalar/v1` to try the endpoints.

## Roadmap

- [x] Project setup and database connection
- [ ] Registration and login
- [ ] Events and ticket types
- [ ] Orders and ticket issuance
- [ ] Check-in
