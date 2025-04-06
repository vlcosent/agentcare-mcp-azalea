# Agent Care MCP Server - Azalea Health Integration

This repository contains the configuration for connecting the Agent Care MCP server to Azalea Health's Ambulatory FHIR API.

## Prerequisites

- Node.js v14 or later
- npm
- Claude Desktop (for AI interaction)

## Setup Instructions

1. Clone this repository:
   ```
   git clone https://github.com/vlcosent/agentcare-mcp-azalea.git
   cd agentcare-mcp-azalea
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Build the project:
   ```
   npm run build
   ```

4. Start the MCP server:
   - On Linux/Mac: `./start-azalea.sh`
   - On Windows: `start-azalea.bat`

## Claude Desktop Configuration

Copy the `claude_desktop_config.json` file to:
- macOS: `~/Library/Application Support/Claude/claude_desktop_config.json`
- Windows: `%APPDATA%\Claude\claude_desktop_config.json`
- Linux: `~/.config/Claude/claude_desktop_config.json`

## Testing

You can test the MCP server using the MCP inspector:

```
npm install -g @modelcontextprotocol/inspector
mcp-inspector build/index.js http://localhost:5173
```

## Azalea Health FHIR API Configuration

The server is configured to connect to Azalea Health's Ambulatory Sandbox FHIR API with the following credentials:

- Client ID: 290
- Redirect URI: http://localhost:3456/oauth/callback
- Base FHIR URL: https://app.azaleahealth.com/fhir/R4/sandbox

These credentials are for sandbox testing only and do not provide access to real patient data.