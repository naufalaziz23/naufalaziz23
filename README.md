name: Waka Readme

on:
  schedule:
    # Jalan otomatis setiap jam 12 malam UTC
    - cron: '0 0 * * *'
  workflow_dispatch: # Supaya bisa di-klik manual

jobs:
  update-readme:
    name: Update Readme with Metrics
    runs-on: ubuntu-latest
    steps:
      - uses: athul/waka-readme@master
        with:
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
