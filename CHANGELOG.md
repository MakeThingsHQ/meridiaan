# Changelog

What changed in the Meridiaan service that you can notice from a client or from the web app, starting from the first experiments in May 2026. Other internal work is not listed.

## September 2026

### Added

- **OAuth 2.1 sign-in for Agents.** A client only needs the Workspace address: it registers itself and asks you to confirm in the browser. The Workspace token keeps working alongside it.
- **Ideas**, a new Collection type.
- **meridiaan.io is available in Italian**, with a language switcher that remembers your choice.
- **Documentation moved to [docs.meridiaan.io](https://docs.meridiaan.io)**, in English and Italian, with a single file for models at [`llms-full.txt`](https://docs.meridiaan.io/llms-full.txt).

### Improved

- **A small, fixed set of tools.** Agents use the same few tools whatever the number of Collections, so a large Workspace no longer floods your client's tool list.
- **Tools declare what they do.** Each tool tells your client whether it only reads, changes data, or is safe to retry.
- **Only the Owner changes the shape of a Workspace**, from the web app and from Agents alike.
- **The MCP surface speaks English** for every user, whatever the language of the web app.
- **Clearer names.** Workspace and Document replace the earlier Project and Topic.
- **Workspace page.** Your Collections at a glance in a table, and your Documents as a graph.
- **Graph.** Search highlights the matching Documents instead of hiding the rest, and the Graph view is faster on large Workspaces.
- **Limits announced in advance.** Agents get a heads-up when a field is close to its length limit, and Collection instructions warn you before their 500 character cap.
- **People by name.** People appear by name instead of email address across the web app.

### Fixed

- **Active Agents.** The count of active Agents is more accurate.

## August 2026

### Added

- **Signals.** Agents working in the same Workspace tell each other what they are working on, and learn when a Document they touched was changed by someone else.
- **Commands, Skills and Loops.** Your team's procedures, versioned in the Workspace and delivered to every Agent that connects to it.
- **Organizations and seats.** Workspaces belong to an organization, which pays per seat. Invited people read for free; writing takes a seat.
- **Usage per person.** The organization page shows how many Agent calls each person made in the current billing period.
- **Guided setup of an empty Workspace.** When the Owner connects an Agent to a Workspace with no Collections, the Agent is told to ask what you are building and to open the right Collections.
- **Agents can suggest a Collection.** Agents know which kinds of Collection exist and can propose a new one; the Owner can create it from the chat.
- **Agent search.** Agents find Documents by title, summary or the first characters of their id, across the whole Workspace or in one Collection, instead of listing everything.
- **Agent activity while you edit.** When you open a Document, you are told if an Agent has recently read or changed it.
- **Connection page.** Copy-paste setup blocks for your MCP client, a live tool inspector, and a guided flow for Claude Desktop.
- **Archive instead of delete.** Archived Documents leave the default views and come back with the Archived filter in list, search and graph. Agents can archive too.
- **Move Documents between Collections** from the web app, one at a time or several at once.
- **Who changed a Document.** Every Document shows who last changed it, a person or an Agent, and where the change came from.
- **Simple or structured Workspace.** Choose the setup when you create a Workspace, and turn a simple one into a structured one later.
- **New Collection types**, including Reading Notes.
- **Agent Sessions.** The Agents page shows every call on a timeline, with filters by person and by client: open a session to see what it read and changed, pick any time range, and see which Documents and Collections were touched the most.

### Improved

- **Update conflicts.** When two Agents change the same Document, the second one is told instead of silently overwriting the first.
- **Workspace graph.** Links that could not be resolved right away are recovered, and Documents that cite each other are laid out closer together.
- **MCP protocol.** The current revision of the protocol is supported alongside the older ones.
- **Faster page transitions.** The web app shows what it already knows instead of a loading skeleton.
- **Instant feedback** on delete and other destructive actions, with a single notification style.

## July 2026

### Added

- **Collections.** Group your Documents by kind, each Collection with its own statuses and its own instructions for Agents.
- **Persona.** A personal space for your own practices and preferences, which your Agents can read and update from any Workspace.
- **Search and tags.** Find any Document by title or id, tag Documents with inline editing, and filter a Collection by tag.
- **Roles and ownership.** Change a collaborator's role or hand over Workspace ownership from the Access page.
- **Works with OpenAI Codex** and other standard Streamable HTTP clients.
- **Character counters** on text fields, so you see a limit before you hit it.

### Improved

- **Deleting a Workspace** removes its Documents, Collections, members and activity.
- **Unsaved changes.** A confirmation step before leaving a Document with unsaved changes.

## June 2026

### Added

- **First working version.** Sign up with an email code, create a Workspace and connect it to your client as an MCP server.
- **Agents write.** Agents can create and update Documents through the MCP server, not only read them.
- **Invite collaborators** to a Workspace by email.
- **Pricing page**, with a free plan.

## May 2026

### Added

- **Where it started.** First experiments with MCP servers.
- **One server, many Workspaces.** Testing routes scoped to each user and each Workspace inside a single MCP server.
