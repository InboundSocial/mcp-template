# MCP Template

This pack contains reusable MCP servers. It does NOT configure Doppler itself —
it only references env vars. Secrets must be provided by the project’s own Doppler config.

## Usage in a project with the Dev Template

1. Add required secrets to the project’s Doppler config:
   doppler secrets set FIRECRAWL_API_KEY=xxx
   doppler secrets set SUPABASE_URL=...
   doppler secrets set SUPABASE_KEY=...
   doppler secrets set CONTEXT7_API_KEY=xxx
   doppler secrets set DATAFORSEO_LOGIN=your_login
   doppler secrets set DATAFORSEO_PASSWORD=your_password

2. Bring this pack into the project:

   # Option A: submodule

   git submodule add https://github.com/<you>/mcp-template .cursor/mcp-pack

   # Option B: copy directly

   cp -r ../mcp-template/.cursor ./

3. Rebuild container in Cursor:
   Dev Containers: Rebuild and Reopen in Container

4. Run app with Doppler (already in Dev Template):
   npm run dev
