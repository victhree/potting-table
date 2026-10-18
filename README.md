# Potting Table

A phone-installable feeding schedule for potted plants. No account, no server, no network needed after the first load.

Live: https://victhree.github.io/potting-table/

## What it does

Seven products, each on its own interval, counted forward from the last time you applied it:

| Product | Every | Dose |
|---|---|---|
| NPK 19:19:19 | 20 days | 1 g per litre |
| Humic Acid | 30 days | 1 to 1.5 ml per litre |
| Epsom Salt | 30 days | 1 g per litre, about one level scoop |
| Neem Oil Spray | 30 days | 5 ml per litre, plus 2 to 3 drops of liquid soap |
| Vermicompost | 60 days | 2 handfuls per 8 to 10 inch pot, 1 for smaller |
| Neem Khali | 60 days | 1 handful per 8 to 10 inch pot |
| Saaf Fungicide | 90 days | 1.5 g per litre |

Opens on the calendar. Tap a day to log an application or clear one. The Due tab lists what is overdue, due today and coming up. The Schedule tab carries the full reference: dose per litre, scoop equivalent, method, and the editable interval for each product.

## Installing it on a phone

Open the live link, then:

- **iPhone, Safari:** Share, then Add to Home Screen.
- **Android, Chrome:** three dot menu, then Add to Home screen.

## Where the data lives

In the browser's `localStorage`, on that device only. Nothing is uploaded and nothing syncs between devices, so pick one phone as the real one. The Backup tab copies everything out as JSON and pastes it back in.

## Working on it

`index.html` here is generated, not hand-edited. The source is the Artifact version, and `build.py` wraps it in a standalone document and adds the manifest, icons and service worker:

```
python3 build.py
```

Bump `CACHE` in `sw.js` when the shell files change, so installed copies pick up the new version.
