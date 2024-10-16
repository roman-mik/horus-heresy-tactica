# HorusHeresyTactica

**HorusHeresyTactica** is a web-based battle tracker and simulator set during the iconic Warhammer 30k timeline of the Horus Heresy. This project allows users to simulate battles between the legendary Space Marine legions, track their outcomes, and explore the tactics and strategies that shaped one of the most pivotal conflicts in the Warhammer universe.

Built using **Go** for the backend and **HTMX** for the frontend, HorusHeresyTactica delivers a fast, interactive experience, complete with real-time battle simulations, legion stats, and historical tracking. Whether you're a Warhammer lore enthusiast or a fan of strategic wargaming, this app brings the tactical depth of the Horus Heresy to life.

## Features:
- **Legion Roster Builder**: Choose your favorite Space Marine legions and assemble them for battle.
- **Battle Simulator**: Engage in epic clashes, with results influenced by legion stats and tactical choices.
- **Dynamic Frontend**: Powered by HTMX, experience real-time updates during battle phases without page reloads.
- **Battle History Tracking**: Log past battles and track each legion's performance across multiple confrontations.
- **Leaderboards**: Compare legion victories and discover which force reigns supreme.

## Tech Stack:
- **Go**: High-performance backend for battle logic and API.
- **HTMX**: Server-driven, real-time UI interactions.
- **PostgreSQL**: (Optional) Database for storing legion stats, battle outcomes, and user data.

Whether you're looking to explore tactical scenarios or build out your own wargaming simulator, HorusHeresyTactica offers a fun and educational project to explore the power of Go and HTMX.

## Necessary tools:
- **Homebrew**: Package manager - [brew.sh](https://brew.sh) 
- **Taskfile**: Task runner - [taskfile.dev](https://taskfile.dev)

## Migrations
- **golang-migrate** - [link](https://github.com/golang-migrate/migrate/tree/master)

golang-migrate is a database migration tool for Go. It allows you to manage your database schema by applying incremental changes (migrations) to your database. This helps in versioning your database schema and ensures that your database structure is consistent across different environments.

### Create migration
```
migrate create -ext sql -dir db/migrations -seq migration_name
```
or using task
```
task create-migration -- migration_name
```

### Run migration

```
migrate -source file://internal/database/migrations -database "postgres://${db_user}:${db_password}@${db_host}:${db_port}/${db_name}?sslmode=disable" up
```
or using task
```
task migrate-up
```
