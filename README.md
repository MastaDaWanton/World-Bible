# World-Bible
An Ai assisted generator for a fictional world with over a millon combinations of premise. It outputs and ecyclopedic entry and can be edited manually or with continued AI assistance.

World Bible
Generate and read complete world bibles, entirely on your own machine.

1. Before you start
2. Your first run
3. Choosing your models
4. Making a world
5. Growing it
6. Editing and fixing
7. The chronicle
8. Exporting your book
9. Where your work lives
10. Making it faster
11. Troubleshooting
1. Before you start
World Bible writes with a large language model. You need to give it one, and you have two choices.

Run it on your own machine — free and private, but slow
Install Ollama from ollama.com, then pull a model. From a terminal:

ollama pull llama3.1:8b

Nothing you write ever leaves your computer, and it costs nothing to run. The trade is speed: your graphics card is doing work that a data centre would otherwise do.

Or use a hosted service — much faster, costs money
World Bible also speaks to Anthropic, OpenAI and Google Gemini. You supply an API key during setup. Your prompts are sent to that company's servers and you pay per world, but generation stops being something you wait an hour for.

Speed is your choice of model, not the app. On a local 8B model expect roughly two minutes per entity, so a world of thirty entities takes about an hour. Point the same app at a hosted model and that world finishes in minutes. If generation feels slow, that is the cost of keeping everything on your own machine — it is not a limit of the app, and you can change it at any time in Settings.
You can also mix the two: a hosted model as Generator for speed, a local one as Proofreader, or the reverse. Neither role is locked to a provider.

2. Your first run
The app opens with a finished sample world, Pangrella, already loaded. Nothing was generated on your machine to produce it — it ships with the app so you can see what a finished world looks like before committing an hour to your own.

Read it, click through its cross-references, export it to a book, take it apart. It is an ordinary world in every respect: you can edit it, rename it, or delete it. If you delete it, it stays deleted — it will not reappear next time you launch.

3. Choosing your models
On first launch a setup wizard asks for two roles:

Role	What it does
Generator	Writes the prose. This is the voice of your world.
Proofreader	Scores each draft and rewrites what falls short.
If Ollama is running, the wizard finds it and lists your installed models. A tested pairing is llama3.1:8b as Generator and deepseek-r1:8b as Proofreader.

The Proofreader earns its keep. It is not a spell-check pass — it reads each draft against the world's established facts, scores it, and rewrites the weak parts. Drafts that score badly are sent back to be rewritten. Using a weaker model here shows up directly in your prose as flat, repetitive description.
You can change either model later in Settings.

4. Making a world
Click New World. You will be asked for:

A premise — rolled for you across several axes. Reroll until something catches your eye. This becomes a hard constraint every part of the world must obey, which is what stops every generated world feeling like the same world.
A name — used exactly as you type it, everywhere.
Physical laws and the exceptional, in detail — how your world works, and what breaks those rules.
An export folder — where finished books are written.
Then the app builds the world's foundation. Watch the work panel for progress; you can keep browsing while it runs.

5. Growing it
A world is a tree, six levels deep:

World → Continent → People and Nations → Cities → Characters

Open any entity and use Expand to generate its children. A nation grows cities; a city grows characters. Each new entity inherits everything established above it, so a city knows the laws of its nation and the history of its continent.

Pinned people
As the world writes itself it names people it never describes — a general in a battle account, a founder in a myth. The app notices these and pins them: a queue of named-but-never-written figures. Create them one at a time, or all at once, and they arrive already knowing where they belong.

6. Editing and fixing
Edit — change any text by hand. It is your world.
Regenerate — rewrite an entity from scratch. Its name and place in the world are kept.
Restore — every change keeps a history. Nothing is lost.
Rename — renames the entity and every mention of it across the whole world, including possessives. Its folder is renamed too.
Move — relocate an entity to a different parent; links follow it.
7. The chronicle
Your world's timeline starts as one-line stubs — "The Great Drying" with a date. The Chronicle pass turns each into a real account: the pressure that built beforehand, the decisive turns within it, who is remembered for it, and what it settled.

It is additive and resumable. Run it once, add entities later, run it again — it only fills in what is missing.

8. Exporting your book
Format	Best for
HTML	Reading. A single self-contained page with working cross-references, a chronology and reference cards. Open it in any browser; send it to anyone.
Word (.docx)	Editing elsewhere, printing, publishing.
Markdown	Feeding into other tools, or version control.
9. Where your work lives
What	Where
Your worlds	Documents\World Bibles
Settings and database	%LOCALAPPDATA%\WorldBible
Worlds are plain folders of readable JSON files — not a database. To back one up, copy the folder. To share one, zip it. To move to a new computer, copy it across. Nothing is locked inside the app.

Back up your worlds. A finished world is hours of generation. Copy the folder somewhere safe when you finish one.
10. Making it faster
If you are using a hosted model, skip this section — you are already running as fast as the app goes. Everything below is about local models, where the work is happening on your own graphics card.

With a local model, speed is almost entirely your graphics card, and the single biggest factor is usually heat rather than anything in this app.

Check your GPU is not throttling. A card that overheats quietly drops its clock speed. On one test machine, fixing case fans and undervolting the card cut generation time by 37% with no change to output quality.
Use a model that fits in your VRAM. If the model is larger than your card's memory it spills into system RAM and slows by roughly ten times.
Close other GPU work — games, video editors, other AI tools.
Or stop using a local model. Everything above buys you tens of percent. Switching the Generator to a hosted model in Settings turns an hour into minutes, and it is a two-field change — see section 1 for what you give up.
Using a smaller or faster model for the Proofreader is a false economy — it scores drafts badly, which triggers more rewrite attempts, and the build ends up slower and worse.

11. Troubleshooting
"Could not reach the server" or generation never starts
Ollama is probably not running. Start it and try again. You can confirm it is up by opening http://localhost:11434 in a browser — it should say "Ollama is running".

Generation is extremely slow
See section 10. Check your model fits in VRAM, and check your card's temperature under load.

A build stopped partway
A partial world is a valid world here. Everything already written is saved. Open the entity that failed and regenerate it, or expand from where it stopped.

An entity is called the wrong name
Use Rename rather than editing the text by hand — it corrects every mention across the entire world, which hand-editing will miss.

The app will not close
If generation is still running you will be asked to confirm. Work already finished is saved; the entity in progress is not.

World Bible — everything runs on your machine unless you choose otherwise.
