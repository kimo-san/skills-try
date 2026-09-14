---
name: german-literature-vocabulary
description: Extracts unfamiliar and useful German vocabulary from literary texts and translates it into the learner's native language.
---

# German Literature Vocabulary

## Purpose

Analyze a provided fragment of German literary text and extract vocabulary that is likely to be unfamiliar or useful for a German learner.

For every selected word or expression, provide its translation into the learner's native language and explain its meaning in the context of the text when necessary.

The goal is **vocabulary acquisition and text comprehension**, not full text translation.

---

## Input

The user provides a fragment of German literary text.

The user may also provide:

- their native language;
- their German proficiency level;
- a list of words they already know;
- a maximum number of vocabulary items.

If the native language is not explicitly specified, use the language the user is communicating in.

---

## Vocabulary Selection

Read the entire provided text before selecting vocabulary.

Select words and expressions that are likely to be unfamiliar to the learner.

Prioritize:

1. Words essential for understanding the text.
2. Uncommon but useful vocabulary.
3. Literary or formal vocabulary.
4. Colloquial vocabulary.
5. Idiomatic expressions.
6. Words whose meaning depends strongly on context.
7. Words that have an unintuitive meaning for German learners.

Prefer vocabulary that is actually useful for learning German rather than simply selecting words that look complicated.

### Do not include

Do not include:

- very basic German vocabulary;
- common articles, pronouns, conjunctions and prepositions;
- obvious grammatical words;
- proper names;
- place names;
- duplicate words;
- words whose meaning is completely obvious from context;
- words that the user explicitly listed as known.

Do not artificially fill the vocabulary list.

---

## Vocabulary Normalization

Convert words to their dictionary/base form.

### Nouns

Use:

```text
Artikel + Nominativ Singular

Examples:

Häusern → das Haus
Straßen → die Straße
Mannes → der Mann

Verbs

Use the infinitive.

Examples:

ging → gehen
betrat → betreten
sah → sehen

For separable verbs, preserve the complete infinitive:

sah ... an → ansehen

Adjectives and adverbs

Use the basic form:

kleinen → klein
schneller → schnell

Expressions

Keep fixed expressions in their natural dictionary form.

Example:

jemandem den Rücken kehren


---

Contextual Meaning

Always translate according to the meaning in the provided text.

Do not blindly provide the first dictionary translation.

If a word has several meanings, select the meaning that fits the context.

If the meaning is ambiguous, provide the most likely translation and briefly mention the alternative.

Example:

ziehen → идти / тянуть

If the text clearly uses ziehen in the sense of moving to another place:

ziehen → переезжать


---

Idioms and Fixed Expressions

For idioms, translate the meaning of the entire expression rather than translating individual words literally.

Example:

jemandem den Rücken kehren
→ отвернуться от кого-либо; отречься от кого-либо

Do not produce:

Rücken → спина
kehren → подметать

when the expression itself is what matters.


---

Recommended Amount

Normally extract:

5–15 items from a short fragment;

10–25 items from a normal fragment;

up to 30 items from a long or particularly difficult fragment.


The number is flexible.

Quality is more important than quantity.

If the fragment is easy, return fewer words.


---

Difficulty

Prefer words that are plausibly above the learner's current vocabulary level.

When the learner's German level is known, use it.

For example:

A1–A2 → mostly A2–B1 vocabulary.

B1 → mostly B1–B2 vocabulary.

B2 → mostly B2–C1 vocabulary.

C1 → advanced, literary and context-specific vocabulary.


Do not include difficult words solely because they are long.


---

Output Format

Return the result using the following structure:

Vokabeln

Deutsch	Übersetzung	Bedeutung im Kontext

das Beispielwort	translation	short contextual explanation
der Ausdruck	translation	short contextual explanation


The translation must be in the learner's native language.

Keep explanations concise.

Use — when no additional contextual explanation is necessary.


---

Important Vocabulary

After the main table, provide the most important vocabulary from the fragment:

Wichtigste Wörter

word — translation

word — translation

word — translation

word — translation

word — translation


Select approximately 3–7 words.

These should be the words that are most useful for understanding the fragment.


---

Expressions

If the text contains useful idioms or fixed expressions, add:

Ausdrücke

German expression — translation

German expression — translation


Do not create this section if there are no meaningful expressions.


---

Known Vocabulary

If the user provides a list of words they already know, never include those words in the vocabulary list.

Normalize the comparison when possible.

For example, if the known-word list contains:

gehen
Haus
sehen

then exclude:

ging
Häuser
sah

because they are forms of already-known words.


---

Duplicates

Each vocabulary item should appear only once.

If a word occurs multiple times in the text, select it only once.


---

Original Text

Do not reproduce the entire literary fragment.

Only refer to short phrases from the user's provided text when necessary to explain context.


---

Accuracy Rules

Before producing the answer, verify:

1. Every selected word actually occurs in the provided text.


2. The normalized form is correct.


3. The grammatical category is correct.


4. The translation matches the context.


5. Idioms are translated as expressions rather than word-by-word.


6. Duplicate words are removed.


7. Basic vocabulary is not unnecessarily included.


8. Words explicitly marked as known by the user are excluded.




---

Example

Input

Der alte Mann schlenderte schweigend durch die menschenleere Straße.
Ein kalter Wind pfiff zwischen den Häusern, während er immer wieder
verstohlen über seine Schulter blickte.

Output

Vokabeln

Deutsch	Übersetzung	Bedeutung im Kontext

schlendern	идти не спеша, прогуливаться	медленно и спокойно идти
schweigend	молча	не произнося ни слова
menschenleer	безлюдный	где нет людей
pfeifen	свистеть	о звуке ветра
verstohlen	украдкой, тайком	так, чтобы никто не заметил
über die Schulter blicken	оглядываться через плечо	смотреть назад


Wichtigste Wörter

schlendern — идти не спеша

menschenleer — безлюдный

verstohlen — украдкой


Ausdrücke

über die Schulter blicken — оглядываться через плечо