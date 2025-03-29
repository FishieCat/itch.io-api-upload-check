# itch.io-api-upload-check
Guide on how to check details of game uploads using itch.io's fee API key

1. Register an account https://itch.io/register and log in:
   > ![registering you know](https://github.com/user-attachments/assets/7013836e-fbab-4903-87ce-4c712086d972)

2. Generate an API key on https://itch.io/user/settings/api-keys:
   > ![pressing a button you know](https://github.com/user-attachments/assets/e1d50896-beea-407c-a38e-a0eedc507b05)

3. On the game page, for example https://ingdani.itch.io/marianne, right click the page and open the source:
   > ![right click context menu you know](https://github.com/user-attachments/assets/56e45e0c-a002-43b4-b9b0-65c8c58d0bff)

4. CTRL+F search for `game_id` and copy the number, `2236407` in this case:
   > ![game_id you know](https://github.com/user-attachments/assets/d3f255b6-3fbf-46a2-b842-611f8903df1c)

5. Insert your API key and game_id number into the `/uploads` API URL call:
   > ![API key you know](https://github.com/user-attachments/assets/375af3e8-6e8d-49b0-bbcc-5d1deff7467e)
   >
   >  ![game_id you know](https://github.com/user-attachments/assets/37680930-e5f3-4450-b612-f7e90005de69)
6. The result ("Pretty-print" recommended) will show you creation/update dates. Looks like `updated_at` gets updated when the `created_at` upload finishes.
   > ![api response you see](https://github.com/user-attachments/assets/620b6d8d-65de-4e91-90ed-e2af33deb7cb)


Here are a bunch of variations for easy copy paste/doubleclick insert replacement:
```
https://itch.io/api/1/API_KEY_GOES_HERE/game/2236407/uploads
https://itch.io/api/1/API_KEY_GOES_HERE/game/GAME_ID_GOES_HERE/uploads
https://itch.io/api/1/ /game/ /uploads
https://itch.io/api/1//game//uploads
```

Once you use this 1-2 times, entering '/uploads' into the URL bar should get the last used one from your history, so you don't have to insert the API key each time. Or just bookmark `https://itch.io/api/1/[insert_your_api_key_here]/game/GAME_ID_GOES_HERE/uploads` (with your API KEY pre-inserted.
