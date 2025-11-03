# Booster Pack Layout 🚀

This is the default layout for the Booster Pack setup to enable autoloading
and environment support for ruby apps.

![Taylor Swift - Strong](https://www.trueheart78.com/assets/images/resume/taylor-strong.gif)

## Goal 🏁

When moving from _"Hey, I have a couple cool scripts"_ and expanding them into a more robust
library, a majority of what's provided should be able to dropped into said project's structure,
and ease the migration to a more fully featured app.

## Bonus 🎁

There is a default `test.yml` file in the `.github/workflows` directory that will enable GitHub's CI
system, and can easily be altered.

### But Wait, There's More... 💻

Alongside a `bin/setup`, there is a handy dandy `bin/console` that will drop you into a Pry console
with the project loaded.

## Reminder 💡

You're new friend will be `require_relative '../booster_pack'`, instead of calling a litany of
requires.

### What About Libraries Like JSON? 📚

If you need part of the Ruby standard library loaded, you will still need to `require` it. If you
want it project-wide, you can add it to the bottom of the `booster_pack.rb` file and you'll have it
wherever you need it.

## Starting Fresh 🌱

This repo is laid out so that, if you want to start a new project from it, everything should
work after you run `bundle install`.

## Copying Into A Repo

Did you break ground on a project and realized, after-the-fact, that it makes sense to kickstat it with the booster pack?

No worries!

```sh
rsync -av --exclude '.git/' --exclude 'coverage/' --exclude 'releases/' /path/to/booster_pack /path/dot/destination
```

## Creating A Release

Creating a new release is straightforward. The biggest concern is making sure to exclude
unnecessary directories.

```sh
zip -r releases/RELEASE_NAME.zip . -x ".git/*" -x "coverage/*" -x "releases/*"
```
