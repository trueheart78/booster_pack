# Booster Pack Layout

This is the default layout for the Booster Pack setup to enable autoloading
and environment support for ruby apps.

## Goal

When moving from _"Hey, I have a couple cool scripts"_ and expanding them into a more robust
library, a majority of what's provided should be able to dropped into said project's structure,
and ease the migration to a more fully featured app.

## Reminder

You're new friend will be `require_relative '../booster_pack', instead of calling a litany of
requires.

## Starting Fresh

This repo is laid how so that, if you want to start a new project from it, everything should
work after you run `bundle install`.
