# Observe Agent Behavior with Traces, Evals, and Alerts

Companion resources for the Dreamforce 2026 developer breakout **Observe Agent Behavior with Traces, Evals, and Alerts**.

This page groups the public resources behind the session's three questions:

1. **Traces:** What happened?
2. **Evals:** Was the response good according to the right criteria?
3. **Alerts:** When should an operator investigate?

## Start Here

- [Agentforce Resources](https://help.salesforce.com/s/articleView?id=ai.agent_resources.htm&type=5)
- [Design and Implement AI Agents with Agentforce](https://trailhead.salesforce.com/content/learn/trails/design-and-implement-ai-agents-with-agentforce)
- [Agentforce Developer Guide](https://developer.salesforce.com/docs/einstein/genai/overview)

## Traces and Data 360

- [Session Tracing Data Model](https://help.salesforce.com/s/articleView?id=ai.generative_ai_session_trace_data_model.htm&type=5) - Official reference for the model used to organize Agentforce session evidence.
- [Customer 360 Data Model](https://help.salesforce.com/s/articleView?id=sf.c360_a_c360datamodel.htm&type=5) - Background on Data 360 data modeling.
- [Data Model Subject Areas](https://help.salesforce.com/s/articleView?id=sf.c360_a_data_model_subject_areas.htm&type=5) - How standard Data Model Objects are organized.
- [Data 360 Query API](https://developer.salesforce.com/docs/data/data-cloud-query-guide/references/data-cloud-query-api-reference/c360a-api-query-v2-call-overview.html) - Developer reference for querying Data 360 data.
- [Einstein Audit and Feedback Data Model](https://developer.salesforce.com/blogs/2024/07/the-einstein-audit-and-feedback-data-model-in-data-cloud) - Supporting background on audit and feedback data. This is related context, not the same model as session tracing.

## Evals and Testing

- [Agentforce Testing Center](https://help.salesforce.com/s/articleView?id=ai.agent_testing_center.htm&type=5) - Batch testing, test scenarios, scorers, and result analysis. Salesforce recommends running agent tests in a sandbox because tests can modify CRM data.
- [Agentforce Testing Tools and Strategies](https://trailhead.salesforce.com/content/learn/modules/agentforce-testing-tools-and-strategies) - Trailhead guidance for designing an agent-testing strategy.
- [Agentforce Testing Center on Trailhead](https://trailhead.salesforce.com/content/learn/modules/agentforce-testing-center) - Guided learning for Testing Center.

## Evals in CI/CD

- [Salesforce CLI Agent Plugin](https://github.com/salesforcecli/plugin-agent) - Official public command source for Agentforce development and testing, including `sf agent test run`, `sf agent test results`, and related commands.
- [Salesforce CLI Command Reference](https://developer.salesforce.com/docs/atlas.en-us.sfdx_cli_reference.meta/sfdx_cli_reference/) - General Salesforce CLI reference.
- [Salesforce DX Authorization](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_auth.htm) - Authentication patterns for automated environments.

Command behavior, flags, product availability, licenses, and supported test runners can change. Verify the current plugin documentation before adding commands to a delivery pipeline. Evals can inform a release gate; the delivery team still owns the promotion decision.

## Agent Health Alerts

- [Manage Alerts for Agent Health Monitoring](https://help.salesforce.com/s/articleView?id=ai.agent_monitor_health_alert.htm&type=5) - Official alert configuration and runtime behavior.

Alert metrics are operational signals. A threshold breach starts an investigation; it does not by itself prove hallucination, semantic drift, retrieval failure, or root cause.

## Presentation Development

Gemini and NotebookLM assisted with brainstorming, organization, synthesis, and wording during presentation development. They were not treated as authoritative technical sources. Technical claims were reviewed against the public Salesforce resources above.

- [NotebookLM workspace used during deck development](https://notebook.google.com/notebook/3953e95e-c5f5-46b6-ae8f-1f43652d06bb) - This notebook contains internal/confidential sources and requires access. It is listed for provenance only and is not an attendee-accessible technical reference.
- [Gemini Apps Privacy Hub](https://support.google.com/gemini/answer/13594961)
- [NotebookLM Help](https://support.google.com/notebooklm/)

The private notebook included internal enablement material and presentation drafts. None of those source files, notebook conversations, or generated claims should be copied into this public repository unless they receive separate publication approval. Where a notebook-generated claim could not be supported by public documentation or verified product behavior, it was corrected or omitted from the final attendee resources.

## Important Notes

- Product behavior, terminology, availability, licenses, limits, and documentation can change after this page is published.
- Confirm implementation decisions against the current official documentation for your Salesforce release and environment.
- Do not interpret session traces as private model chain-of-thought.
- Testing Center and runtime scoring are related but distinct evaluation surfaces.
- Different scorers can use different labels and scales.
- Traces provide evidence, evals apply criteria, and alerts signal when investigation may be needed.

## AI-Assistance Disclosure

This resource accompanies a Dreamforce presentation and is provided for educational purposes. Gemini and NotebookLM assisted with research organization, drafting, and synthesis. The presenters reviewed the published material, but generative AI can produce incomplete or inaccurate content. AI-generated output is not an authoritative technical source. Verify technical claims, product behavior, availability, limits, security guidance, and licensing requirements against the linked official documentation before relying on or implementing them.

## Public-Release Checklist

- [ ] Open every link without an employee login.
- [ ] Confirm each page title and remove links that redirect to unavailable content.
- [ ] Recheck alert timing, metric, and notification claims against the current Help article.
- [ ] Recheck CLI commands against the current `plugin-agent` documentation.
- [ ] Add the public slide deck or recording only if event policy permits redistribution.
- [ ] Use only synthetic or explicitly approved data in screenshots and videos.
- [ ] Remove org URLs, session IDs, email addresses, credentials, internal notes, and unpublished product details.
- [ ] Add an appropriate repository license only after confirming rights to all repository content.
- [ ] Complete technical, privacy, legal/IP, accessibility, and event-policy review.

Last reviewed: September 2026.
