# FYP Project Roadmap

## What the folder currently contains

- `AI-Powered Desktop Task Assistant.md`: the initial concept and a list of undecided choices.
- `FYP Proposal - Desktop AI Assistant.pdf`: a nine-page proposal draft with the problem, objectives, proposed architecture, modules, scope, and evaluation idea already outlined.

The proposal is a useful starting draft, but it is not submission-ready yet: team and supervisor details/date are placeholders; the application and tasks are not fixed; the validation method and experiment are not operationally defined; the appendices' diagrams are missing; and the references are preliminary. The concept also includes many product features that may crowd out the research contribution.

## Recommended project focus

Keep the research question at the center:

> For a small, predefined set of tasks in one supported application, does validating extracted task information before AI analysis improve the correctness and usefulness of assistant suggestions compared with sending unvalidated screen-derived information?

Start with **one application and one task family**. A practical first candidate is VS Code with a language/toolchain the team already knows, using static analysis (compiler or linter diagnostics) as the validation signal. Confirm this with the supervisor before locking it. Expand to a second task or application only if the first experiment and core workflow are working early enough.

For a fair research comparison, define two conditions over the same scenarios: (A) AI receives screen-derived context without the proposed validation gate; (B) AI receives the context only when it passes the defined application-specific checks, with an explicit abstain outcome otherwise. Use the same model, prompt policy, scenario inputs, and scoring rubric in both conditions. Save the inputs and outputs so results can be checked.

## Work sequence and deliverables

| Stage | Work | Concrete deliverable / exit condition |
|---|---|---|
| 1. Confirm constraints (immediately) | Obtain department proposal/report template, submission dates, required diagrams, evaluation expectations, team roles, supervisor preferences, and available hardware/API budget. | A one-page constraints sheet and agreed scope. |
| 2. Freeze the research scope | Choose one application, one task family, supported input, what counts as an error, and what the system will never do. Draft the research question, objectives, and exclusions. | Supervisor-approved scope; no unresolved core feature choices. |
| 3. Literature review and gap | Search and read primary papers and official technical documentation on GUI/screen agents, task understanding, static analysis, grounding/validation, abstention, and evaluation. Record each source's method, findings, limitations, and relevance. Verify every citation. | Literature matrix, synthesized gap, and reference list; claims in the proposal supported by sources. |
| 4. Finalize proposal | Revise title, introduction/problem, research question, objectives, related work, method, feasibility, scope, risks, timeline, and references. Add system/block and use-case diagrams if required. Replace all placeholders and align with department format. | Complete proposal submitted and supervisor feedback recorded. |
| 5. Specify experiment before building | Define scenarios and ground truth, the two comparison conditions, success criteria, rating rubric, metrics, number of repeated runs, data handling, and how abstentions are scored. Pilot a few cases. | Evaluation protocol and frozen scenario set that can be run repeatedly. |
| 6. Design and technical spike | Sketch architecture and data flow; verify selected-window capture, extraction, app/task identification, validation, and AI call with a tiny prototype. Decide whether app APIs/accessibility data or OCR are feasible before committing. | Architecture diagram, threat/privacy notes, and a working feasibility spike. |
| 7. Build the minimum research prototype | Implement user-controlled start/stop and selected-window monitoring; extraction; deterministic validator; AI comparison path; suggestion/abstain output; event logging for evaluation. Keep manual review and user confirmation. | End-to-end vertical slice for the chosen task; no unvalidated autonomous action. |
| 8. Test and refine | Check functional cases, edge cases, unsupported windows, poor OCR/extraction, validator failures, low-confidence/abstain behavior, latency, and API failures. Fix issues that affect the experiment and document limitations. | Stable release candidate and test record. |
| 9. Run evaluation | Run the predefined scenarios under both conditions. Blind or independently review outputs where possible. Compute precision, recall, F1, false positive/negative rates, abstention coverage, and response time as appropriate. Preserve raw results. | Reproducible results table/plots and analysis answering the research question. |
| 10. Write report and prepare defense | Write methodology before results; then results, discussion, threats to validity, limitations, conclusion, and future work. Include architecture, use cases, experiment materials, and user guide. Rehearse a demo that works offline or has a fallback recording. | Final report, reproducible demo, slides, and defense Q&A notes. |

## Scope guardrails

### Core (must work)

- One user-selected supported application and narrowly defined task family.
- Explicit monitoring controls and clear indication of what is being captured.
- Application/task recognition and relevant information extraction.
- A documented, testable validation mechanism and an abstain path.
- AI explanation/suggestion and a comparison against the unvalidated condition.
- Scenario-based evaluation with preserved ground truth and outputs.

### Defer until the research prototype is sound

Multiple Office apps, broad cross-application support, selectable animated avatars, account recovery, multi-user memory, recurring reminders, playful mode, voice, calendar, and additional personalities. A basic interface is enough to demonstrate the research. If any supporting feature is required by the supervisor, schedule it only after the core experiment is viable.

### Keep out of scope

Autonomous keyboard/mouse control, automatic editing of user files, monitoring unselected windows, and training a new foundation model.

## Immediate next steps

1. Ask the supervisor to approve the proposed research question and one-application scope.
2. Get the department's proposal template, rubric, submission date, and required methodology/evaluation details.
3. Agree on the target task and validation signal. For a code task, a compiler/linter diagnostic is a stronger, measurable starting point than vague visual “mistake detection.”
4. Make a literature matrix and replace the current proposal's broad, currently unsupported gap claim with a gap grounded in verified studies.
5. Define the baseline and validation conditions and draft a small scenario set before developing the full app.
6. Revise and submit the proposal, then prototype the highest-risk technical step (capturing and reliably extracting task context from the selected window).

## Planning cadence

Use the university's actual milestones rather than treating the stages above as fixed calendar dates. At each weekly supervisor meeting, bring: completed work linked to a deliverable, evidence/demo, blockers, decisions needed, and the next week's target. Keep a decision log and update this roadmap when scope or dates change.

## Decisions to record

- Approved final title and research question.
- Target application, language/toolchain, and exact task family.
- What information can be captured, where it is processed, retention/deletion policy, and consent/privacy requirements.
- Validator rules, confidence/abstention rule, and unsupported-case behavior.
- AI provider/model, API cost limit, key storage, and failure behavior.
- Baseline comparison, scenario count, ground truth, rating procedure, metrics, and repeatability plan.
- Required features versus stretch features, owner per module, and department deadlines.
