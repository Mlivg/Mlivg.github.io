# Using an MCP server

## What an MCP server is, and why I trust this one

An MCP server is a program that connects an agent to an outside service in a standard way, through tools, resources and instructions. I trust datarobot.no/mcp because my course at BI names it, I read what its tools do, and it asked for no keys, files or actions beyond its purpose, but I still check its results.

## The prompt and the tool

My prompt:

> Use the datarobot MCP server. Run the Acemoglu (2024) tool for the TFP gain over ten years with the paper's inputs, then again with the share of exposed tasks raised from 0.20 to 0.30. Tell me which tool you called, what went in, what came back, and which of the paper checks did not match.

The tool my agent called: `ac_hulten`.

## The results

Inputs in both runs: 0.23 of exposed tasks profitably automated, labour cost saving 0.27, labour share 0.535, capital share 0.43, ten years.

| Run | Share of exposed tasks | Share of tasks impacted | TFP gain over ten years |
|---|---|---|---|
| The paper's inputs | 0.20 | 0.046 | 0.0066447 (0.66 percent) |
| My change | 0.30 | 0.069 | 0.00996705 (1.00 percent) |

## Why the second result follows from the first

The TFP gain is the share of tasks impacted times the overall cost saving. The cost saving is 0.27 × 0.535 = 0.14445 in both runs.

- Paper: 0.20 × 0.23 × 0.14445 = 0.0066447
- My change: 0.30 × 0.23 × 0.14445 = 0.00996705

Only the exposed share changes, and it rises by half. So the TFP gain rises by exactly half: 0.0066447 × 1.5 = 0.00996705.

## A number in the paper that does not follow

The paper prints a TFP gain of 0.66 percent over ten years and annual growth of about 0.064 percent. 0.66 divided by ten is 0.066, so the annual figure should be about 0.066 percent. The tool also flagged this row.
