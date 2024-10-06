Air Quality Dashboards
######################

The Air Quality project has both private and public dashboards. Private dashboards can only be accessed by individual users and are read-write (may be modified). Whereas public dashboards may be viewed by anyone, but are read-only (cannot be modified).

Private
*******

Private dashboards make use of the dedicated :ref:`cloud/metrics/index:Prometheus` instances that are provisioned for each DesignSpark Cloud user. When the user account is created a default private dashboard is also provisioned.

For details of how to browse dashboards, set a home dashboard, make copies and edit dashboards, see :ref:`DesignSpark Metrics documentation <cloud/metrics/index:Grafana>`.

.. warning::
   The default dashboard should not be edited, since a future updated my delete this and provision an updated dashboard. Instead the default dashboard should be copied and the copy edited. Details can be found in the aforementioned documentation. 

Public
******

Generally speaking, public dashboards will not show data from individual sensors and instead will provide statistics such as minimum, maximum and mean values. Exceptions to this include dashboards for Air Quality sub-projects, e.g. hackerspace air quality monitoring, where it may be useful to have things such as a league table with individual metrics from each shown.

*Further details will be added here when public dashboards launch*.