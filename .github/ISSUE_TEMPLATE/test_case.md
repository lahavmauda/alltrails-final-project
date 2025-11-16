name: Test case
description: Propose or document a test case
title: "[TC] Feature - short name"
labels: test-case
body:
  - type: input
    attributes:
      label: ID
      placeholder: TC-001
  - type: textarea
    attributes:
      label: Preconditions
      placeholder: System state or data setup before running this test
  - type: textarea
    attributes:
      label: Steps
      placeholder: 1. Open page ...  2. Click button ...  3. Observe result ...
  - type: textarea
    attributes:
      label: Expected Result
      placeholder: What should happen when the steps are followed
  - type: dropdown
    attributes:
      label: Priority
      options: [P1, P2, P3]
