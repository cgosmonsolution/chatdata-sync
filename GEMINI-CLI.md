# ChatData Sync Gemini CLI extension

Save a garden log, find a maintenance entry, or total client payments from Gemini
CLI using your private ChatData Sync tracker. This public repository is the
extension source; the hosted service keeps your records and enforces permissions.

## Install and connect

You need two independent connections: supported Google authentication to run
Gemini's AI, and a ChatData Sync connection key to access your tracker. Your
ChatData Sync key does not authenticate you with Google. Confirm that Gemini can
answer an ordinary question before testing tracker tools.

1. Install a current [Gemini CLI](https://geminicli.com/docs/get-started/installation/)
   with extension settings and Streamable HTTP support.
2. [Sign in to ChatData Sync](https://chatdatasync.com/app), open a tracker, and
   create a named, tracker-specific connection in **Connect**. Start read-only;
   grant writes only if you want Gemini to change records.
3. Install the extension:

   ```shell
   gemini extensions install https://github.com/cgosmonsolution/chatdata-sync
   ```

4. Enter your connection key at the sensitive configuration prompt. Gemini
   documents system-keychain storage for sensitive extension settings. Do not
   paste keys into chat, command-line arguments, issues, screenshots, or files
   committed to Git.
5. Restart Gemini CLI, check `/mcp` for `chatdatasync`, and ask: "Describe my
   available tracker sections." The assistant should call `get_sync_context`.

The root [manifest](gemini-extension.json) connects directly to
`https://chatdatasync.com/api/mcp` using native Streamable HTTP and the `x-api-key`
header. No bridge, npm package installation, or build is required. The bundled
[agent guidance](GEMINI.md) covers schema discovery, confirmation, revisions,
pending approvals, accurate summaries, and untrusted record content.

Keep normal tool confirmations enabled. Tool visibility does not grant access:
the server checks the connection's active status, expiry, tracker, actions,
sections, and fields. A read-only connection must reject writes.

## Included tools

| Tool | Purpose |
| --- | --- |
| `get_sync_context` | Discover current authorized sections, fields, and guidance |
| `list_records` | Find records with exact filters |
| `get_record` | Read one record and its current revision |
| `create_record` | Save one requested entry |
| `update_record` | Apply a confirmed partial patch with its expected revision |
| `delete_record` | Delete a confirmed entry with its expected revision |
| `summarize_records` | Request structured counts/sums and preserve completeness warnings |

This conservative extension intentionally does not expose tracker creation,
layout changes, semantic search, history/recovery tools, change polling, or
attachment uploads. The full MCP service supports additional capabilities through
appropriate [host connections](https://chatdatasync.com/integrations/agents.html).
ChatGPT's file-upload parameter is not a generic Gemini file-upload contract.

## Verify your connection

- Read: "Show my tracker sections, then find my latest entries."
- Summary: "Count my entries." Check the returned canonical answer and whether
  it says the requested scope is complete.
- Write, if permitted: ask to save a disposable entry, provide required facts,
  then read the returned record back. Review-before-saving connections return a
  pending proposal rather than a successful save.
- Update/delete: read the current record, confirm the target and replacement
  values, and pass its revision. Do not delete anything without explicit confirmation.
- Permission check: with read-only access, a write must fail rather than appear saved.

The package passed native Gemini CLI installation in an isolated local profile
and checks against the application's core tool contract and live MCP protocol
initialization. A logged-in Gemini end-to-end test and Google
gallery acceptance are separate checks, not certifications claimed by this README.

## Troubleshooting and updates

- **Google sign-in fails before any tracker call:** during a November 1, 2026
  test with Gemini CLI 0.42.0, Google returned `UNSUPPORTED_CLIENT` for its
  Code Assist for individuals authentication route. The error directed the tester
  to Antigravity. This observation does not establish that every account or
  authentication method is affected, or that Antigravity accepts this extension.
  Check Google's current supported authentication options and any eligibility,
  project, or billing requirements. Do not rotate your ChatData Sync key to fix
  a Google sign-in rejection: no tracker call has occurred at that stage.
  A successful extension installation is not an authenticated end-to-end test,
  and this sign-in error is not a gallery rejection.
- **Missing or rotated key:** run `gemini extensions config chatdatasync` and
  restart. If no prompt appeared during installation, configure the key here.
- **Denied tool call:** check connection status, expiry, and permissions in
  ChatData Sync. Do not broaden them automatically.
- **Revision conflict:** reread the record and confirm the intended change again.
- **Unknown create outcome:** check existing entries before retrying to avoid duplicates.
- **Update:** run `gemini extensions update chatdatasync`, then restart.
- **Remove:** run `gemini extensions uninstall chatdatasync`. Revoke the named
  connection in ChatData Sync as well if you no longer need it.

For local extension development, clone this public repository and run
`gemini extensions link .` from its root. Do not add local settings or credentials
to Git. Keep the manifest at the repository root.

## Google discoverability and scope

Google's [official gallery requirements](https://geminicli.com/docs/extensions/releasing/)
are a public repository, a root `gemini-extension.json`, and the GitHub topic
`gemini-cli-extension`. Google documents daily discovery of qualifying repositories
and validation before listing; no issue or email submission is required.

This is a Gemini CLI integration. It does not install ChatData Sync into the
consumer Gemini website, create a Google Chat bot, or establish a Google Workspace
Marketplace listing. Those are distinct products and publishing routes.

Published by [Smarter Way to Apply](https://smarterwaytoapply.com).
Built by [Charles Anthony Gosmon](https://cgosmon.com).
Product: [ChatData Sync](https://chatdatasync.com).
Support: [support@smarterwaytoapply.com](mailto:support@smarterwaytoapply.com).
