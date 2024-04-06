# Observability

Observability, a term that extends beyond the confines of traditional monitoring, offers a holistic view into the behavior of complex systems, particularly in the dynamic and distributed nature of cloud-native environments. It's a concept borrowed from control theory, which helps understand how systems can be manipulated based on their external outputs.

## Observability vs. Monitoring

- **Monitoring:** Focuses on tracking predefined metrics and logs to identify known issues within a system. It's about keeping an eye on the system's health and performance through specific indicators.
- **Observability:** Encompasses monitoring but goes further by enabling the exploration of unknowns within the system. It provides the tools and practices necessary to ask arbitrary questions about your system's state and behavior, without needing to know upfront what you might be looking for.

## The Essence of Observability

The principle of observability in IT and cloud-native systems can be likened to the cruise control in cars: it's about setting a desired state (e.g., speed or system utilization) and making adjustments based on real-time feedback to maintain or achieve that state, such as scaling resources in response to load changes.

### Key Questions Observability Aims to Answer

1. **Stability:** Is the system stable under manipulation, or does it exhibit unexpected behaviors?
2. **Sensitivity:** How does the system react to changes, such as increased latency in services?
3. **Limits:** Are any operational metrics exceeding predefined thresholds?
4. **Failures:** What causes requests to the system to fail?
5. **Bottlenecks:** Where are the system's performance bottlenecks?

## The Higher Goal of Observability

The ultimate purpose of observability is to enable a deep analysis of data collected from various parts of the system. This insight allows for:

- **A Better Understanding:** Gaining a comprehensive view of how the system operates under different conditions.
- **Proactive Response:** Quickly identifying and rectifying error states or performance issues before they impact the end users.
- **Continuous Improvement:** Leveraging feedback loops akin to those in agile software development to continually adapt and enhance the system based on real-world performance and user interactions.
