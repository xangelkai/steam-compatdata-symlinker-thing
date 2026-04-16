# steam-compatdata-symlinker

Creates human-readable symlinks for Steam's `compatdata` directories, so you don't have to remember game IDs.

**Before:** `compatdata/22380/`
**After:** `compatdata/Fallout New Vegas/` -> `compatdata/22380/`

Also finds and cleans up broken symlinks, unused compatdata/common/shadercache directories.

## Install

```bash
chmod +x steam-compatdata-symlinker
```

## Usage

```bash
# Manual — pass your steamapps directory:
./steam-compatdata-symlinker /path/to/steamapps

# Auto — find all steamapps directories automatically (requires fd):
./steam-compatdata-symlinker -a

# Help:
./steam-compatdata-symlinker -h
```

## Flags

| Flag | Description |
|------|-------------|
| `-h` | Show help |
| `-e` | Explain what "unused directories" means |
| `-a` | Auto-detect steamapps directories using `fd` |
