# Japanese Flashcards Project

This project is a collection of interactive, web-based flashcards designed for learning Japanese Katakana and Kanji vocabulary. Each flashcard set is a standalone HTML file that contains its own data and logic.

## Directory Overview

The project consists of static HTML files that provide a user-friendly interface for practicing Japanese vocabulary. The flashcards support multiple study modes, including starting with the Japanese term, the definition, or the reading.

### Key Technologies
- **HTML5/JavaScript**: Core structure and interactivity.
- **Tailwind CSS**: Styling and responsive design (loaded via CDN).
- **Google Fonts**: Custom Japanese fonts (`Noto Sans JP`, `Noto Serif JP`).
- **Speech Synthensis**:  Speak word and translate example text

## Key Files

- `katakanaflashcards.html`: Interactive flashcards for Katakana-based vocabulary.
- `unit6flashcards.html`: Interactive flashcards for Unit 6 Kanji vocabulary.

## Project Structure

Each HTML file follows a consistent internal structure:
1. **Header**: Includes Tailwind CSS and custom font styles.
2. **UI Components**: A card display area, navigation buttons (Prev, Next, Shuffle), and a "Start with" selector.
3. **Data**: Vocabulary is stored as an array of objects within a `<script>` tag. Each object typically includes:
   - `kanji`: The Japanese term (Kanji or Katakana).
   - `hiragana`: The reading in Hiragana (if applicable).
   - `romaji`: The Romanized reading.
   - `definition`: The English meaning.
   - `example`: An example sentence.
4. **Logic**: JavaScript handles card shuffling, cycling through phases (Kanji -> Meaning -> Reading), and keyboard navigation.

## Usage

To use the flashcards, simply open any of the `.html` files in a web browser.

### Controls
- **Tap/Click Card / Space / Enter**: Cycle through the current card's phases (Term -> Meaning -> Reading).
  - Phase 0:  Display Kanji / Katakana and example
    * With voice speaker icon and Google Translation link for the word and example text
  - Phase 1:  Display meaning / definition
  - Phase 2:  Display hiragana and romanji
- **Next / Arrow Right**: Move to the next card.
- **Prev / Arrow Left**: Move to the previous card.
- **Shuffle**: Randomize the current deck.
- **Start with**: Change the initial phase for new cards.

## Development Notes

- **Modifying Vocabulary**: To add or edit words, update the `vocabulary` array within the `<script>` tag of the respective HTML file.
- **Styling**: Styles are primarily handled via Tailwind CSS classes. Custom font overrides are in the `<style>` block.
- **Portability**: Each file is self-contained (except for external CSS/font CDNs), making them easy to share and use offline if the assets are cached.
