# Slide decks

## [Same Model, Different Paradigm](same-model/)

A live, phone-polled talk about how we use Claude and GPT. `same-model/index.html` is the deck, the phone voting page and the results panel in one file.

- Open the page to present. The QR code on screen opens the voting page on phones.
- Keys: `→` next, `←` back, `↓` bonus poll, `A` results and setup, `Q` big QR code, `D` demo data, `F` full screen, `T` timer, `L` bright room, `W` lab wall.
- Answers travel through the public ntfy.sh relay by default (about 25 phones per Wi-Fi). For a bigger room, add a Firebase Realtime Database URL in the `A` panel.

### Lab wall (six screens in a row)

The deck can drive a row of six 640×360 screens (a 3840×1080 output with the screens in the middle band, as in the Lab Display Composer). Screen 1 shows which question you are on, screens 2–5 show the slide, and screen 6 shows the join code and the phone count. Results and word clouds are live on the wall too.

1. On the laptop, open the deck from GitHub Pages, press `W` (the HUD shows **Wall**), then `A` → **Lab wall** for the wall link: `…/same-model/#w.<session>`.
2. On the workstation, open that link in Chrome and press `F11` (or start Chrome with `--kiosk "<link>"`). `C` shows the screen numbers to check alignment.

The wall follows the deck through the same relay or Firebase database as the phones, so both computers only need internet access, not the same network. The deck sends one small message per slide change, and only while the wall is on. The link stays the same between talks, and after **Start a new session** the wall moves to the new one by itself. To change the screen layout, edit `CONFIG.wall` at the top of the script.
