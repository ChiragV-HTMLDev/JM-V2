JOYOUS MINERAL — WEBSITE PACKAGE
=================================

WHAT'S INSIDE
  index.html        The one-page website (open this in a browser to preview)
  css/style.css      All styling
  js/main.js          All animation / interaction logic (header, hero intro,
                      scroll reveals, sticky process section, pipeline,
                      grain-size counter, quality rings, contact form)
  contact.php         Server-side handler for the contact form
  assets/             Logo + your plant photographs, already optimized

HOW TO GO LIVE
  1. Upload the ENTIRE folder (keeping the same structure) to your web
     host via FTP/cPanel — a host that supports PHP (almost every shared
     host does).
  2. Open contact.php and check the two settings at the top:
       $to_email   -> already set to joyousmineral@gmail.com
       $from_email -> set to a no-reply@ address on your OWN domain once
                      you have one (e.g. no-reply@joyousmineral.com).
                      Many mail servers block/junk mail that claims to be
                      "from" a Gmail address it doesn't control.
  3. That's it — the form on the Contact section will POST to contact.php
     and email every enquiry straight to joyousmineral@gmail.com, with
     the visitor's email set as Reply-To so you can just hit "reply".

NOTES
  - The form has live validation (name, phone, email, message) with
    floating labels, inline error messages, and a success/error status
    line — all client-side in js/main.js, double-checked server-side in
    contact.php.
  - A hidden honeypot field blocks the most basic spam bots.
  - The Google Map uses a keyless embed (no API key needed). If you'd
    prefer the full Maps JavaScript API/Places experience later, that
    needs a Google Cloud API key with billing enabled.
  - GSAP (animation library) and Google Fonts load from public CDNs —
    the page needs an internet connection to show the full animated
    experience; layout and content still work without it.
  - Test the form on your live host: PHP mail() depends on the server's
    mail transport being configured. If messages don't arrive, most hosts
    let you switch to SMTP (ask your host for SMTP credentials) — happy
    to wire that in if mail() doesn't work on your setup.
