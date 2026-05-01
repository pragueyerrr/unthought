# Unthought -- https:/unthought.io

*If you're from O'Shaughnessy Ventures — I left something for you here.*

---

## What This Is

**Unthought** is a philosophy, a participatory installation, a data project, and the first physical instantiation of a thirty-year intellectual practice that finally found its name.

The name is precise. Not *unthinking* — which implies carelessness. **Unthought** — existing prior to thought. The self that acts before the self that performs.

---

## The Core Idea

We are a tapestry made of all the routes we take without thinking.

Not the decisions we make consciously. Not the destinations we choose. The automatic, prereflective, unintentional choices — the paths the body takes while the mind is elsewhere. These reveal something truer about who we are than anything we decide to perform or present.

The first project maps this. People trace their unreflective daily routes — the paths taken through cities, parks, lives, without destination as the primary intention — and layer them on top of each other into collective physical terrain. Individual habit becomes landscape. Mountains form where everyone turns left without thinking. Valleys appear where the road nobody takes runs quietly through. A ridge emerges where two different kinds of people make the same choice for completely different reasons.

Route terrain. The city, and the self, revealed through accumulation.

---

## Where It Came From

Freshman year in New York. Walking back to my dorm with someone who would become one of my closest friends — our first genuine solo interaction. I noticed something immediately and never stopped thinking about it.

She navigated the Manhattan grid entirely by availability. Every time a signal turned green around her, she moved in that direction while traveling toward the general destination. No fixed route. Just direction and total responsiveness to what was open in the moment.

I had been taking the exact same turns every single day for a week without once registering that I was making a choice. Same sequence, same timing, same turns. The most legible possible grid — numbered, ordered, optimized for navigation — and I had reduced it to a single path.

She was mycelial. I was linear. And I saw the difference instantly.

That observation never resolved. It sat for eleven years, gathering context.

The context it gathered: a lifelong obsession with the structure beneath the structure. With mycelium — not as metaphor but as mirror. The invisible network that quietly connects everything, accomplishes without announcing, branches in all directions without needing to explain itself. With trees — their generosity, their scale, their way of being alive that requires no legibility.

And three books I loved enough to tattoo on my body before I understood they were all the same idea:

- *The Mushroom at the End of the World* — Anna Tsing. Entanglement, the mycelial network as model for how lives and systems actually connect and produce meaning. The polyphonic, multi-species story of what grows in the ruins.
- *The Poetics of Space* — Gaston Bachelard. The phenomenology of intimate space — corners, nests, drawers — the architecture of the inner life that we inhabit without naming. The philosophical project of attending to what we take for granted.
- *The Overstory* — Richard Powers. Deep time. Rootedness. The intelligence of systems that operate on timescales we can't perceive from inside them. What exists beneath the visible surface, accomplishing everything without announcement.

Three distinct intellectual traditions. One unified question: what exists beneath the threshold of intentional consciousness, and what does it reveal about how we actually live?

I had a fully formed philosophy living in my body, expressed through tattooed books, before I had a name for it.

The name is Unthought.

---

## What Makes It Different

The world is filling with maps of what people consciously choose. Pins dropped on places enjoyed, moments decided to remember, experiences curated and saved. Every pin is a thought. These are maps of the intentional self — the self that decided something was worth keeping.

Unthought is interested in the opposite.

The path *between* the pins. The route the body takes to get from one saved place to the next, without the mind registering it as worth saving. The unconscious connective tissue between moments of noticing. The part that never gets documented because it never rises to the level of a decision.

The Manhattan grid is the perfect illustration: inside maximum legibility, she found a mycelial path. The mycelial way of moving isn't the absence of structure — it's a different relationship to structure. Using the grid without being governed by it.

Unthought maps the governance. And the freedom from it. And the difference between them, rendered as terrain.

---

## The First Project

### The Data Collection

Weekly sessions. Participants trace their unreflective daily routes from memory — paths through their city taken habitually, without thought, the routes the body chose rather than the mind decided.

They also document a second thing: a constraint, real or imagined, they navigate regularly without fully acknowledging it. The building they avoid without knowing why. The side of the street they always take. The turn they never make.

This is the philosophically rich data point — the constraint that shapes movement before the question of movement is ever consciously raised. It is also the hardest to collect honestly. The methodology must create conditions where a genuine answer is possible rather than a performed one.

### The Data Schema

Each participant session produces:

- `route_id` — unique identifier
- `participant_id` — anonymized
- `route_geometry` — GeoJSON LineString (the traced path)
- `route_type` — daily commute / habitual / unintentional park / other
- `constraint_noted` — text field, the acknowledged navigation
- `collection_date`, `city`, `neighborhood`
- `session_notes`

Routes are collected in collaboration with NYU, where a professor in urban studies has agreed to involve students in data collection as part of a structured research partnership. This gives the project academic infrastructure, diverse participants, and institutional credibility from the beginning.

### The Installation

The layered route data becomes physical terrain — a large-scale sculptural map where accumulated routes create topography. Mountains of habit. Valleys of the overlooked. The ridge where two different kinds of people made the same choice for entirely different reasons.

The body of the viewer should be inside the data, not looking at it from outside. Scale is a philosophical commitment, not an aesthetic preference.

The installation is not the project. It is the most tangible, graspable entry point into something that has no ceiling.

