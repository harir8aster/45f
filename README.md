# VLESS-WS on Fly.io

Single fixed user, no database. Settings come from Fly secrets:

- `SECRET_KEY` (required, min 16 chars)
- `USER_UUID` (any valid UUID; if omitted it is derived from SECRET_KEY)

Deploy (flyctl):

    fly launch --copy-config --no-deploy
    fly secrets set SECRET_KEY=... USER_UUID=...
    fly deploy

Then open `https://<app>.fly.dev/panel/<USER_UUID>` for the VLESS link, copy button and QR code.
