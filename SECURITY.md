# Security

Yui connects people's devices to agents that can act on their behalf, so we take security reports seriously.

## Reporting a problem

Please do not open a public issue for a security problem.

- Preferred: use GitHub's private reporting. Go to the Security tab of this repo and click "Report a vulnerability".
- Or email chris@postscarcity.ai with "Yui security" in the subject.

Tell us what you found, how to reproduce it, and what an attacker could do with it. We will reply within three business days, keep you posted while we fix it, and credit you in the progress log if you want.

## Scope

This repo (Yui for Apple Watch), and anything in it that lets one Yui user read or change another user's data, or lets someone pose as a connected agent. The backend and the iPhone app are covered in [postscarcityai/yui](https://github.com/postscarcityai/yui/blob/main/SECURITY.md), the parsers and the site in [postscarcityai/yuigui](https://github.com/postscarcityai/yuigui/blob/main/SECURITY.md).

Never commit a real secret. The only key a Yui client may carry is the backend's publishable key, which is public by design.

## Supported versions

Yui is pre-release. Only the latest commit on `main` gets fixes.
