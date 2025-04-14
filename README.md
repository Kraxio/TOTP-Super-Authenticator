# TOTP Super Authenticator

**TOTP Super Authenticator** to aplikacja okienkowa (GUI) w Pythonie, służąca do generowania jednorazowych kodów TOTP.  
Pozwala na:
- Logowanie przy użyciu PIN-u (przechowywanego w formie zahashowanej).
- Szyfrowanie tajnych kluczy (Fernet).
- Dodawanie kont poprzez ręczne wprowadzenie klucza lub skan kodu QR (z pliku lub ekranu).
- Eksport i import listy kont w formacie JSON (z zachowanym szyfrowaniem).
- Obsługę jednego okna z wbudowanym ekranem logowania i stylowy interfejs dzięki [ttkbootstrap](https://pypi.org/project/ttkbootstrap/).

## Funkcjonalności

- **Generowanie kodów TOTP** (zgodnie z RFC 6238).
- **Skanowanie kodów QR** za pomocą:
  - Plików graficznych (`.png`, `.jpg`, itp.).
  - Zrzutu ekranu (wymaga zainstalowanej biblioteki `pyautogui`).
- **Wbudowany mechanizm odświeżania** kodów co 30 sekund – wraz z odliczaniem w GUI.
- **Logowanie użytkownika** (hasło/PIN) i **zaszyfrowany plik z kontami**.
- **Jedno okno**: po udanej rejestracji/logowaniu ekran zmienia się w widok główny z listą kont.

## Wymagania

- Python 3.8+ (zalecany 3.10 lub nowszy)
- Zainstalowane pakiety:
  - `ttkbootstrap`
  - `cryptography`
  - `bcrypt`
  - `pyzbar`
  - `Pillow`
  - `qrcode`
  - *(opcjonalnie)* `pyautogui` – do skanowania QR z ekranu.
  
Instalacja wszystkich pakietów:
```bash
pip install -r requirements.txt
