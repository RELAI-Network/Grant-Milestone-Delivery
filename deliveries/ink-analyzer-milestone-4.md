# Milestone Delivery :mailbox:

**The [invoice form :pencil:](https://docs.google.com/forms/d/e/1FAIpQLSfmNYaoCgrxyhzgoKQ0ynQvnNRoTmgApz9NrMp-hd8mhIiO0A/viewform) has been filled out correctly for this milestone and the delivery is according to the official [milestone delivery guidelines](https://github.com/w3f/Grants-Program/blob/master/docs/Support%20Docs/milestone-deliverables-guidelines.md).**

* **Application Document:** [ink! Analyzer](https://github.com/w3f/Grants-Program/blob/master/applications/ink-analyzer.md)
* **Milestone Number:** 4

**Context** (optional)

This delivery is for a [Visual Studio Code Extension](https://github.com/ink-analyzer/ink-vscode) that implements all the ink! language support features provided by the [Language Server](https://github.com/ink-analyzer/ink-analyzer/tree/master/crates/lsp-server) and [Semantic Analyzer](https://github.com/ink-analyzer/ink-analyzer/tree/master/crates/analyzer) that were delivered and evaluated in
milestones 1 ([PR](https://github.com/w3f/Grant-Milestone-Delivery/pull/848), [delivery](https://github.com/w3f/Grant-Milestone-Delivery/blob/master/deliveries/ink-analyzer-milestone-1.md) and [evaluation](https://github.com/w3f/Grant-Milestone-Delivery/blob/master/evaluations/ink_analyzer_1_dsm-w3f.md)), 
2 ([PR](https://github.com/w3f/Grant-Milestone-Delivery/pull/873), [delivery](https://github.com/w3f/Grant-Milestone-Delivery/blob/master/deliveries/ink-analyzer-milestone-2.md) and [evaluation](https://github.com/w3f/Grant-Milestone-Delivery/blob/master/evaluations/ink_analyzer_2_dsm-w3f.md)) and 
3 ([PR](https://github.com/w3f/Grant-Milestone-Delivery/pull/900), [delivery](https://github.com/w3f/Grant-Milestone-Delivery/blob/master/deliveries/ink-analyzer-milestone-3.md) and [evaluation](https://github.com/dastansam/Grant-Milestone-Delivery/blob/master/evaluations/ink_analyzer_3_dastansam.md)) - 
i.e. diagnostics, completions, code/intent actions and hover content.

**Deliverables**

| Number  | Deliverable                  | Link                                                                                                                                                                                                                                                                                                                                                     | Notes                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **0a.** | License                      | [GPL-3.0](https://github.com/ink-analyzer/ink-vscode/blob/master/LICENSE).                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **0b.** | Documentation                | [Visual Studio Code Extension README](https://github.com/ink-analyzer/ink-vscode/blob/master/README.md), [Development and Testing Guide](https://github.com/ink-analyzer/ink-vscode/blob/master/DEVELOPMENT.md) on GitHub, and extensive inline source documentation in the [Github repository](https://github.com/ink-analyzer/ink-vscode/tree/master). | The VS Code Extension README is published on both [GitHub](https://github.com/ink-analyzer/ink-vscode/blob/master/README.md) and [the Visual Studio Code Marketplace](https://marketplace.visualstudio.com/items?itemName=ink-analyzer.ink-analyzer).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **0c.** | Testing and Testing Guide    | [Testing guide](https://github.com/ink-analyzer/ink-vscode/blob/master/DEVELOPMENT.md).                                                                                                                                                                                                                                                                  | Comprehensive integration tests are implemented for all the core features. Integration tests for each feature can be found in the [`src/test/suite` directory](https://github.com/ink-analyzer/ink-vscode/tree/master/src/test/suite) (i.e [diagnostics](https://github.com/ink-analyzer/ink-vscode/blob/master/src/test/suite/diagnostics.test.ts), [completions](https://github.com/ink-analyzer/ink-vscode/blob/master/src/test/suite/completions.test.ts), [code/intent actions](https://github.com/ink-analyzer/ink-vscode/blob/master/src/test/suite/actions.test.ts) and [hover content](https://github.com/ink-analyzer/ink-vscode/blob/master/src/test/suite/hover.test.ts)). Additionally, test ink! smart contracts are provided in the [`test-fixtures`](https://github.com/ink-analyzer/ink-vscode/tree/master/test-fixtures) directory as a cargo workspace that is used for both manual debugging and automated testing. Lastly, VS Code [launch configurations](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations) for debugging and automated testing are also provided as described in the [Development and Testing guide](https://github.com/ink-analyzer/ink-vscode/blob/master/DEVELOPMENT.md). |
| **0d.** | Docker                       | [Dockerfile](https://github.com/ink-analyzer/ink-vscode/blob/master/.devcontainer/devcontainer.json).                                                                                                                                                                                                                                                    | A [docker configuration](https://github.com/ink-analyzer/ink-vscode/blob/master/.devcontainer/devcontainer.json) is provided in the form of a [Dev Container](https://code.visualstudio.com/docs/devcontainers/containers) which can be used for container-based development and testing in an isolated environment. See the [Development and Testing guide](https://github.com/ink-analyzer/ink-vscode/blob/master/DEVELOPMENT.md) for details.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **0e.** | Article                      | [Article](https://analyze.ink/blog/introducing-ink-analyzer).                                                                                                                                                                                                                                                                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 1.      | Visual Studio Code Extension | [GitHub repository](https://github.com/ink-analyzer/ink-vscode).                                                                                                                                                                                                                                                                                         | The extension is also available in the [Visual Studio Code Marketplace](https://marketplace.visualstudio.com/items?itemName=ink-analyzer.ink-analyzer), additionally [VSIX packages](https://code.visualstudio.com/api/working-with-extensions/publishing-extension#packaging-extensions) can be downloaded directly from the [releases page of the GitHub repo](https://github.com/ink-analyzer/ink-vscode/releases).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |


**Additional Information**

Please use the [master branch](https://github.com/ink-analyzer/ink-vscode/tree/master) for testing, another branch will be used for continued work until the completion of the review.