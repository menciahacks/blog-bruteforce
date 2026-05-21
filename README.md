# Blog Bruteforce Local

A local Windows console version of Blog Bruteforce.

## How to run

Double-click:

```text
run.bat
```

No Node, npm, Wrangler, Python, or Cloudflare setup is required. The app uses Windows PowerShell, which is built into Windows.

## Folder structure

```text
README.md
run.bat
assets/
  app.ps1
logs/
```

The `assets` folder is hidden automatically when `run.bat` starts, if Windows allows it.

## Logs

The app writes logs to:

```text
logs/session-YYYYMMDD-HHMMSS.txt
logs/found-blogs.txt
```

## Input example

Enter names one per line:

```text
johndoe
janedoe
```

Then press ENTER on an empty line.

You can also paste names separated by commas or semicolons.

## Smart skip behavior

If a name already ends with a number, the scanner does not check numbers below that suffix for that name.

Example:

```text
test2
test3
```

With start number `2`, the scanner checks `test2-2`, but skips `test3-2` and starts `test3` at `3`.

## Stop scanning

Press `CTRL+C` to stop an unlimited scan.
