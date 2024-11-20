# Fork from Chatbot UI Legacy version.

Differences from the original:
- [x] Added **gpt-4o** model
- [x] Added model **gpt-4o-mini**
- [x] Added cross-env to change the operating port to **3030**
- [x] Added application local autostart in windows as a service via NSSM. (see win_autorun_Readme.md)

Fork was made from here:   
https://github.com/mckaywrigley/chatbot-ui/tree/legacy

## License Compliance

The original Chatbot-UI is published under the MIT license, which allows you to use, copy, modify, merge, publish, distribute, sublicense and even sell the existing code - subject to copyright.

## Why was the fork made?

This is an outdated version of the interface that is not being developed. The official repository has moved to version 2.0, which requires installation of Supabase, Docker and many more system resources. 
This version with all dependencies takes up about 874 MB, and does not require anything other than node.js. 

However, such simplicity has disadvantages. The main difference between this version and v2.0 is that it uses local browser storage to store data, and this is not the best solution for several reasons:
- Security issues
- Limited storage space
- Limits multimodal use options

I warned you.

But much easier! Let's go!

# Chatbot UI

Chatbot UI is an advanced chatbot kit for OpenAI's chat models built on top of [Chatbot UI Lite](https://github.com/mckaywrigley/chatbot-ui-lite) using Next.js, TypeScript, and Tailwind CSS.

See a [demo](https://twitter.com/mckaywrigley/status/1640380021423603713?s=46&t=AowqkodyK6B4JccSOxSPew).

![Chatbot UI](./public/screenshot.png)

## Updates

Chatbot UI will be updated over time.

Expect frequent improvements.

**Next up:**

- [ ] Delete messages
- [ ] More model settings
- [ ] Plugins

**Recent updates:**

- [x] Prompt templates (3/27/23)
- [x] Regenerate & edit responses (3/25/23)
- [x] Folders (3/24/23)
- [x] Search chat content (3/23/23)
- [x] Stop message generation (3/22/23)
- [x] Import/Export chats (3/22/23)
- [x] Custom system prompt (3/21/23)
- [x] Error handling (3/20/23)
- [x] GPT-4 support (access required) (3/20/23)
- [x] Search conversations (3/19/23)
- [x] Code syntax highlighting (3/18/23)
- [x] Toggle sidebar (3/18/23)
- [x] Conversation naming (3/18/23)
- [x] Github flavored markdown (3/18/23)
- [x] Add OpenAI API key in app (3/18/23)
- [x] Markdown support (3/17/23)

## Modifications

Modify the chat interface in `components/Chat`.

Modify the sidebar interface in `components/Sidebar`.

Modify the system prompt in `utils/index.ts`.

<!--
## Deploy

**Vercel**

Host your own live version of Chatbot UI with Vercel.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fmckaywrigley%2Fchatbot-ui)

**Replit**

Fork Chatbot UI on Replit [here](https://replit.com/@MckayWrigley/chatbot-ui-pro?v=1).

**Docker**

Build locally:

```shell
docker build -t chatgpt-ui .
docker run -e OPENAI_API_KEY=xxxxxxxx -p 3000:3000 chatgpt-ui
```

Pull from ghcr:

```
docker run -e OPENAI_API_KEY=xxxxxxxx -p 3000:3000 ghcr.io/mckaywrigley/chatbot-ui:main
```
-->

## Running Locally

**1. Clone Repo**

```bash
git clone -b legacy https://github.com/ali-adm/chatbot-ui.git chatbot-ui-legacy
```

**2. Install Dependencies**

```bash
npm i
```

**3. Provide OpenAI API Key**

Create a .env.local file in the root of the repo with your OpenAI API Key:

```bash
OPENAI_API_KEY=YOUR_KEY
```

> You can set `OPENAI_API_HOST` where access to the official OpenAI host is restricted or unavailable, allowing users to configure an alternative host for their specific needs.

> Additionally, if you have multiple OpenAI Organizations, you can set `OPENAI_ORGANIZATION` to specify one.

**4. Run App**

```bash
npm run dev
```

**5. Use It**

You should be able to start chatting.

## Configuration

When deploying the application, the following environment variables can be set:

| Environment Variable  | Default value                  | Description                                             |
| --------------------- | ------------------------------ | ------------------------------------------------------- |
| OPENAI_API_KEY        |                                | The default API key used for authentication with OpenAI |
| DEFAULT_MODEL         | `GPT-4o-mini`                | The default model to use on new conversations           |
| DEFAULT_SYSTEM_PROMPT | [see here](utils/app/const.ts) | The defaut system prompt to use on new conversations    |

If you do not provide an OpenAI API key with `OPENAI_API_KEY`, users will have to provide their own key.
If you don't have an OpenAI API key, you can get one [here](https://platform.openai.com/account/api-keys).

## Contact

As far as possible, I will implement the declared but not implemented features, and add my own new ones. You also need to configure deployment and docker. 

If you have any questions, please ask them in the **"Problems"** section, I don't think anyone will have many questions. And if there are, we will open discussions! I will be glad to communicate. Come to the light!
