# Teams Post Processor

#### An autopkg post-processor which sends a Microsoft Teams notification using a webhook, when an item is added to Munki

Originally written by Andy Semak (asemak) whos autopkg repo was archived https://github.com/autopkg/asemak-recipes

A screenshot example can be found in this repo

First you need to create a webhook in Teams: https://docs.microsoft.com/en-us/microsoftteams/platform/webhooks-and-connectors/how-to/add-incoming-webhook#add-an-incoming-webhook-to-a-teams-channel

This will give you the webhook url, make sure you save this as you will need it next.

Add this repo:
``` autopkg repo-add asemak-recipes ```

Then run a recipe or recipes, replacing the webhook_url with one you saved earlier:
``` autopkg run myRecipe.munki MakeCatalogs.munki --post=com.github.autopkg.asemak-recipes.postprocessors/TeamsPost --key webhook_url=https://outlook.office.com/webhook/XXXXXXXXXXX```

Or run using a recipe list:
```autopkg run --recipe-list="/path/to/my/RecipeList.txt" --post=com.github.autopkg.asemak-recipes.postprocessors/TeamsPost --key webhook_url=https://outlook.office.com/webhook/XXXXXXXXXXX```
