# Rollback Steps

## Purpose

This file documents the rollback steps for the remediation actions used in the endpoint security lab.

Rollback steps are important because automated remediation should be reversible.

## Rollback 1: Unlock Linux Test User

Remediation action:

The Linux user account testuser was locked using:

sudo usermod -L testuser

Rollback command:

sudo usermod -U testuser

Verification command:

sudo passwd -S testuser

Expected result:

The user should no longer show as locked.

## Rollback 2: Remove UFW IP Block

Remediation action:

The endpoint IP address 192.168.70.10 was blocked using:

sudo ufw deny from 192.168.70.10

Rollback command:

sudo ufw delete deny from 192.168.70.10

Verification command:

sudo ufw status numbered

Expected result:

The deny rule for 192.168.70.10 should no longer be listed.

## Notes

Rollback commands should be tested before any remediation is used in production.

High-impact remediation actions should require analyst approval.

All rollback activity should be logged and reviewed.
