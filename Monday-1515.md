# Observability: the Hard Parts
## Peter Bourgon, @peterbourgon
## From Fastly, 120 engineers

### Goals
Is the system healthy?
If not why not?

- Run Prometheus
- Duplicate instrumentation that works
- Prometheus exporters
- Curate dashboards

### Rollout
- Inventory all services

The grind
- Pair up with responsible engineer
- Learn how the Prometheus model works
- Build and maintain Empathy

1. Instrument
 - Hour of pare programming
 - Mistake trying to layout process up front
 - Better: letting documentation emerge naturally
 - Documentation portal extremely helpful
2. Wire-up
 - Deploy Prometheus
 - Plumb service into Prometheus
 - Heterogeneous deployments made difficult

Code: Engineering autonomy
- Orgs must balance local vs global optimization
- Tech autonomy is a form of tech debt

Coda: Empathy
- de-learning helplessness
- understanding problems/concerns others face

### The politics of ownership
- Some services are nebulously owned
- Must have C level buy in

Tricky bits
- Empathy vs learned helplessness 
- Resistance before "production-ready"
- Socializing infrastructural knowledge 
- Alert manager

### Successful
- Team of two is a good mix
- Consulting model works, real change requires connection
- Prometheus, simple, stable and adaptable
- GitOps-style of resource management

### Questions:
1. Size of company
2. How did this project / putting people on call correspond?
 - Transition, there were already on-call engineers, could be increasing
3. How did you get engineers to maintain the systems after leaving teams?
 - Hard question: The ideal is systems should be owned. Ownership is the one or two people who wrote it. The on-call rotation could be an indicator of who should own it. Have a team who receives systems in maintenances mode, as lifecycle and they manage it and hand it back off.
4. What was the handoff process like, consulting to production.
 - Leaving an embed, on the intro email, introducing themselves and about observability story when I leave then the system belongs to you. Made clear at the beginning. Consistent communication is the key.

# Warning: This Talk Contains Content Known to the State of California to Reduce Alert Fatigue
## Aditya Mukerjee
## From Stripe

Alert Fatigue
Number of alerts train you to ignore them

Health Care Industry
72-99% of clinical alerts are false positive
Patterns of alerts contribute disproportionately to fatigue

Four steps to reducing alert fatigue: STAT
1. Supported
 - Alerting system includes people who respond to alerts, are they supported?
 - The person who responds to has the right to make the changes
2. Trustworthy
 - Consider the expected changes (model it)
 - Thresholds can be adjusted
3. Actionable
 - One decision required to respond
 - Alerts difficult to action get ignored
 - Decision tree of how to respond to alerts
 - If it's unclear who takes action, it will be ignored
4. Triaged
 - Alert type should reflect urgency
 - Urgency of alerts can change
 - Commonly understood tiers
 - Periodic re-evaluation

Don't just leverage and maximize the trust they have (grade, system analysis and outcomes)


# Monitory Report: I Have Seen Your Observability Future. You Can Choose a Better One.
## Ian Bennett, @enbnt
## From Twitter

What is twitter?
 - Every side of the conversation

Thinking of starting observability
 - What is your companies mission? 
 - If not monitoring and the likes:
   - Plan to be true to observability
   - Have Empathy
   - Get people out of the tool
   - Get used to jumping in, support, on-call

Five things that happened, challenges for the 20%
Query language (DO NOT write your own QL)
Dashboards and alerts 
Query and config
Incomparable concepts

The problem: Aggregate Monitors
- Monitor definitions are vendor lock-in
- They are directly tied to your queries
   - Simplify vocabulary
- They live longer than your time series dB
- They change infrequently

Building monitors & alerts
- Do you know what your notifications look like until you've entered an incident?
- Do you know what data your given?
- What is the added stress to our end users?
- The story here is terrible

Scope
- Limit the scope of what you plan to migrate
- Limit the scope of user interaction
- Drive for feature alignment

Evaluator project OSS, they want to share
- Adhoc evaluation API
- Flexible

[Sekhmet project](https://github.com/twitter/sekhmet)