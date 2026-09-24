# Contributing

The Meridiaan service is closed source, but this repository is open, and three kinds of contribution help everyone:

1. **Client reports.** You connected a client: tell us whether the configuration in [`clients/`](clients/) worked as written, with the client version. A "worked" report is as useful as a "did not work" one. Use the [client report form](../../issues/new?template=client_report.yml).
2. **New client configurations.** Got a tool we do not list working? Open a pull request with a new file in `clients/`, following the shape of the others, and mark it "Not yet verified" unless a second person confirms it.
3. **Workspace templates.** A structure that works for your kind of project: a pull request with a new file in `templates/`, with the Collections table and the setup prompt.

## Rules for anything you submit

- Never include a real token, Workspace id, or anything from a private Workspace.
- Plain, direct English. Short sentences beat clever ones.
- One change per pull request.
