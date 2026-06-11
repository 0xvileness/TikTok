Tiktok is an OSINT tool to fetch details on verified accounts and scrapes data.
No API Required.

Functions:
Account creation date from a username, @handle, or profile URL, plus followers, likes, bio, verified, and private status.
Video upload time from a video URL or id (the snowflake timestamp, id >> 32).
Optional OSINT pivots (opt in): reverse image search of the avatar (Yandex / Google Lens / TinEye), Wayback Machine link, same-handle probes on Instagram / X / YouTube / Twitch / Reddit, and the bio link from the profile.

Optional integrity flags (opt in): heuristic signals for bought followers, follow farms, rapid growth, and handle / display-name changes that can hint at a rebrand, sale, or takeover.
Reports saved to reports/ as JSON and TXT.
A clean terminal UI, or a single command. No RapidAPI, no key, no card.

Note: you'll need python 3.11

Installation: 
pip3 install -r requirements.txt

Usage:

python3 tiktok_created.py user
python3 tiktok_created.py @user

# Optional extras (off by default)
python3 tiktok_created.py user --osint    # add pivot links
python3 tiktok_created.py user --flags    # add integrity heuristics
python3 tiktok_created.py user --all      # both
