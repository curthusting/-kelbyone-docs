# KelbyOne Components Library

#### Description

The KelbyOne Components Library is comprised of multiple "layers" that interact with each other to provide a seemless UX/UI throughout all of their implementing [Applications](/external-Applications.html).

## Structure

There is a very specific way that each layer comunicates with the others in order to accomplish this.

###### [Applications](/external-Applications.html) -> [Views](/module-Views.html) | [Partials](/module-Partials.html) <-> [Providers](/Providers.html) <-> [Services](/Services.html) <-> Database

## Overview

There following is a list of the "layers" separated by their function as well as a brief description of their purpose.

### UX/UI

---

#### [Application](/external-Applications.html)

- Any user facing KelbyOne website, app, etc that implements the [`KelbyOne Components Library`](/index.html).
- Implements a combination of pre-defined [`Views`](/module-Views.html) to build out the page structure within the given [`Applications`](/external-Applications.html) framework.

#### [Views](/module-Views.html)

- A collection highly configurable yet reusable templates that take a configuration object that determines what information to display.
- Consist of a combination of pre-defined [`Partials`](/module-Partials.html) to build out the layout.
- Interact directly with the [`Providers`](/Providers.html) to convert the provided `Configuration` into _Readable and Styled DOM elemnts_.

#### [Partials](/module-Partials.html)

- The lowest-level DOM structure implemented by [`Views`](/module-Views.html)

### JS

---

#### [Providers](/Providers.html)

- Receives information from the implementing [`Views`](/module-Views.html) via `Config` for initial setup.
- Mainly comprised of Event Listeners that are triggered by the implementing [`Views`](/module-Views.html) | [`Components`](/Components.html).
  - Once an event is triggered, it implements the required method(s) in [`Services`](/Services.html) to update the [`Store`](/Store.html).
    - On response from the [`Services`](/Services.html) it fires events which the [`Views`](/module-Views.html) | [`Components`](/Components.html) are subscribed to in order to update the DOM.

[View Docs](/Providers.html)

#### [Services](/Services.html)

KelbyOne Services JS
[View Docs](/Services.html)

---

#### [Core](/Core.html)

KelbyOne Core JS
[View Docs](/Core.html)

#### [Store](/Store.html)

KelbyOne Store JS
[View Docs](/Store.html)
