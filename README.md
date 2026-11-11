# AI Registry — OPCoach

Vendor repository for the [AI Registry](https://github.com/eclipsefdn-ai-registry/ai-registry-core), maintained by [OPCoach](https://opcoach.ai). Contains approvals for AI artifacts published or approved by OPCoach.

## Contributing

1. Add one JSON file per approved artifact to `mcp/`, `skills/`, `plugins/`, `agents/`, or `sandbox-extensions/`. The file name is the artifact ID with `/` replaced by `--`. The central repository provides agent skills that generate these files: [MCP](https://github.com/eclipsefdn-ai-registry/ai-registry-core/blob/main/skills/create-mcp-approval/SKILL.md), [skill](https://github.com/eclipsefdn-ai-registry/ai-registry-core/blob/main/skills/create-skill-approval/SKILL.md), [plugin](https://github.com/eclipsefdn-ai-registry/ai-registry-core/blob/main/skills/create-plugin-approval/SKILL.md), and [agent](https://github.com/eclipsefdn-ai-registry/ai-registry-core/blob/main/skills/create-agent-approval/SKILL.md) approvals.
2. Validate locally:

   ```sh
   npm run validate           # standalone — clones the central repo automatically
   npm run validate:local     # fast — requires ai-registry-core checked out as a sibling
   ```

3. Open a pull request to `main`. CI runs the same validation, and a push to `main` triggers the central consolidation.

## Documentation

See the [Organization Guide](https://github.com/eclipsefdn-ai-registry/ai-registry-core#organization-guide) in the central repository for how organization repos work, how to add approvals, and how validation runs.
