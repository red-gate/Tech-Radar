---
title: "Asynchronous state management in React"
ring: adopt
quadrant: techniques
tags: ["frontend","javascript","practices"]
---

Asynchronous state management in React should be delegated to a third-party framework such as [react-query](https://tanstack.com/query/v4/docs/overview). This avoids manual management of promises' states (e.g. loading/errors), and allows using suspense and error boundaries in modern React.
