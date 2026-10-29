# Playwright test runner + a headless JRE.
#
# The official Playwright image ships Node + browsers but no Java, so
# `allure generate` (allure-commandline is a Java tool) fails in CI with
# "JAVA_HOME is not set and no 'java' command could be found". Baking a
# headless JRE in here fixes that without an apt install on every run.
FROM mcr.microsoft.com/playwright:v1.63.0-noble

# noble = Ubuntu 24.04 (apt). default-jre-headless is enough for allure generate.
RUN apt-get update \
    && apt-get install -y --no-install-recommends default-jre-headless \
    && rm -rf /var/lib/apt/lists/* \
    && java -version
