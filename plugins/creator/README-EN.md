# Creator

The agent that builds tools for Allkin. You tell it what you want; it asks its questions in a
**form**, writes the tool, the service or the competence to the Allkin standard, **checks** it
and debugs it with you. Creator has no page of its own: it is an agent, in the list of agents,
that you talk to.

## What it is for

- **Create a tool**: a program that runs continuously, a page, a part of Allkin's interface, a
  dedicated agent — or several at once.
- **Create a service**: teach Allkin how to reach an external API, so that your agents call it
  with your key.
- **Create a competence**: a know-how an agent loads on demand.

Everything Creator writes follows the **Allkin standard**, shipped with the tool
(`standard/PLUGIN-STANDARD.md`, `standard/SERVICE-STANDARD.md`, `standard/SKILL-STANDARD.md`),
and it checks it itself after every change.

## Getting started

1. Install Creator, then grant its three rights on its page. The **Creator** agent and your
   local repository are created at that moment.
2. Open the conversation of the Creator agent (it is in the list of agents, in pink like every
   tool's agent) and tell it what you want.
3. It asks its questions once, in a form; answer, it writes the files, checks them, and ends by
   telling you what to do: install, grant a right, reload the page, start the service.
4. To install what it wrote: **Tools** page, your "Creator" repository is one of its sources;
   **Install**, then the rights on the tool's page. A service is connected from the **Services**
   page; a competence from the **Competences** page.

## Debugging

When a tool does not do what it should, tell Creator: it reads the service's log
(`read_tool_log`), runs the check again (`check_project`), fixes, bumps the version, and tells
you what to do again. Give it the exact error you see: that is what helps it most.

## Where your files are

In the agent's working folder: `~/.allkin/plugin-data/creator/workspace/`, with a `plugins/`
folder, a `services/` folder and a `skills/` folder. That folder is a **local repository**: it
appears in the *Repositories* window of the Tools, Services and Competences pages, and your
creations are listed there with the "Creator" tag.

That folder is **not deleted** when you uninstall Creator. To publish a creation, copy its folder
into your tools repository.

## Rights asked

| Right | Why |
|-------|-----|
| Dedicated agent | The Creator agent, which writes the files. It has no access to the machine outside its working folder |
| Repository | Make the working folder a source of tools, services and competences for this Allkin |
| Network | Let the agent read the online documentation of APIs |

## If it does not work

- **The Creator agent does not appear**: a right is not granted. Open the tool's page.
- **Install changes nothing**: the version did not change. Ask Creator to raise it.
- **The tool's interface does not appear**: grant its rights on its page, then reload.
- **The agent does not answer**: check your AI provider in Allkin's Settings.
