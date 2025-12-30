# Chinkiang Customs Ledger Transcription Project (July 1841)

## Project Overview

This repository contains a collaborative transcription of a single page from the Chinkiang customs ledger dated July 1841, just before the city's capture during the First Opium War. The ledger details daily imports and exports, providing a snapshot of commercial activity at a critical historical moment.

The goal of this project is to create a clean, machine‑readable dataset from a high‑resolution scan of the original document. The final dataset will be used for quantitative analysis of the immediate commercial impact of the war on the treaty port of Chinkiang.

## Dataset Structure

The transcribed data will be stored in `trade_data.csv` with the following columns:

- **Date** (format: YYYY‑MM‑DD) – the calendar date of the transaction.
- **Commodity** – the type of good (e.g., raw silk, tea, ginseng, cotton cloth).
- **Quantity** – the amount of the commodity, recorded in the unit used in the original ledger (e.g., piculs, catties, bales, pieces).
- **Origin_Destination** – the port or location from which the commodity came or to which it was sent (abbreviations explained below).
- **Duty_Taels** – the customs duty paid, recorded in taels of silver to two decimal places.

## Transcription Guidelines

1. **Dates**: Convert the lunar‑calendar dates found in the ledger to Gregorian dates using the provided conversion table (available in the seminar materials). Enter dates in ISO 8601 format (`YYYY‑MM‑DD`).

2. **Commodities**: Transcribe the commodity names exactly as they appear in the ledger. If a commodity name is abbreviated in the original, expand it using the standard abbreviation key (e.g., “Raw Silk” for “R.S.”).

3. **Quantities**: Record the numerical quantity as written. If the unit is not explicitly stated, infer it from the column heading or the surrounding entries and note the assumption in the relevant Issue.

4. **Origin/Destination**: Use the following three‑letter abbreviations for major ports:
   - **CTN** – Canton
   - **SHG** – Shanghai
   - **NGB** – Ningbo
   - **AMY** – Amoy (Xiamen)
   - **FZH** – Fuzhou
   - **TWN** – Taiwan
   - **OTH** – Other (specify in a note if possible)

   For domestic locations not listed, transcribe the Chinese characters as they appear and add a note in the corresponding Issue.

5. **Monetary values**: All duties are recorded in **taels of silver**. Convert any fractional amounts to two decimal places (e.g., `12.50`). If the original entry is illegible or ambiguous, create a new Issue with a cropped image of the cell and a description of the problem.

6. **Illegible entries**: If a word or number cannot be read with confidence, enter `[illegible]` in the cell and immediately open an Issue titled “Ambiguous Entry in Row X” with a detailed description and, if possible, a cropped image of the problematic cell.

## Workflow

1. Each student is assigned a block of rows (see the “Project Kick‑off” Issue).
2. Students fork the repository, create a branch named after themselves, and transcribe their assigned rows into `trade_data.csv`.
3. When finished, they open a Pull Request with the title “Transcription: Rows X‑Y”.
4. All other participants review the changes in the “Files changed” tab, adding inline comments on any suspected errors.
5. Once all comments are resolved, the Pull Request is merged (squash‑and‑merge) into the `main` branch.

## Repository Contents

- `README.md` – this file.
- `ledger_scan.jpg` – a high‑resolution scan of the ledger page (placeholder in this repository; the full‑resolution image is available on the seminar’s shared drive).
- `trade_data.csv` – the target dataset, initially containing only the header row.

## Acknowledgments

This project is part of a university research seminar on the economic history of Chinese treaty ports. We thank the archivists who provided access to the original ledger.