# Elixir / Pheonix App

Create new pheonix app
```
mix pmix phx.new <app-name>
```

Fetch and install dependencies
```
mix deps.get
```
cd assets && npm install && node node_modules/brunch/bin/brunch build

Configure database in config/dev.exs and run
```
mix ecto.create
```

Start Phoenix app
```
mix phx.server
```

Run IEx (Interactive Elixir) console
```
iex -S mix phx.server
```
