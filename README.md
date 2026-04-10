# OOK Signal Explorer

Interactive Streamlit app for understanding On-Off Keying (OOK) RF signals, built during the [Sofucor ceiling fan reverse-engineering project](https://github.com/tclancy/radiofrequency).

## What it teaches

- How OOK pulse-distance modulation encodes bits (short gap = 0, long gap = 1)
- Why `rtl_fm` output looks "inverted" in Audacity (carrier ON = quiet, carrier OFF = noisy)
- How to read individual bits from a waveform
- How address and command bits combine in a 32-bit RF packet

## Run locally

```bash
pip install -r requirements.txt
streamlit run signal_explorer.py
```

## Deploy to Streamlit Community Cloud

1. Fork or connect this repo to [share.streamlit.io](https://share.streamlit.io)
2. Set the main file path to `signal_explorer.py`
3. Deploy — no environment variables or secrets needed

## Data

`sofucor_fan.yaml` contains the decoded protocol for two Sofucor ceiling fans — timing values, addresses, and commands all verified against real captures.

## Files

| File | Purpose |
|------|---------|
| `signal_explorer.py` | Streamlit app — run this |
| `sofucor_fan.yaml` | Device profile (timing, addresses, commands) |
| `requirements.txt` | Python dependencies |
