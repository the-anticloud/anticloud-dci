# DCI

![license](https://img.shields.io/badge/license-MIT-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-clothing_retail-lightgrey)

> Anticloud-hardened packaging of the upstream project `DCI` in category **CLOTHING RETAIL**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** CLOTHING RETAIL · **Upstream:** https://github.com/domesticcatsoftware/DCIntrospect · **Upstream pin:** `9555122e94e0f61375e5b375b906b81d6d5b1e6e` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

DCIntrospect
============

Twitter: [@patr](http://twitter.com/patr)

Our commercial apps: [domesticcat.com.au](http://domesticcat.com.au/apps)

Introspect is small set of tools for iOS that aid in debugging user interfaces built with UIKit.  It's especially useful for UI layouts that are dynamically created or can change during runtime, or for tuning performance by finding non-opaque views or views that are re-drawing unnecessarily.  It's designed for use in the iPhone simulator, but can also be used on a device.

![Introspect Demo Image](http://domesticcat.com.au/projects/introspect/introspectdemo.png)

It uses keyboard shortcuts to handle starting, ending and other commands.  It can also be invoked via an app-wide `UIGestureRecognizer` if it is to be used on the device.

Features:
--------------
* Simple to setup and use
* Controlled via app-wide keyboard commands
* Highlighting of view frames
* Displays a views origin & size, including distances to edges of main window
* Move and resize view frames during runtime using shortcut keys
* Logging of properties of a view, including subclass properties, actions and targets (see below for an example)
* Logging of accessibility properties — useful for UI automation scripts
* Manually call setNeedsDisplay, setNeedsLayout and reloadData (for UITableView)
* Highlight all view outlines
* Highlight all views that are non-opaque
* Shows warning for views that are positioned on non-integer origins (will cause blurriness when drawn)
* Print a views hierarchy to console (via private method `recursiveDescription`) to console

Usage
-----

Add the `DCIntrospect` class files to your project, add the QuartzCore framework if needed.  To start:

    [window makeKeyAndDisplay]
    
    // always call after makeKeyAndDisplay.
    #if TARGET_IPHONE_SIMULATOR
        [[DCIntrospect sharedIntrospector] start];
    #endif

The `#if` to target the simulator is not required but is a good idea to further prevent leaving it on in production code.

Once setup, simply push the space bar to invoke the introspect or then start clicking on views to get info.  You can also tap and drag around the interface.

A a small demo app is included to test it out.

Selected keyboard shortcuts
-----------------------------------------

* Start/Stop: `spacebar`
* Help: `?`
* Print properties and actions of selected view to console: `p`
* Print accessibility properties and actions of selected view to console: `a`
* Toggle all view outlines: `o`
* Toggle highlighting non-opaque views: `O`
* Nudge view left, right, up & down: `4 6 8 2` (use the numeric pad) or `← → ↑ ↓`
* Print out the selected views' new frame to console after nudge/resize: `0`
* Print selected views recursive description to console: `v`

Logging selected views properties
-------------------------------------------------

Pushing `p` will log out the available properties about the selected view.  DCIntrospect will try to make sense of the values it can and show more useful info.  An example from a `UIButton`:

    ** UIRoundedRectButton : UIButton : UIControl : UIView : UIResponder : NSObject **
    
    ** UIView properties **
        tag: 1
        frame: {{21, 331}, {278, 37}} | bounds: {{0, 0}, {278, 37}} | center: {160, 349.5}
        transform: [1, 0, 0, 1, 0, 0]
        autoresizingMask: UIViewAutoresizingFlexibleRightMargin | UIViewAutoresizingFlexibleTopMargin
        autoresizesSubviews: YES
        contentMode: UIViewContentModeScaleToFill | contentStretch: {{0, 0}, {1, 1}} backgroundColor: nil
        alpha: 1.00 | opaque: NO | hidden: NO | clips to bounds: NO |
        clearsContextBeforeDrawing: YES
        userInteractionEnabled: YES | multipleTouchEnabled: NO
        gestureRecognizers: nil
    
    ** UIRoundedRectButton properties **
    
    ** Targets & Actions **
        target: <DCIntrospectDemoViewController: 0x4c8c0e0> action: buttonTapped:

Customizing Key Bindings
--------------------------------------

Edit the file `DCIntrospectSettings.h` to change key bindings.  You might want to change the key bindings if your using a laptop/wireless keyboard for development.

License
-----------

Made available under the MIT License.

Collaboration
-------------

If you have any feature requests/bugfixes etc. feel free to help out and send a pull request, or create a new issue.

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Unknown (no standard manifest detected)** (manifests: none detected; scanned in UPSTREAM_CLONE)
- Top-level source layout: `DCIntrospect/`, `DCIntrospectDemo/`
- Snapshot size: **24 files**, **2587 lines of code** (measured; see Benchmarks)
- Primary languages: `.h` (7), `.m` (7), `(none)` (1), `.md` (1), `.pbxproj` (1), `.pch` (1)
- Upstream commit pinned for this packaging: `9555122e94e0f61375e5b375b906b81d6d5b1e6e`

---

## Installation

* Controlled via app-wide keyboard commands
* Highlighting of view frames
* Displays a views origin & size, including distances to edges of main window
* Move and resize view frames during runtime using shortcut keys
* Logging of properties of a view, including subclass properties, actions and targets (see below for an example)
* Logging of accessibility properties — useful for UI automation scripts
* Manually call setNeedsDisplay, setNeedsLayout and reloadData (for UITableView)
* Highlight all view outlines
* Highlight all views that are non-opaque
* Shows warning for views that are positioned on non-integer origins (will cause blurriness when drawn)
* Print a views hierarchy to console (via private method `recursiveDescription`) to console

Usage
-----

Add the `DCIntrospect` class files to your project, add the QuartzCore framework if needed.  To start:

    [window makeKeyAndDisplay]
    
    // always call after makeKeyAndDisplay.
    #if TARGET_IPHONE_SIMULATOR
        [[DCIntrospect sharedIntrospector] start];
    #endif

The `#if` to target the simulator is not required but is a good idea to further prevent leaving it on in production code.

Once setup, simply push the space bar to invoke the introspect or then start clicking on views to get info.  You can also tap and drag around the interface.

A a small demo app is included to test it out.

Selected keyboard shortcuts
-----------------------------------------

* Start/Stop: `spacebar`
* Help: `?`
* Print properties and actions of selected view to console: `p`
* Print accessibility properties and actions of selected view to console: `a`
* Toggle all view outlines: `o`
* Toggle highlighting non-opaque views: `O`
* Nudge view left, right, up & down: `4 6 8 2` (use the numeric pad) or `← → ↑ ↓`
* Print out the selected views' new frame to console after nudge/resize: `0`
* Print selected views recursive description to console: `v`

Logging selected views properties
-------------------------------------------------

Pushing `p` will log out the available properties about the selected view.  DCIntrospect will try to make sense of the values it can and show more useful info.  An example from a `UIButton`:

    ** UIRoundedRectButton : UIButton : UIControl : UIView : UIResponder : NSObject **
    
    ** UIView properties **
        tag: 1
        frame: {{21, 331}, {278, 37}} | bounds: {{0, 0}, {278, 37}} | center: {160, 349.5}
        transform: [1, 0, 0, 1, 0, 0]
        autoresizingMask: UIViewAutoresizingFlexibleRightMargin | UIViewAutoresizingFlexibleTopMargin
        autoresizesSubviews: YES
        contentMode: UIViewContentModeScaleToFill | contentStretch: {{0, 0}, {1, 1}} backgroundColor: nil
        alpha: 1.00 | opaque: NO | hidden: NO | clips to bounds: NO |
        clearsContextBeforeDrawing: YES
        userInteractionEnabled: YES | multipleTouchEnabled: NO
        gestureRecognizers: nil
    
    ** UIRoundedRectButton properties **
    
    ** Targets & Actions **
        target: <DCIntrospectDemoViewController: 0x4c8c0e0> action: buttonTapped:

Customizing Key Bindings
--------------------------------------

Edit the file `DCIntrospectSettings.h` to change key bindings.  You might want to change the key bindings if your using a laptop/wireless keyboard for development.

License
-----------

Made available under the MIT License.

Collaboration
-------------

If you have any feature requests/bugfixes etc. feel free to help out and send a pull request, or create a new issue.

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

![Introspect Demo Image](http://domesticcat.com.au/projects/introspect/introspectdemo.png)

It uses keyboard shortcuts to handle starting, ending and other commands.  It can also be invoked via an app-wide `UIGestureRecognizer` if it is to be used on the device.

Features:
--------------
* Simple to setup and use
* Controlled via app-wide keyboard commands
* Highlighting of view frames
* Displays a views origin & size, including distances to edges of main window
* Move and resize view frames during runtime using shortcut keys
* Logging of properties of a view, including subclass properties, actions and targets (see below for an example)
* Logging of accessibility properties — useful for UI automation scripts
* Manually call setNeedsDisplay, setNeedsLayout and reloadData (for UITableView)
* Highlight all view outlines
* Highlight all views that are non-opaque
* Shows warning for views that are positioned on non-integer origins (will cause blurriness when drawn)
* Print a views hierarchy to console (via private method `recursiveDescription`) to console

Usage
-----

Add the `DCIntrospect` class files to your project, add the QuartzCore framework if needed.  To start:

    [window makeKeyAndDisplay]
    
    // always call after makeKeyAndDisplay.
    #if TARGET_IPHONE_SIMULATOR
        [[DCIntrospect sharedIntrospector] start];
    #endif

The `#if` to target the simulator is not required but is a good idea to further prevent leaving it on in production code.

Once setup, simply push the space bar to invoke the introspect or then start clicking on views to get info.  You can also tap and drag around the interface.

A a small demo app is included to test it out.

Selected keyboard shortcuts
-----------------------------------------

* Start/Stop: `spacebar`
* Help: `?`
* Print properties and actions of selected view to console: `p`
* Print accessibility properties and actions of selected view to console: `a`
* Toggle all view outlines: `o`
* Toggle highlighting non-opaque views: `O`
* Nudge view left, right, up & down: `4 6 8 2` (use the numeric pad) or `← → ↑ ↓`
* Print out the selected views' new frame to console after nudge/resize: `0`
* Print selected views recursive description to console: `v`

Logging selected views properties
-------------------------------------------------

Pushing `p` will log out the available properties about the selected view.  DCIntrospect will try to make sense of the values it can and show more useful info.  An example from a `UIButton`:

    ** UIRoundedRectButton : UIButton : UIControl : UIView : UIResponder : NSObject **
    
    ** UIView properties **
        tag: 1
        frame: {{21, 331}, {278, 37}} | bounds: {{0, 0}, {278, 37}} | center: {160, 349.5}
        transform: [1, 0, 0, 1, 0, 0]
        autoresizingMask: UIViewAutoresizingFlexibleRightMargin | UIViewAutoresizingFlexibleTopMargin
        autoresizesSubviews: YES
        contentMode: UIViewContentModeScaleToFill | contentStretch: {{0, 0}, {1, 1}} backgroundColor: nil
        alpha: 1.00 | opaque: NO | hidden: NO | clips to bounds: NO |
        clearsContextBeforeDrawing: YES
        userInteractionEnabled: YES | multipleTouchEnabled: NO
        gestureRecognizers: nil
    
    ** UIRoundedRectButton properties **
    
    ** Targets & Actions **
        target: <DCIntrospectDemoViewController: 0x4c8c0e0> action: buttonTapped:

Customizing Key Bindings
--------------------------------------

Edit the file `DCIntrospectSettings.h` to change key bindings.  You might want to change the key bindings if your using a laptop/wireless keyboard for development.

License
-----------

Made available under the MIT License.

Collaboration
-------------

If you have any feature requests/bugfixes etc. feel free to help out and send a pull request, or create a new issue.

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

![Introspect Demo Image](http://domesticcat.com.au/projects/introspect/introspectdemo.png)

It uses keyboard shortcuts to handle starting, ending and other commands.  It can also be invoked via an app-wide `UIGestureRecognizer` if it is to be used on the device.

Features:
--------------
* Simple to setup and use
* Controlled via app-wide keyboard commands
* Highlighting of view frames
* Displays a views origin & size, including distances to edges of main window
* Move and resize view frames during runtime using shortcut keys
* Logging of properties of a view, including subclass properties, actions and targets (see below for an example)
* Logging of accessibility properties — useful for UI automation scripts
* Manually call setNeedsDisplay, setNeedsLayout and reloadData (for UITableView)
* Highlight all view outlines
* Highlight all views that are non-opaque
* Shows warning for views that are positioned on non-integer origins (will cause blurriness when drawn)
* Print a views hierarchy to console (via private method `recursiveDescription`) to console

Usage
-----

Add the `DCIntrospect` class files to your project, add the QuartzCore framework if needed.  To start:

    [window makeKeyAndDisplay]
    
    // always call after makeKeyAndDisplay.
    #if TARGET_IPHONE_SIMULATOR
        [[DCIntrospect sharedIntrospector] start];
    #endif

The `#if` to target the simulator is not required but is a good idea to further prevent leaving it on in production code.

Once setup, simply push the space bar to invoke the introspect or then start clicking on views to get info.  You can also tap and drag around the interface.

A a small demo app is included to test it out.

Selected keyboard shortcuts
-----------------------------------------

* Start/Stop: `spacebar`
* Help: `?`
* Print properties and actions of selected view to console: `p`
* Print accessibility properties and actions of selected view to console: `a`
* Toggle all view outlines: `o`
* Toggle highlighting non-opaque views: `O`
* Nudge view left, right, up & down: `4 6 8 2` (use the numeric pad) or `← → ↑ ↓`
* Print out the selected views' new frame to console after nudge/resize: `0`
* Print selected views recursive description to console: `v`

Logging selected views properties
-------------------------------------------------

Pushing `p` will log out the available properties about the selected view.  DCIntrospect will try to make sense of the values it can and show more useful info.  An example from a `UIButton`:

    ** UIRoundedRectButton : UIButton : UIControl : UIView : UIResponder : NSObject **
    
    ** UIView properties **
        tag: 1
        frame: {{21, 331}, {278, 37}} | bounds: {{0, 0}, {278, 37}} | center: {160, 349.5}
        transform: [1, 0, 0, 1, 0, 0]
        autoresizingMask: UIViewAutoresizingFlexibleRightMargin | UIViewAutoresizingFlexibleTopMargin
        autoresizesSubviews: YES
        contentMode: UIViewContentModeScaleToFill | contentStretch: {{0, 0}, {1, 1}} backgroundColor: nil
        alpha: 1.00 | opaque: NO | hidden: NO | clips to bounds: NO |
        clearsContextBeforeDrawing: YES
        userInteractionEnabled: YES | multipleTouchEnabled: NO
        gestureRecognizers: nil
    
    ** UIRoundedRectButton properties **
    
    ** Targets & Actions **
        target: <DCIntrospectDemoViewController: 0x4c8c0e0> action: buttonTapped:

Customizing Key Bindings
--------------------------------------

Edit the file `DCIntrospectSettings.h` to change key bindings.  You might want to change the key bindings if your using a laptop/wireless keyboard for development.

License
-----------

Made available under the MIT License.

Collaboration
-------------

If you have any feature requests/bugfixes etc. feel free to help out and send a pull request, or create a new issue.

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Unknown (no standard manifest detected) |
| Manifests detected | none |
| Files in snapshot | 24 |
| Lines of code | 2587 |
| Dependency references | 0 |
| Upstream license | MIT |
| Overlay license | Anticommons 0.1.0 |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

Add the `DCIntrospect` class files to your project, add the QuartzCore framework if needed.  To start:

    [window makeKeyAndDisplay]
    
    // always call after makeKeyAndDisplay.
    #if TARGET_IPHONE_SIMULATOR
        [[DCIntrospect sharedIntrospector] start];
    #endif

The `#if` to target the simulator is not required but is a good idea to further prevent leaving it on in production code.

Once setup, simply push the space bar to invoke the introspect or then start clicking on views to get info.  You can also tap and drag around the interface.

A a small demo app is included to test it out.

Selected keyboard shortcuts
-----------------------------------------

* Start/Stop: `spacebar`
* Help: `?`
* Print properties and actions of selected view to console: `p`
* Print accessibility properties and actions of selected view to console: `a`
* Toggle all view outlines: `o`
* Toggle highlighting non-opaque views: `O`
* Nudge view left, right, up & down: `4 6 8 2` (use the numeric pad) or `← → ↑ ↓`
* Print out the selected views' new frame to console after nudge/resize: `0`
* Print selected views recursive description to console: `v`

Logging selected views properties
-------------------------------------------------

Pushing `p` will log out the available properties about the selected view.  DCIntrospect will try to make sense of the values it can and show more useful info.  An example from a `UIButton`:

    ** UIRoundedRectButton : UIButton : UIControl : UIView : UIResponder : NSObject **
    
    ** UIView properties **
        tag: 1
        frame: {{21, 331}, {278, 37}} | bounds: {{0, 0}, {278, 37}} | center: {160, 349.5}
        transform: [1, 0, 0, 1, 0, 0]
        autoresizingMask: UIViewAutoresizingFlexibleRightMargin | UIViewAutoresizingFlexibleTopMargin
        autoresizesSubviews: YES
        contentMode: UIViewContentModeScaleToFill | contentStretch: {{0, 0}, {1, 1}} backgroundColor: nil
        alpha: 1.00 | opaque: NO | hidden: NO | clips to bounds: NO |
        clearsContextBeforeDrawing: YES
        userInteractionEnabled: YES | multipleTouchEnabled: NO
        gestureRecognizers: nil
    
    ** UIRoundedRectButton properties **
    
    ** Targets & Actions **
        target: <DCIntrospectDemoViewController: 0x4c8c0e0> action: buttonTapped:

Customizing Key Bindings
--------------------------------------

Edit the file `DCIntrospectSettings.h` to change key bindings.  You might want to change the key bindings if your using a laptop/wireless keyboard for development.

License
-----------

Made available under the MIT License.

Collaboration
-------------

If you have any feature requests/bugfixes etc. feel free to help out and send a pull request, or create a new issue.

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

Upstream contributions: fork the `DCI` project, create a feature branch, and open a pull request against upstream. Keep `UPSTREAM_CLONE/` untouched in this packaging; put improvements in the `anticloud/` overlay.

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: MIT** (evidence: `LICENSE.txt` in the upstream snapshot).

License file excerpt:

```text
Copyright (C) 2011 by Patrick Richards domesticcatsoftware.com

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original MIT terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `MIT` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `DCI` (category: CLOTHING RETAIL)
- **Upstream URL:** https://github.com/domesticcatsoftware/DCIntrospect
- **Pinned commit (SHA):** `9555122e94e0f61375e5b375b906b81d6d5b1e6e`
- **Branch:** master
- **Pin provenance:** GitHub API commits/master. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`0948a1fc0d43fd28826ca70529a3b1e53acb59227d1005747f8eb7d9f55bd584`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

