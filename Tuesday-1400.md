# Slack in the Age of Prometheus
## By George Luong
## From Slack

### Graphite
- Metrics were difficult to understand
- User experience, standpoint (slow)
- No tags/label (at that point)
- Team of 6
- Couldn't scale Graphite, they used a hash ring and to extend, would require time/challenge
- Suseptible to developers taking down system

### When considering replacement
- Ease of metrics discovery
- Fast response time
- Custom retention
- Scales
- Compare across dimensions
- Took queries
- An API

### For ops 
- Prevent single node failures
- Teams want to own theirs

### Why Prometheus (mentioned Thanos, which runs on Prometheus)
- Infrastructure now, icinga, graphite, Prometheus, 
- Prometheus HA, scraping same servers with multiple Prometheus
- Similar architecture, of scraping from global, the regional

### How do we build it?
- Terraform 
- Pair HT servers
- Configures route 53
- Configures Cloud Watch
- Configures EC2 Instance Recovery
- Optional Canaries

### Configs are managed in Chef
- Prometheus jobs rules stored
- Ruby has converse to Yaml
- Lots of repeat code

### Metrics to Grafana from StatsD
- They used a variation of StatsD, but then get the raw data also (not aggregated)

### Challenges
- Communication across time and space is difficult (empathize)
- For new projects, momentum
- Demonstrate value early and often\


# Sparky the fire dog: incident response as code
## Tapasweni Pathak

### Components
- AWS
- PagerDuty

### When setting up service monitoring
- Define (why was triggered)
- What it means Root: cause _ contributing factors, how they were determined
- What to do about it: Why the incident was resolved
- Things to check which may be related: Useful Cloudwatch graphs/sumo logic queries
- Tracking: ticket number related to resolution

Can we reduce the dependency on people?
     