# good-microservices
Best practices


- Monitoring setup
- Dashboards
- Alerting rules
- Integration tests
- Performance tests
- Failure mode handling
- Documentation of operational procedures
- Configuration management
- Resource provisioning

In this light, separate repositories make more sense because:

- Each component can have its complete operational context (monitoring, dashboards, etc.) colocated with the code
- Teams can own entire components end-to-end without cross-repo coordination
- Issues/incidents can be traced to specific components more easily
- Each component can evolve its operational practices independently
- Deployment risk is contained to one component at a time

For shared code between components, you could:

- Create a separate shared library repo for common utilities
- Use versioned packages to manage dependencies
- Or even copy critical code between repos if the components need to evolve independently

This aligns well with the "you build it, you run it" philosophy and gives each component the full attention it deserves as a distributed system.
