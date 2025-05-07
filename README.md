# addon-standalone-chromium

> [!CAUTION]
> This is still work in progress and things might not work as expected.
> I won't provide support, if you find an issue PRs are welcome though!

## What it does

Provides a Chromium Standalone addon to run Selenium Webdriver remotely.

Exposes port 4444 internally, so integrations that use selenium can connect remotely to it and scrape the web.

The integration needs to connect to `http://CONTAINER_NAME:4444/wd/hub`, where CONTAINER_NAME is the name of the container started within Home-Assistant.

You can also expose port 7390 for a NoVNC access, which allows you to view the selenium actions.

An integration that uses this addon is: [home-assistant-voebb](https://github.com/mrueg/home-assistant-voebb).

Builds are available for arm64 and amd64, as they depend on what selenium upstream provides.

## Work in Progress:

- Selenium Grid UI doesn't load through ingress, if you need to access it you need to expose port 4444 externally.
