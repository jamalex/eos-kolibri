# eos-kolibri

Collection of Endless OS system helpers and tools for Kolibri.

# Description

This package contains eos-kolibri-system-helper: a socket-activated systemd
unit for Kolibri.

## eos-kolibri-system-helper

Provides systemd configuration to integrate the Kolibri flatpak with Endless
OS. It creates a 'kolibri' system user, and a systemd service file which runs
Kolibri as a system service using the org.learningequality.Kolibri flatpak. In
addition, it adds socket activation so the service starts automatically when a
user navigates to <http://localhost:18009> in a web browser.

