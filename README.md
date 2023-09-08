Go PokeDex CLI
==============

Overview
--------
Go guided project from [Boot.dev](https://boot.dev)

Pokedex in a command-line REPL (Read-Eval-Print-Loop) Project.
This is a guided project from boot.dev
The PokéAPI will be powering all of the data needed in this project.
A Pokedex is just a make-believe device that lets us look up
information about Pokemon.

Learning Goals
--------------
- Learn how to parse JSON in Go
- Practice making HTTP requests in Go
- Learn how to build a CLI tool that makes interacting with a back-end server easier
- Get hands-on practice with local Go development and tooling
- Learn about caching and how to use it to improve performance

Execution
---------
1. Clone this repository to your local machine:  
```shell
git clone <repository-url>
```

2. Navigate to the project directory:  
```shell
cd pokedexcli
```

3. Compile the program:  
```shell
go build
```

4. Run the program:
```shell
./pokedexcli
```
You should see the following output:  

File Tree
---------
```shell
pokedexcli
├── README.md
├── command_catch.go
├── command_exit.go
├── command_explore.go
├── command_help.go
├── command_inspect.go
├── command_map.go
├── command_pokedex.go
├── go.mod
├── internal
│   ├── pokeapi
│   │   ├── client.go
│   │   ├── location_get.go
│   │   ├── location_list.go
│   │   ├── pokeapi.go
│   │   ├── pokemon_get.go
│   │   ├── types_locations.go
│   │   └── types_pokemon.go
│   └── pokecache
│       └── pokecache.go
├── main.go
├── pokedexcli
└── repl.go
```

Sample Run
----------
```shell
Pokedex > map
canalave-city-area
eterna-city-area
pastoria-city-area
sunyshore-city-area
sinnoh-pokemon-league-area
oreburgh-mine-1f
oreburgh-mine-b1f
valley-windworks-area
eterna-forest-area
fuego-ironworks-area
mt-coronet-1f-route-207
mt-coronet-2f
mt-coronet-3f
mt-coronet-exterior-snowfall
mt-coronet-exterior-blizzard
mt-coronet-4f
mt-coronet-4f-small-room
mt-coronet-5f
mt-coronet-6f
mt-coronet-1f-from-exterior
```

```shell
Pokedex > explore canalave-city-area
Exploring canalave-city-area...
Found Pokemon: 
 - tentacool
 - tentacruel
 - staryu
 - magikarp
 - gyarados
 - wingull
 - pelipper
 - shellos
 - gastrodon
 - finneon
 - lumineon
```

```shell
Pokedex > inspect pikachu
you have not caught that pokemon
Pokedex > catch pikachu
Throwing a pokeball at pikachu...
pikachu was caught!
Pokedex > inspect pikachu
Name: pikachu
Height: 4
Weight: 60
Stats:
 -hp: 35
 -attack: 55
 -defense: 40
 -special-attack: 50
 -special-defense: 50
 -speed: 90
Types:
 - electric

```
