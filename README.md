# AmazonPriceTracker: Wishlist price-history prototype

AmazonPriceTracker is a Python prototype for collecting prices from a shared Amazon wishlist, storing dated snapshots in JSON, and plotting individual product histories with Matplotlib.

## 1. Components

- Browser extraction uses Pyppeteer to scroll the wishlist and read item details.
- Local persistence groups observations by date in `config.json`.
- Plotting groups available observations by product and creates price-over-time lines.
- A `readonly` argument selects the stored-data plotting path.

## 2. Requirements

Python 3, Pyppeteer, and Matplotlib. A dependency manifest is not included in this snapshot.

## 3. Intended workflow

`setup.py` writes a shared wishlist URL to a local `config.json` file. The main application then collects product observations, updates the local history, and passes that history to the plotting component. Previously stored history can be selected with:

```sh
python3 app.py readonly
```

This command requires a configuration file containing the expected `items` history structure.

## 5. License

MIT. See `LICENSE`.

<!--
## Screenshots
-->

<!--
## Tests and evaluation

### Verified results
-->
