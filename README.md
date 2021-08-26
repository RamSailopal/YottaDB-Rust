# Introduction

This repo allows the provision of a development environment through docker that gives you everything that you need to develop with Rust and YottaDB

# Sandbox

The sandbox environment is an immutable environment with no persistent code base or storage. To provision:

      git clone https://github.com/RamSailopal/YottaDB-Rust.git
      cd YottaDB-Rust/sandbox
      docker-compose up
      
# dev

The dev environment differs from sandbox in that the code base and database is persistent. To provision:
  
First clone the YDBRust repo

      git clone https://gitlab.com/YottaDB/Lang/YDBRust.git

Then clone this repo

      git clone https://github.com/RamSailopal/YottaDB-Rust.git

Set the persistent YottaDB and Rust paths

      export yottadatadir="/path/to/yottadata"
      export rustcode="/path/to/YDBRust"

Provision the stack

     docker-compose up

# Beginning development

Navigate to http://ipofdockerserver:3002/#/home/yottadb-settings/Yottadb.theia-workspace

Open a commpilation window:

   Terminal -> Run Task -> YottaDB Compiler

Open the say_hello_rust example:

   File -> Open -> examples -> say_hello_rust.rs

This examples sets the global entry ^hello("Rust") to a value.


