# Multi-Select-Picklist-Lightning

A Lightning component to allow multi selection from a drop down with tons unique feature. Please take a note of few things on how you can make the most out of this component:

General syntax to use:
<code><c:MultiSelect msoptions="{!v.options}" /></code>

The one and only required attribute is "<b>msoptions</b>" which accept a list or javascript array of object. Each object must have a two parameters:
* Id - Id of option. Always try to keep this value unique as it helps in finding out selection uniquely.
* Name - Label of option. This value renderes in the pick list field.

<h3>Other optional attributes:</h3>

* mslabel - Label to be shown on top of multi picklist field. If you don't supply a value, the label will not be shown.
* maxSelectedShow - It accepst a number. Show the selected item names. If selection count increases, it display the count of selection instead of selectio names. Dafault is 2.
* showFilterInput - Boolean attribute, if set to true, a text box will be displayed within picklist field to search through values. Default is true.
* showRefreshButton - Boolean attribute, if set to true, display a refresh button to clear the picklist selection and rebuild the picklist. Default is true.
* showClearButton - Boolean attribute, if set to true, display a clear button to clear text box value.
* msname - String attribute to display default value in picklist before selection. Default is "Select a value"


<h3>Get selected options</h3>
To get all selected options, assign an aura:id to multiselect picklist component and access the value of attribute <b>selectedOptions</b>:

<code><c:MultiSelect aura:id="jobLocationMS" mslabel="Job Location" msoptions="{!v.options}" /></code>

In JavaScript Controller:

<code>const selectedOptions = component.find("jobLocationMS").get("v.selectedOptions");//this will return an array of selected elements</code>
  
