<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/128535272/15.2.5%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/T355128)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
<!-- default badges end -->
<!-- default file list -->
*Files to look at*:

* [Default.aspx](./CS/Default.aspx) (VB: [Default.aspx](./VB/Default.aspx))
* [Default.aspx.cs](./CS/Default.aspx.cs) (VB: [Default.aspx.vb](./VB/Default.aspx.vb))
<!-- default file list end -->
# ASPxGridView - How to save selected rows to the database by using WebMethods


<p>This example shows how to save and retrieve selection state of the row. It is realized by using <a href="https://msdn.microsoft.com/en-us/library/byxd99hx(v=vs.90).aspx">WebMethods</a>. On page loading, selection state is retrieved from the database and <a href="https://documentation.devexpress.com/#AspNet/clsDevExpressWebASPxGridViewtopic">ASPxGridView</a> rows are selected by the <a href="https://documentation.devexpress.com/#AspNet/DevExpressWebDataWebDataSelection_SetSelectiontopic">SetSelection</a> method. When a row is selected, the client-side <a href="https://documentation.devexpress.com/#AspNet/DevExpressWebScriptsASPxClientGridView_SelectionChangedtopic">ASPxClientGridView.SelectionChanged</a> event is raised and the <strong>UpdateDB</strong> method is called. This method updates a database.<br>On the client side, <strong>WebMethod</strong> is called by</p>


```js
PageMethods.UpdateDB(array);
```


<p>On the server side, <a href="https://msdn.microsoft.com/en-us/library/bb398863.aspx">ScriptManager</a> is used with <a href="https://msdn.microsoft.com/en-us/library/system.web.ui.scriptmanager.enablepagemethods.aspx">EnablePageMethods</a> set in "True".</p>


```aspx
<asp:ScriptManager ID="ScriptManager1" runat="server" EnablePageMethods="true"></asp:ScriptManager>
```


<p>and the C# method is marked by <a href="https://msdn.microsoft.com/en-us/library/system.web.services.webmethodattribute.aspx">WebMethodAttribute</a> </p>


```cs
using System.Web.Services;
 [WebMethod]
public static void UpdateDB(object[] array) {
//method code
}
```


<p> </p>
<p><strong>See also</strong>:<br><a href="https://www.devexpress.com/Support/Center/p/T355127">ASPxGridView - How to save selected rows to the database when ProcessSelectionChangedOnServer is True</a><br><a href="https://www.devexpress.com/Support/Center/p/T156786">How to track progress of server side processing on the client side (using WebMethods)</a></p>

<br/>


