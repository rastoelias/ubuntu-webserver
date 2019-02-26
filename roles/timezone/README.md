
# Role: Timezone

* This role configures the timezone setting, both of the system clock and of the hardware clock.
* It is recommended to restart `crond` after changing the timezone, otherwise the jobs may run at the wrong time.

## Tasks

* Make sure `/usr/share/zoneinfo/{{ TIMEZONE }}` exists.
* Fail if `/usr/share/zoneinfo/{{ TIMEZONE }}` does not exists.
* If not fails, set timezone to `{{ TIMEZONE }}`.
* Restart `crond`.
