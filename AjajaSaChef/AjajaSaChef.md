# Ajaja Sa Chef
### Description
My Sardinian grandmother was a great chef and pastry chef. When I visited her, she delighted me with a typical recipe. Today, I would like to try replicating it, and I asked her to send me the recipe. However, besides being so weird and big, I don’t understand anything. Can you help me?

## Solution 
the challenge gives us a pdf that simply is a recipe with a list of ingredients and their dosage. <br>
![Screenshot from 2023-10-29 21-02-56](https://github.com/FeeeDz/Srdnlen-CTF-2023/assets/67475596/9f4a23c8-d44d-4dd4-b252-7c2bfb684b20)

the ingredients are listed with the format: number + name of the ingredient
i recognized that that numbers were characters in ascii.
The real flag of the challenge starts from the word *Metodu* <br>
![Screenshot from 2023-10-29 21-07-57](https://github.com/FeeeDz/Srdnlen-CTF-2023/assets/67475596/c6bdd91b-207a-4789-8f71-391778cd9715)


the sentences all follow the same pattern, in each one only the name of the ingredient changes.
At this point it was only necessary to make a list of the number of grams associated with the ingrendient and create the flag number by number.
![Screenshot from 2023-10-29 21-15-36](https://github.com/FeeeDz/Srdnlen-CTF-2023/assets/67475596/3a5be779-a9a1-4f32-986a-18f150bb20a5)

But the flag was backwards: **}yenoh_htiw_ylno_seog_adaes{nelndrs** --> **srdnlen{seada_goes_only_with_honey}**
