Builder l'image :

```
docker build -t card-game docker/
```

Générer les images :

```
docker run -it -v $PWD/data:/app/data -v $PWD/_output:/app/_output card-game ruby deck.rb
```

Clean output folders:

```
rm -rf $PWD/_output-level1-challenges
rm -rf $PWD/_output-level2-challenges
rm -rf $PWD/_output-level3-challenges
rm -rf $PWD/_output-level1-concepts
rm -rf $PWD/_output-level2-concepts
rm -rf $PWD/_output-level3-concepts
rm -rf $PWD/_output-level1-solutions
rm -rf $PWD/_output-level2-solutions
rm -rf $PWD/_output-level3-solutions
rm -rf $PWD/_output-game
```

Run all:

```
docker run -it -v $PWD/data-level1-challenges:/app/data -v $PWD/_output-level1-challenges:/app/_output card-game ruby deck.rb
docker run -it -v $PWD/data-level1-concepts:/app/data -v $PWD/_output-level1-concepts:/app/_output card-game ruby deck.rb
docker run -it -v $PWD/data-level1-solutions:/app/data -v $PWD/_output-level1-solutions:/app/_output card-game ruby deck.rb

docker run -it -v $PWD/data-level2-challenges:/app/data -v $PWD/_output-level2-challenges:/app/_output card-game ruby deck.rb
docker run -it -v $PWD/data-level2-concepts:/app/data -v $PWD/_output-level2-concepts:/app/_output card-game ruby deck.rb
docker run -it -v $PWD/data-level2-solutions:/app/data -v $PWD/_output-level2-solutions:/app/_output card-game ruby deck.rb

docker run -it -v $PWD/data-level3-challenges:/app/data -v $PWD/_output-level3-challenges:/app/_output card-game ruby deck.rb
docker run -it -v $PWD/data-level3-concepts:/app/data -v $PWD/_output-level3-concepts:/app/_output card-game ruby deck.rb
docker run -it -v $PWD/data-level3-solutions:/app/data -v $PWD/_output-level3-solutions:/app/_output card-game ruby deck.rb

docker run -it -v $PWD/data-game:/app/data -v $PWD/_output-game:/app/_output card-game ruby deck.rb
```

docker run -it -v $PWD/data-game:/home/data -v $PWD/tmp:/home/app -v $PWD/_output-game:/app/_output card-game ruby deck.rb


```
docker run -it --rm -v $PWD/data-game:/home/data -v $PWD/app:/home/app -v $PWD/_output-game:/app/_output card-game bash
cd ./_output/
rm *
cd ..
echo "Processing cryptobuzz..."
ruby deck.rb cryptobuzz
cd ./_output/
for file in card_*.svg; do
    mv "$file" "cryptobuzz-${file#card_}"
done
cd ..
echo "Processing cryptoquest..."
ruby deck.rb cryptoquest
cd ./_output/
for file in card_*.svg; do
    mv "$file" "cryptoquest-${file#card_}"
done
cd ..
echo "Processing consommateurs-oups..."
ruby deck.rb consommateurs-oups
cd ./_output/
for file in card_*.svg; do
    mv "$file" "consommateurs-oups-${file#card_}"
done
cd ..
echo "Processing consommateurs-finances..."
ruby deck.rb consommateurs-finances
cd ./_output/
for file in card_*.svg; do
    mv "$file" "consommateurs-finances-${file#card_}"
done
cd ..
echo "Processing consommateurs-usages..."
ruby deck.rb consommateurs-usages
cd ./_output/
for file in card_*.svg; do
    mv "$file" "consommateurs-usages-${file#card_}"
done
cd ..
echo "Processing hackers-avance..."
ruby deck.rb hackers-avance
cd ./_output/
for file in card_*.svg; do
    mv "$file" "hackers-avance-${file#card_}"
done
cd ..
echo "Processing hackers-securite..."
ruby deck.rb hackers-securite
cd ./_output/
for file in card_*.svg; do
    mv "$file" "hackers-securite-${file#card_}"
done
cd ..
echo "Processing hackers-tokeneconomie..."
ruby deck.rb hackers-tokeneconomie
cd ./_output/
for file in card_*.svg; do
    mv "$file" "hackers-tokeneconomie-${file#card_}"
done
cd ..
echo "Processing market-makers..."
ruby deck.rb market-makers
cd ./_output/
for file in card_*.svg; do
    mv "$file" "market-makers-${file#card_}"
done
cd ..
echo "Processing partenaires..."
ruby deck.rb partenaires
cd ./_output/
for file in card_*.svg; do
    mv "$file" "partenaires-${file#card_}"
done
cd ..
echo "Processing projets-securite..."
ruby deck.rb projets-securite
cd ./_output/
for file in card_*.svg; do
    mv "$file" "projets-securite-${file#card_}"
done
cd ..
echo "Processing projets-tokeneconomie..."
ruby deck.rb projets-tokeneconomie
cd ./_output/
for file in card_*.svg; do
    mv "$file" "projets-tokeneconomie-${file#card_}"
done
cd ..
echo "Processing regulateurs..."
ruby deck.rb regulateurs
cd ./_output/
for file in card_*.svg; do
    mv "$file" "regulateurs-${file#card_}"
done
cd ..
echo "Processing traders-oups..."
ruby deck.rb traders-oups
cd ./_output/
for file in card_*.svg; do
    mv "$file" "traders-oups${file#card_}"
done
cd ..
echo "Processing traders-risque..."
ruby deck.rb traders-risque
cd ./_output/
for file in card_*.svg; do
    mv "$file" "traders-risque-${file#card_}"
done
cd ..
echo "Processing traders-strategie..."
ruby deck.rb traders-strategie
cd ./_output/
for file in card_*.svg; do
    mv "$file" "traders-strategie-${file#card_}"
done
cd ..
```
