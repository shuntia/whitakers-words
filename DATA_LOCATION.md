# Data Files Location

The dictionary data files (*.GEN, *.LAT, *.SEC) have been moved to `/data/` directory at the project root for better organization.

## Files Moved

The following files are now in `/data/`:
- `*.GEN` - Generated dictionary and stem files
- `*.LAT` - Latin dictionary source files
- `*.SEC` - Inflection data files
- `WORK.*` - Working files
- `CHECKEWD.*` - Working files

## Source Code

This directory (`whitakers-words/`) still contains:
- Source code (`src/`)
- Build system (Makefile, *.gpr files)
- Libraries (`lib/`)
- Tests (`test/`)
- Documentation (HOWTO.txt, LICENCE.txt)

## Building

To rebuild the dictionary data or binary:

```bash
cd whitakers-words
make
```

The binary will be placed in `whitakers-words/bin/words` and should be copied to the project root's `bin/` directory.

## API Usage

The API route (`src/app/api/lookup/route.ts`) now references:
- Binary: `/bin/words`
- Data directory: `/data/`
