# How to better use claude code?  ([中文版本](readme-zh.md))
prompt should clear , detailed
through the lession not only should we learn,but also work

## explain
if the current context is over,plz turn off and start another new context
MCP server - add as needed ,do not overdo it
CLAUDE.md - keep it clean , only put the necessary information, you can also put your rules of project in there

## location
put your folder of .claude in the root dir of project dir
if you put folder of .claude
if not in the root of project ,you can put .claude in the ~/.claude ,that has  global scope

## CLAUDE.md
-say what does this project work?
-technical stack
-variable name,style of code
-rules and banned

## commands
type less words to do more job
/review   --   "check out the commit quality of code,and gave feedback,if has bug then fix it" 
only one command to replace template of prompt
.claude/commands/command_name.md

## mcp server
if function calling let llm could use local function
then mcp server let llm could use local server through model context protocol
like the playwright server , llm -> mcp context protocol(expose the server) -> local mcp server ->llm control browser
```
claude mcp add playwright -- npx @playwright/mcp@latest
claude mcp add github -e GITHUB_PERSONAL_ACCESS_TOKEN=token -- npx -y @modelcontextprotocol/server-github
```

## skills
natural language to execute standard operation process



