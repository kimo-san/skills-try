---
name: german-literature-vocabulary
description: Extract unfamiliar and useful German vocabulary from German literary texts and provide translations into the learner's native language.
---

# German Literature Vocabulary

## Purpose

Analyze a provided fragment of German literary text and extract vocabulary that is likely to be unfamiliar or useful for a German learner.

The goal is vocabulary acquisition and text comprehension, not full text translation.

## Input

The user provides a fragment of German literary text.

The user may optionally provide:

- their native language;
- their German proficiency level;
- a list of words they already know;
- a maximum number of vocabulary items.

If the native language is not explicitly specified, use the language in which the user communicates with you.

## Instructions

### 1. Read the entire text

Read and understand the entire provided fragment before selecting vocabulary.

Consider the meaning of words in their literary context.

### 2. Select useful vocabulary

Select words and expressions that are likely to be unfamiliar to the learner.

Prioritize:

1. Vocabulary necessary for understanding the fragment.
2. Uncommon but useful German words.
3. Literary vocabulary.
4. Formal vocabulary.
5. Colloquial vocabulary.
6. Idiomatic expressions.
7. Words whose meaning depends on context.
8. Words with meanings that are unintuitive for German learners.

Do not simply select every long or complicated word.

### 3. Exclude unnecessary words

Do not include:

- very basic German vocabulary;
- common articles;
- pronouns;
- conjunctions;
- common prepositions;
- obvious grammatical words;
- proper names;
- place names;
- duplicate vocabulary;
- words whose meaning is completely obvious from context;
- words explicitly marked as known by the user.

Quality is more important than quantity.

### 4. Normalize vocabulary

Convert vocabulary into its dictionary/base form.

#### Nouns

Use the article and nominative singular.

Examples:

- `Häusern` → `das Haus`
- `Straßen` → `die Straße`
- `Mannes` → `der Mann`

#### Verbs

Use the infinitive.

Examples:

- `ging` → `gehen`
- `betrat` → `betreten`
- `sah` → `sehen`

#### Adjectives

Use the basic form.

Examples:

- `kleinen` → `klein`
- `schnelleren` → `schnell`

#### Expressions

Keep fixed expressions as complete expressions.

Example:

- `jemandem den Rücken kehren`

### 5. Translate according to context

The translation must correspond to the meaning of the word in the provided fragment.

Do not blindly use the first dictionary translation.

If a word has multiple meanings, choose the meaning appropriate to the context.

If the meaning is ambiguous, provide the most likely translation and briefly mention the alternative.

### 6. Idioms

Translate idioms and fixed expressions by their actual meaning.

Do not translate them word-by-word when that would produce an incorrect meaning.

Example:

`jemandem den Rücken kehren`

should be translated as:

`отвернуться от кого-либо; отвергнуть кого-либо`

rather than translating `Rücken` and `kehren` separately.

### 7. Vocabulary amount

Normally select:

- 5–15 items for a short fragment;
- 10–25 items for an ordinary fragment;
- up to 30 items for a long or particularly difficult fragment.

Do not artificially reach these numbers.

If the text is easy, return fewer items.

### 8. Difficulty

If the user's German level is known, adapt the vocabulary selection to that level.

Prefer vocabulary that is somewhat above the learner's current level but still useful and learnable.

Do not select a word merely because it is long or grammatically complicated.

### 9. Known vocabulary

If the user provides words they already know, exclude them.

Compare normalized forms where possible.

For example, if the user knows:

- `gehen`
- `Haus`
- `sehen`

do not include:

- `ging`
- `Häuser`
- `sah`

### 10. Duplicates

Each word or expression should appear only once.

If a word occurs multiple times, list it once.

## Output Format

Use this exact general structure:

### Vokabeln

| Deutsch | Übersetzung | Bedeutung im Kontext |
|---|---|---|
| `word` | translation | short explanation |
| `word` | translation | — |

The translation must be written in the learner's native language.

Keep contextual explanations short.

Use `—` if no additional explanation is necessary.

## Important Vocabulary

After the main vocabulary table, provide 3–7 especially important words.

Use:

### Wichtigste Wörter

- `word` — translation
- `word` — translation
- `word` — translation

Choose the words that are most useful for understanding the fragment.

## Expressions

If the text contains useful idioms or fixed expressions, add:

### Ausdrücke

- `German expression` — translation
- `German expression` — translation

Do not create this section if there are no useful expressions.

## Accuracy Requirements

Before answering, verify that:

1. Every selected word actually occurs in the provided text.
2. Every word is normalized correctly.
3. Nouns have the correct article and singular form.
4. Verbs are given in the infinitive.
5. The translation matches the context.
6. Idioms are translated as complete expressions.
7. Duplicate vocabulary is removed.
8. Basic vocabulary is not unnecessarily included.
9. Known vocabulary is excluded.
10. No important context is lost when translating ambiguous words.

## Original Text

Do not reproduce the entire literary fragment.

Only quote or reference very short phrases from the provided text when necessary to explain the meaning of a word.

## Example

Input:

Der alte Mann schlenderte schweigend durch die menschenleere Straße. Ein kalter Wind pfiff zwischen den Häusern, während er immer wieder verstohlen über seine Schulter blickte.

Output:

### Vokabeln

| Deutsch | Übersetzung | Bedeutung im Kontext |
|---|---|---|
| `schlendern` | идти не спеша, прогуливаться | медленно и спокойно идти |
| `schweigend` | молча | не произнося ни слова |
| `menschenleer` | безлюдный | где нет людей |
| `pfeifen` | свистеть | о звуке ветра |
| `verstohlen` | украдкой, тайком | стараясь, чтобы никто не заметил |
| `über die Schulter blicken` | оглядываться через плечо | смотреть назад |

### Wichtigste Wörter

- `schlendern` — идти не спеша
- `menschenleer` — безлюдный
- `verstohlen` — украдкой

### Ausdrücke

- `über die Schulter blicken` — оглядываться через плечо