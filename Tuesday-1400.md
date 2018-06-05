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

When considering replacement
Ease of m,estrous discovery
Fast response time
Custom retention
Scales
Compare across dimensions
Took queries
An API

### For ops 
Prevent single node failures
Teams want to own theirs

Why Prometheus (mentioned Thanos, which runs on Prometheus)
Infrastructure now, icinga, graphite, Prometheus, 
Prometheus HA, scraping same servers with multiple Prometheus
Similar architecture, of scraping from global, the regional

How do we build it?
Terraform 
Pair HT servers
Configures route 53
Configures Cloud Watch
Configures EC2 Instance Recovery
Optional Canaries

Configs are managed in Chef
Prometheus jobs rules stored
Ruby has converse to Yaml
Lots of repeat code


# Sparky the fire dog: incident response as code
## Tapasweni Pathak