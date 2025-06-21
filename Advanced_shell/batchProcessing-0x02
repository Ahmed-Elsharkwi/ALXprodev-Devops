list_strings=('bulbasaur', 'ivysaur', 'venusaur', 'charmander', 'charmeleon')

for word in "${list_strings[@]}"; do
	name=$(echo "$word" | sed -E 's/,$//g');
	echo "Fetching data for $name ..."
	curl --fail "https://pokeapi.co/api/v2/pokemon/$name" 1>$name.json 2> errors.txt
	sleep 5
	echo "Saved data to pokemon_data/$name.json ✅"
done
