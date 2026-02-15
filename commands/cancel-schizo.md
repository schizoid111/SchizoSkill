# /cancel-schizo Command

Emergency stop for SCHIZO-MODE.

## Usage
```
/cancel-schizo
```

## What Happens

1. Creates `./schizo-output/CANCEL` file
2. The next iteration of the schizo loop will detect this and stop
3. Prints abbreviated final report

## Output

```
╔══════════════════════════════════════╗
║    SCHIZO-MODE DEACTIVATED           ║
╠══════════════════════════════════════╣
║  The memes have been contained...    ║
║              for now.                ║
╚══════════════════════════════════════╝

Check ./schizo-output/ for artifacts created.
```

## Implementation

When this command is invoked:
```bash
mkdir -p ./schizo-output
touch ./schizo-output/CANCEL
```

Then print the deactivation message.
