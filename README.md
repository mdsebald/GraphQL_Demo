# GraphQL Demo

Using the: https://www.howtographql.com/graphql-elixir  Elixir GraphQL

## Issues

### Installing PostgreSQL

I used these instructions for installing on Windows Subsystem for Linux (WSL), Ubuntu 18.04 (bionic)

https://tecadmin.net/install-postgresql-server-on-ubuntu/

After installing postgreSQL, it needed to be restarted and the `postgres` password needed to be reset

`$ /etc/init.d/postgresql start`
`$ /etc/init.d/postgresql stop`
`$ /etc/init.d/postgresql restart`
`$ /etc/init.d/postgresql status`

Login to PostgreSQL (default user name: postgres):  

`$ sudo su - postgres`
`$ psql`

Open a `psql` session as the postgres user (you won't be asked for the password
under TRUST authentication) to the database and execute the command:

`ALTER USER postgres WITH PASSWORD 'postgres';`


### Making it work

In the main `mix.exs` file  changed dependancy `{:cowboy, "~> 1.0"}`  to `{:cowboy_plug, "~>1.0"}`
and changed the `:absinthe_plug` dependency version from `1.3.4` to `1.4.6`
Removed the quotes around `test:` in th aliases list to suppress warnings.




To start your Phoenix server:

  * Install dependencies with `mix deps.get`
  * Create and migrate your database with `mix ecto.create && mix ecto.migrate`
  * Start Phoenix endpoint with `mix phx.server`

Now you can visit [`localhost:4000`](http://localhost:4000) from your browser.

Ready to run in production? Please [check our deployment guides](http://www.phoenixframework.org/docs/deployment).

## Learn more

  * Official website: http://www.phoenixframework.org/
  * Guides: http://phoenixframework.org/docs/overview
  * Docs: https://hexdocs.pm/phoenix
  * Mailing list: http://groups.google.com/group/phoenix-talk
  * Source: https://github.com/phoenixframework/phoenix
