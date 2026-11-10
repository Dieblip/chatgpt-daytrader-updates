# ChatGPT Day Trader — GitHub update releases

This repository hosts public update ZIP files for the ChatGPT Day Trader Windows app. **Never upload .env, .venv, or any API keys.**

## Publish an update (one ZIP upload)

1. Download the new release ZIP from the ChatGPT conversation.
2. On GitHub, open the [release-assets folder](release-assets).
3. Use **Add file → Upload files** to upload a file with the exact name **ChatGPT_DayTrader_Update.zip**, replacing the older file (if any).
4. Click **Commit changes**.
5. GitHub Actions runs [Publish Day Trader Release](.github/workflows/publish-daytrader-update.yml), validates the archive and its version, and publishes a GitHub Release tagged like **v5.1.1**, with the required asset filename.
6. Go to [Releases](../../releases) and confirm it is published and has the asset attached. If no release appears, check the Actions tab for a validation/permissions error.
7. In the Windows app, set **GitHub Updates → Repository** to **Dieblip/chatgpt-daytrader-updates**, save, then click **Check for Updates**. Stop the trading and practice processes before applying an update.

**Current test update prepared:** v5.1.1. The release file must be uploaded to `release-assets/ChatGPT_DayTrader_Update.zip` to trigger the publishing workflow.

Do not upload the full Windows installer ZIP. Use only the **GitHub release update ZIP**. The release updater will not update if the installed version is equal or newer, if trading is active, or if GitHub's release metadata fails verification.

Publishing through GitHub does **not** verify trading profitability, API integration, or suitability for real-money execution.
