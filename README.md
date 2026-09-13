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
- [Data 360 Query API](https://developer.salesforce.com/docs/data/data-cloud-query-guide/references/data-cloud-query-api-reference/c360a-api-queryservices-overview.html) - Developer reference for querying Data 360 data.
- [Einstein Audit and Feedback Data Model](https://developer.salesforce.com/blogs/2024/07/the-einstein-audit-and-feedback-data-model-in-data-cloud) - Supporting background on audit and feedback data. This is related context, not the same model as session tracing.

## Evals and Testing

- [Agentforce Testing Center](https://help.salesforce.com/s/articleView?id=ai.agent_testing_center.htm&type=5) - Batch testing, test scenarios, scorers, and result analysis. Salesforce recommends running agent tests in a sandbox because tests can modify CRM data.
- [Agentforce Testing Tools and Strategies](https://trailhead.salesforce.com/content/learn/modules/agentforce-testing-tools-and-strategies) - Trailhead guidance for designing an agent-testing strategy.

## Evals in CI/CD

- [Salesforce CLI Agent Plugin](https://github.com/salesforcecli/plugin-agent) - Official public command source for Agentforce development and testing, including `sf agent test run`, `sf agent test results`, and related commands.
- [Salesforce CLI Command Reference](https://developer.salesforce.com/docs/atlas.en-us.sfdx_cli_reference.meta/sfdx_cli_reference/) - General Salesforce CLI reference.
- [Salesforce DX Authorization](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_auth.htm) - Authentication patterns for automated environments.

Command behavior, flags, product availability, licenses, and supported test runners can change. Verify the current plugin documentation before adding commands to a delivery pipeline. Evals can inform a release gate; the delivery team still owns the promotion decision.

## Agent Health Alerts

- [Manage Alerts for Agent Health Monitoring](https://help.salesforce.com/s/articleView?id=ai.agent_monitor_health_alert.htm&type=5) - Official alert configuration and runtime behavior.

Alert metrics are operational signals. A threshold breach starts an investigation; it does not by itself prove hallucination, semantic drift, retrieval failure, or root cause.

## Important Notes

- Product behavior, terminology, availability, licenses, limits, and documentation can change after this page is published.
- Confirm implementation decisions against the current official documentation for your Salesforce release and environment.
- Do not interpret session traces as private model chain-of-thought.
- Testing Center and runtime scoring are related but distinct evaluation surfaces.
- Different scorers can use different labels and scales.
- Traces provide evidence, evals apply criteria, and alerts signal when investigation may be needed.

Last reviewed: September 2026.
