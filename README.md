# C.B.D.B.'s : The Comic Book Database

## A free and open source comic book inventory application

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![GitHub issues](https://img.shields.io/github/issues/eprislac/cbdb)
![GitHub pull requests](https://img.shields.io/github/issues-pr/eprislac/cbdb)
![GitHub last commit](https://img.shields.io/github/last-commit/eprislac/cbdb)
![GitHub repo size](https://img.shields.io/github/repo-size/eprislac/cbdb)

### Overview

C.B.D.B.'s is a web application that allows users to catalog comic book
collections. Users can add, edit, and delete comic book entries, as well as
search and filter through the collection. The application also features user
authentication and authorization to ensure secure access to personal
collections. Very-much in starting phase, still testing out ideas and features.

### Why?

It's been a long time since I contributed code to anything outside of work.
My goal with this project is to exhibit my own coding skills, learn new
technologies and frameworks, and to have fun doing it. I also want to create
something that I would use myself, and I love comic books. I have a large that
has long gone uncatalogued, and I intend to change that, and demonstrate my
abilities in the process.

### Screenshots

(#TODO: add screenshots)

### Features

- User authentication and authorization
- Comic book management (add, edit, delete, view)
- Search and filter comic books by various criteria (TODO)
- Reverse-image search to add books by cover image (TODO)
- Responsive design for mobile and desktop
- Public API for integration with other applications (TODO)
- Real-time market-value tracking (TODO)
- MCP Server for RESTful API (TODO)

### Technologies Used

- Dev Environment:
  - [Docker](), [Docker Compose]() and [Dockerfile]() for containerization
  - [moon]() monorepo tool
  - [proto]() language version manager
- Frontend: [NEXTjs](), [Tailwind CSS](), [Auth0](), [HeroUI](), [pnpm]()
  - testing: [Jest](), [Playwright](), [Storybook](), [Cucumber]()
- Backend: [Ruby on Rails](), [PostgreSQL]()
  - testing: [RSpec](), [FactoryBot](), [Cucumber]()
- CI/CD: [Github Actions]()

### Installation

1. Clone the repository:

   ```bash
   git clone git@github.com/eprislac/cbdb.git
   ```

2. Navigate to the project directory:

   ```bash
   cd cbdb
   ```

3. Set up environment variables:
   - Copy the `.env.example` file to `.env` and fill in the required values
     (#TODO: create .env.example file)
   - Ensure you have the necessary credentials for Auth0 and PostgreSQL
   - Example variables:
     - `AUTH0_DOMAIN`
     - `AUTH0_CLIENT_ID`
     - `RAILS_ENV=development`
4. Build and start the Docker containers:

   ```bash
   docker-compose up --build
   ```

5. Access the application:
   - Frontend: `http://localhost`
   - Backend: `http://localhost:3000` (accessible via cbdb network as `http://api`)
   - Database: `localhost:5432` (accessible via cbdb network as `database`)

### Monorepo Structure

/apps/

- cbdb_client/: (sub-module) Next.js application
- cbdb_api/: (sub-module) Ruby on Rails API
- cbdb_public_api/: (sub-module) API for public access (TODO)
- cbdb_mcp/: (sub-module) MCP server for public API integration (TODO)
- db_data/: PostgreSQL data volume
- pgadmin-data/: pgAdmin data volume
- .moon/: moon configuration directory
- .prototools: proto version manager configuration
- .github/: GitHub Actions workflows
- .gitignore: Git ignore file
- .gitmodules: Git submodule configuration
- .env.example: Example environment variables file (TODO)
- .dockerignore: Docker ignore file
- docker-compose.yml: Docker Compose configuration
