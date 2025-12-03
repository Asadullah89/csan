# CSAN: Cutter-Sanborn Call Number Generator

`csan` is a CLI tool that generates a Cutter-Sanborn identifier, given a last name and an optional first name.

The Cutter-Sanborn call number, commonly called "Cutter number", is an alphanumeric code that forms part of the call number in library classification systems in order to arrange books alphabetically by author. It consists of the first letter of the author's last name followed by three-digit number derived from a predefined [table](https://github.com/veralvx/cutter-sanborn-table). This system was originally developed by Charles Cutter, and revised by Kate Sanborn.

## Installation

You can install this tool using [`uv`](https://docs.astral.sh/uv/) or `pip`:

```console
uv tool install csan
```

```console
pip install csan
```

## Usage  


```console
usage: csan [-h] [-f FIRST_NAME] -l LAST_NAME [-t TITLE] [-v]

Cutter-Sanborn identifier generator.

options:
  -h, --help            show this help message and exit
  -f, --first-name FIRST_NAME
  -l, --last-name LAST_NAME
  -t, --title TITLE
  -v, --verbose
```

For instance:

- `csan -f John -l Doe` -> D649
- `csan -f John -l Doe -t "My Book"` -> D649m
- `csan -f First -l Last -v` -> L349, with log output to the console
- `csan -f Jorge -l "De la Cruz"` -> D332

## Examples

The following cutter numbers are expected for their respective names. This is achieved with `cutter_number` function from `csan.cutter`, which returns only the integer part. When run via CLI, the output is the Cutter call number (`cutter_call_number` function), which also includes the Cutter integer number.

| First Name | Last Name    | Cutter Integer Number | Cutter Call Number |
|------------|--------------|:---------------------:|:------------------:|
| Jane       | Austen       | 933                   | A933               |
| Eric       | Blair        | 635                   | B635               |
| Agatha     | Christie     | 555                   | C555               |
| Samuel     | Clemens      | 625                   | C625               |
| Jorge      | De la Cruz   | 332                   | D332               |
| Charles    | Dickens      | 548                   | D548               |
| Emily      | Dickinson    | 553                   | D553               |
| Fyodor     | Dostoyevsky  | 724                   | D724               |
| Stephen    | King         | 52                    | K52                |
| VERA       | LVX          | 979                   | L979               |
| Herman     | Melville     | 531                   | M531               |
| George     | Orwell       | 79                    | O79                |
| William    | Shakespeare  | 527                   | S527               |
| Lord       | Sith         | 622                   | S622               |
| Ivan       | Smith        | 649                   | S649               |
| William    | Smith        | 664                   | S664               |
| Leo        | Tolstoy      | 654                   | T654               |
| Mark       | Twain        | 969                   | T969               |
| Virginia   | Woolf        | 913                   | W913               |
| Emile      | Zola         | 86                    | Z86                |
