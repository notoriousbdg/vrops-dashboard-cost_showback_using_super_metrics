
# Cost Showback using Super Metrics Dashboard for vRealize Operations 7.5 and 8.0
---------

Use this [vRealize Operations](https://www.vmware.com/products/vrealize-operations.html) dashboard to show the cost of VMs on various object types.  Supported objects consist of Custom Group types of Security Zone, Service Level Objective, Function, Location, Department, and Environment; Virtual Machine folders from vSphere; vRA 8 constructs of Project, Organization, and Cloud Zone; and Applications and Application Tiers.

## Dashboard
![Dashboard](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cost_showback_using_super_metrics/master/Dashboard.png)

## Installation
1. Import the super metric at `Administration` / `Configuration` / `Super Metrics` / `Import Super Metric`  
![Import Super Metric](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cost_showback_using_super_metrics/master/Import_Super_Metric.png)
2. Click `Browse...` then select the file named [Supermetrics.json](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cost_showback_using_super_metrics/master/Supermetrics.json)
3. Edit the Policy at `Administration` / `Policies` / `Policy Library`.  The policy should be `vSphere Solution's Default Policy (DATE)` unless a new policy was explicitly created.  
![Policy Library](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cost_showback_using_super_metrics/master/Policy_Library.png)
4. Enable Super Metrics that contain with `Cost of Child VMs` in their name for Security Zone, Service Level Objective, Function, Location, Department, Environment, Virtual Machine Folder, Project, Organization, Cloud Zone, Applications and Tier object types only.  Do not enable the super metric on the row called `All Object Types`.
![Policy Metrics](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cost_showback_using_super_metrics/master/Policy_Metrics.png)
5. Import the custom groups at `Environment` / `Custom Groups` / `Gear Icon` / `Import Custom Group(s)`  
![Import Custom Groups](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cost_showback_using_super_metrics/master/Import_CustomGroup.png)
6. Click `Browse...` then select the file named [CustomGroups.json](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cost_showback_using_super_metrics/master/CustomGroups.json)
7. Import the view at `Dashboards` / `Views` / `Import...`  
![Import View](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cost_showback_using_super_metrics/master/Import_View.png)
8. Click `Browse...` then select the file named [Views.zip](https://github.com/notoriousbdg/vrops-dashboard-cost_showback_using_super_metrics/raw/master/Views.zip)
9. Import the dashboard at `Dashboards` / `Actions` / `Manage Dashboards` / `Import Dashboards`  
![Import Dashboard](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cost_showback_using_super_metrics/master/Import_Dashboard.png)
10. Click `Browse...` then select the file named [Dashboard.zip](https://github.com/notoriousbdg/vrops-dashboard-cost_showback_using_super_metrics/raw/master/Dashboard.zip)
11. The dashboard should now be available in in the dashboard list  
![Dashboard List](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cost_showback_using_super_metrics/master/Dashboard_List.png)
12. The super metrics won't show cost until the next cost calculation run.  To manually run cost calculations to validate the super metrics, click `Run` at `Administration` / `Configuration` / `Cost Settings` / `Cost Calculation Status`.

Note: Additional objects can be added to the super metrics and to each widget and view in the dashboard.

## Support

This dashboard requires vRealize Operation 7.5 or 8.0 Advanced or Enterprise edition.

Please open an [issue](https://github.com/notoriousbdg/vrops-dashboard-cost_showback_using_super_metrics/issues) for feedback.
