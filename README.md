> [!IMPORTANT]
>
> **This plugin is no longer maintained.**

# Carbon Date

A plugin for [Craft CMS](https://craftcms.com/) that provides template access to methods of Brian Nesbitt’s popular [Carbon extension](https://github.com/briannesbitt/Carbon) for date/time handling.

## Usage

```twig
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
{{ since.diffForHumans(until) }} {# Outputs “1 week before” #}
```
