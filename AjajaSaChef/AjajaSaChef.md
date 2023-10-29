# Ajaja Sa Chef
### Description
My Sardinian grandmother was a great chef and pastry chef. When I visited her, she delighted me with a typical recipe. Today, I would like to try replicating it, and I asked her to send me the recipe. However, besides being so weird and big, I don’t understand anything. Can you help me?

## Solution 
the challenge gives us a pdf that simply is a recipe with a list of ingredients and their dosage. <br>
-mettere immagine
the ingredients are listed with the format: number + name of the ingredient
i recognized that that numbers were characters in ascii.
The real flag of the challenge starts from the word *Metodu* <br>
-mettere immagine
the sentences all follow the same pattern, in each one only the name of the ingredient changes.
At this point it was only necessary to make a list of the number of grams associated with the ingrendient and create the flag number by number.
-mettere immagine cyberchef
But the flag was backwards