---

## The Technical Proof of Concept

**[Threadthulhu](https://github.com/pragueyerrr/threadthulhu)** — an interactive visualization of 206,000 tweets, built as a creative act of making a mind's mycelial structure visible.

It was built with no engineering background. The intent came first. The technical execution followed the intent.

Threadthulhu is an accidental prototype for Unthought: a large body of data rendered as navigable, spatial, living structure rather than list or timeline. The methodology of making invisible networks physical and explorable is the same. The data domain is different.

---

## What We Know

The philosophical framework is settled. The core distinction — prereflective vs. reflective self, the path between the pins, the unthought as object of study — is precise and defensible.

The data schema is drafted (above). The NYU collaboration is confirmed. The long-form vision is clear: the methodology becomes transmissible. Other universities, other cities, other contexts replicate it. The prereflective self becomes a legitimate object of collective study — the way the unconscious became one after Freud, not because anyone set out to create a field, but because the work was precise enough that the field grew around it.

City planning changes because of what the terrain revealed.

Unthought propagates without me. Mycelially.

---

## What We're Still Figuring Out

These are named honestly because intellectual honesty is part of the project's practice. If you're reading this and have thoughts on any of these, that's exactly the kind of conversation this README is trying to start.

**The paper-to-coordinate problem** — the central unsolved technical question. A participant draws a route from memory on paper. How does that become a GeoJSON LineString? Options include georeferenced paper maps photographed and processed, digital tracing on a tablet after the fact, or direct tablet input during the session. Each has tradeoffs between presence and precision. The most phenomenologically honest collection method may produce the least technically usable data. This question is load-bearing — everything downstream depends on its answer.

**Dubai is a car city** — most participants will trace routes driven, not walked. A car route from memory will be radically imprecise: people navigate by landmark, not street name. The methodology needs to account for landmark-based wayfinding versus street-based, and for the different phenomenology of unreflective car travel versus foot travel. These may not be the same kind of Unthought.

**Who attends the sessions, and how** — the data quality and diversity depends entirely on activation. What brings people to a weekly session to trace their routes from memory? What makes them willing to name the constraint they navigate without acknowledging?

**Longitudinal vs. cross-sectional** — one route per person once, or the same person's route over weeks and months? Longitudinal data is far more philosophically interesting — it captures drift, the way habitual paths shift with seasons, relationships, mood. It is also significantly harder to collect.

**The constraint question** — this is the most philosophically rich data point and the one most likely to produce a performance rather than a genuine answer. How do you create session conditions where an honest response is possible? What does the room look like? What does the facilitator do?

**The AI question** — there is a live possibility that the visualization and analysis layer becomes primarily AI-leveraged. What that looks like precisely is still forming. It may become the whole thing.

**Studio** — large-scale installation work cannot be done from home. Studio space in Dubai or Abu Dhabi needs to be secured. Tashkeel has residency programs that embed artists in community and provide exhibition infrastructure. This is the right ecosystem but the right space within it is still being found.

**The README audience** — who is this for? OSV has seen the application. The live audience is: collaborators to find, academics who might engage with the methodology, artists who might want to participate, and future me returning after months away. Those audiences want different things from the same document.

---

## The Long Vision

The installation is proof of concept. The methodology is the thing.

If the methodology is precise enough — if the data is real, the analysis rigorous, the translation into terrain honest — then Unthought becomes a framework that doesn't stay an art project. Urban planning engages it. Psychology circles it. Philosophy names it. Neuroscience finds the same phenomenon from another angle. Fields that have been looking at the prereflective self from different directions without a unified framework discover they've been describing the same thing.

Unthought names it. The installation is the first proof that the framework produces real knowledge.

In the wildest version, someone builds a city using Unthought data. Policy changes because of what the terrain revealed. And the methodology propagates — other researchers, other universities, other contexts running the same study without me needing to be there. The way a rigorous research methodology propagates once it's precise enough.

The wildest version is not me building it everywhere. It's the idea escaping me entirely.

---

## What I'm Looking For

If you have expertise in:
- Geospatial data processing and the paper-to-coordinate problem specifically
- Large-scale physical installation design and fabrication
- Phenomenology, prereflective consciousness, Merleau-Ponty adjacent research
- Urban data and the phenomenology of movement through cities
- AI-leveraged data visualization
- Running participatory data collection with general publics

...this README is for you. The open questions above are genuine invitations.

And if you're simply someone who has spent time thinking about the self that exists before the performing self — I want to hear from you.

---

## The Intellectual Lineage

The philosophical ancestor of this project is Maurice Merleau-Ponty, specifically his work on the lived body and the primacy of perception. The prereflective self — the body that navigates the world before consciousness catches up — is his territory. Unthought is what happens when you try to collect data on it.

The practical ancestors are the three tattooed books: Tsing, Bachelard, Powers. Entanglement. The architecture of the inner life. Deep time and rootedness. All three attend to what exists beneath the threshold of intentional documentation.

The technical ancestor is Threadthulhu — proof that a large body of unstructured data can be rendered as spatial, navigable, living structure rather than list.

The personal ancestor is a friend walking through Manhattan by following green lights, eleven years ago, while I took the same turns I always took.

---

*The marble was always this shape. We just chipped until it was visible.*
