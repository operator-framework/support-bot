## AI chatbot for supporting operator-framework engineers, support their customers better

The [operator-framework](https://operatorframework.io) group in Openshift have been enabling the Operatorhub ecosystem since OCP 3.11. In other words, the [products](https://github.com/operator-framework) developed by the group is the underlying infrastructure that makes this possible when you launch an OCP cluster: 

![OperatorHub Screenshot](/docs/artifacts/OperatorHub.png)


As of today, there are over 400 operators in Operatorhub shipped with OCP, that are built by internal Openshift teams, ISV partners, and other Kubernetes community members. [#forum-ocp-operator-fw](https://redhat.enterprise.slack.com/archives/C3VS0LV41) in the internal Red Hat slack space is the channel that customers of Operator-Framework interact with when they need support related to the operators that are being shipped with OCP(more specifically, how they are being shipped and lifecycled on the customer clusters). This includes both other operator author teams reaching out with questions related to sdk/other tooling provided by our framework, and customer support personnel reaching out with support requests for customer clusters (eg "Customer tried upgrading Openshift Storage operator from version 1.0.0 to 1.0.1 but something broke, please advise asap"). A lot of these support requests are solved using repetitive answers. However, not all of these requests start out conversationally from the same starting point, even if the conclusions that these support requests reach can be collectively grouped to a handful of options (ie clustered to few groups). This presents an opportunity for an AI chat bot to be the first point of contact for support in the forum-ocp-operator-fw, and for an engineer from the dev team to step in only when the chat bot is unable to fulfill the support request.

This repository is a attempt to build an LLM model that can help operator-framework engineers support their customers, while maintaining velocity for feature development for the future, ie more focus time for doing the fun stuff!   