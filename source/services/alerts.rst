Alerts
~~~~~~~

How to Change Your Credit Card
==============================

To change your credit card, run

.. code-block:: bash

    gigalixir account:payment_method:set

How to see the current period's usage
=====================================

To see how many replica-size-seconds you've used so far this month, run

.. code-block:: bash

    gigalixir account:usage

The amount you see here has probably not been charged yet since we do that at the end of the month.

How to see previous invoices
============================

To see all your previous period's invoices, run

.. code-block:: bash

    gigalixir account:invoices

.. _`money back guarantee`:


=================
Lists all alerts
=================

******************
'equal-to' filters
******************

The 'equal-to' filters allow for the exact lookup of a field's value.  The value must be equal to the filter value.

Example URL w/ query params: {{host}}/api/v1/alerts?name=sprite

The following filters are supported:

* key
* message
* name
* response
* type

{{host}}/api/v1/alerts?name=sprite
String-starts-with filters
The string-type field's value must start with the filter's value.
Example URL w/ query params:
{{host}}/api/v1/alerts?resource_prefix=posit
The following filter names are supported:
key_prefix (actual field is key)
message_prefix (actual field is message)
name_prefix (actual field is name)
response_prefix (actual field is response)
type_prefix (actual field is type)

String-contains filters
The string-type field's value must contain the filter's value.  The minimum number of characters required is 4.
Example URL w/ query params:
{{host}}/api/v1/alerts?query_string_search=tion
The following filter names are supported:
key_search (actual field is key)
message_search (actual field is message)
name_search (actual field is name)
response_search (actual field is response)
type_search (actual field is type)

Order-by sorting
Order-by sorting will support a single filter. If more than one 'order-by' filter is supplied via query param, the last definition will be used.
Example URL w/ query params:
{{host}}/api/v1/alerts?order_by=asc:name
The following filters are supported:
key
message
name
response
type

The supported filtering directions are:
ValueDescriptionascascendingasc_nulls_lastascending nulls lastasc_nulls_firstascending nulls firstdescdescendingdesc_nulls_lastdescending nulls lastdesc_nulls_firstdescending nulls first
Limit filter
The limit filter sets a maximum for the number of rows in the result set and may be used for pagination.  Default limit if not set is 50.
Example URL w/ query params:
{{host}}/api/v1/alerts?limit=25
Offset filter
The offset filter skips a number of rows in the result set and may be used for pagination.
Example URL w/ query params:
{{host}}/api/v1/alerts?offset=2



