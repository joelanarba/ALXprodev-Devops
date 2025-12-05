#!/usr/bin/env bash
# apiAutomation-0x00.sh
# Script to fetch data for Pikachu from the Pokémon API
# Saves response to data.json or logs errors to errors.txt

URL="https://pokeapi.co/api/v2/pokemon/pikachu"
OUTPUT_FILE="data.json"
ERROR_FILE="errors.txt"

# Make the API request
HTTP_RESPONSE=$(curl -s -w "%{http_code}" -o "$OUTPUT_FILE" "$URL")

# Check HTTP status code
if [ "$HTTP_RESPONSE" -ne 200 ]; then
    echo "Failed to fetch Pikachu data. HTTP status: $HTTP_RESPONSE" >> "$ERROR_FILE"
fi
