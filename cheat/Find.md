# Find Commands

## List Directories Containing Files of a Certain Type or Name

    find . -name '*.rb' | sed 's/\/[^\/]*$//' | sort | uniq

    find . -name '*.conf' | sed 's/\/[^\/]*$//' | sort | uniq

    find . -name '*rc' | sed 's/\/[^\/]*$//' | sort | uniq


## Same thing without regex

    find . -name '*.php' | rev | cut -d/ -f2- | rev | sort | uniq