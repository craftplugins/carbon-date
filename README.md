<img src="./carbondate/resources/icon.svg" width="72">

# Carbon Date plugin for Craft CMS

Provides access to methods of Brian Nesbitt’s popular [Carbon date extension](https://github.com/briannesbitt/Carbon) for DateTime.

## Using Carbon Date

```jinja
{# Gets the current date/time #}
{{ 'now'|carbon }}

{# Gets the current date/time #}
{{ carbon() }}

{# Converts a date field to human relative difference (e.g. “1 year ago”) #}
{{ entry.dateField|carbon.diffForHumans }}

{# Carbon is chainable #}
{{ carbon().subMonth.subYear.toIso8601String }}

{# Carbon can also handle relative date differences #}
{% set since = '3 weeks ago'|carbon %}
{% set until = '2 weeks ago'|carbon %}
{{ since.diffForHumans(until) }}{# 1 week before #}
```
