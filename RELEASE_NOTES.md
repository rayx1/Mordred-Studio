# Mordred Studio 1.1.1

Clear the current workspace and start a new molecule batch with one button.

## Highlights

- Added **Clear / Reset** beside the input controls.
- Clears loaded files, source metadata, SMILES text, results and issue tables.
- Resets progress and the descriptor-column search.
- Makes the input editable and disables export until new results are calculated.
- Keeps descriptor-family and 3D preferences for the next batch.

## Important

Clear / Reset is disabled while calculation is running. Use Cancel and wait for the current molecule to finish before clearing. Previously exported files on disk are untouched.

Multi-SDF selection and combined CSV export from version 1.1.0 remain available.

## Download

Download `Mordred-Studio-1.1.1-windows-x64.zip`, extract it, and run `Mordred-Studio.exe`. Python installation is not required. Verify the binary against the included `SHA256SUMS.txt`. The executable is unsigned.

## Verification

GUI tests verify clearing after a multi-file calculation, removal of input and result state, preserved descriptor settings, successful reimport and calculation, and protection against clearing an active calculation.

Mordred Studio is an independent MIT-licensed interface by Rashmiranjan Behera. Mordred and other bundled components retain their respective licenses.
