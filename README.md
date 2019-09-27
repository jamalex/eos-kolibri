# eos-kolibri

Collection of Endless OS system helpers and tools for Kolibri.

# Description

This package contains eos-kolibri-system-helper: a socket-activated systemd
unit for Kolibri.

## eos-kolibri-system-helper

Provides systemd configuration to integrate the Kolibri flatpak with Endless
OS. It creates a 'kolibri' system user, and a systemd service which runs
Kolibri using the org.learningequality.Kolibri flatpak.

In addition, it enables socket activation, so the service starts automatically
when a connection is made to <http://localhost:18009>. Kolibri itself uses
CherryPy, which accepts a file descriptor from systemd.

