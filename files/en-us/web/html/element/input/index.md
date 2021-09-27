---
title: '<input>: The Input (Form Input) element'
slug: Web/HTML/Element/input
tags:
  - Data entry
  - Element
  - Forms
  - HTML
  - HTML forms
  - HTML input tag
  - Input
  - MakeBrowserAgnostic
  - Reference
  - Web
browser-compat: html.elements.input
---
<div>{{HTMLRef}}</div>

<p>The <strong><code>&lt;input&gt;</code></strong> <a href="/en-US/docs/Web/HTML">HTML</a> element is used to create interactive controls for web-based forms in order to accept data from the user; a wide variety of types of input data and control widgets are available, depending on the device and {{Glossary("user agent")}}. The <code>&lt;input&gt;</code> element is one of the most powerful and complex in all of HTML due to the sheer number of combinations of input types and attributes.</p>

<div>{{EmbedInteractiveExample("pages/tabbed/input-text.html", "tabbed-shorter")}}</div>

<h2 id="input_types">&lt;input&gt; types</h2>

<p>How an <code>&lt;input&gt;</code> works varies considerably depending on the value of its {{htmlattrxref("type", "input")}} attribute, hence the different types are covered in their own separate reference pages. If this attribute is not specified, the default type adopted is <code>text</code>.</p>

<p>The available types are as follows:</p>

<table class="no-markdown">
 <colgroup>
  <col>
  <col style="width: 50%;">
  <col>
 </colgroup>
 <thead>
  <tr>
   <th>Type</th>
   <th>Description</th>
   <th>Basic Examples</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{HTMLElement("input/button", "button")}}</td>
   <td>A push button with no default behavior displaying the value of the {{anch('attr-value', 'value')}} attribute, empty by default.</td>
   <td id="examplebutton">
    <pre class="brush: html hidden">
&lt;input  type="button" name="button" value="Button" /&gt;</pre>
    {{EmbedLiveSample("examplebutton",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/checkbox", "checkbox")}}</td>
   <td>A check box allowing single values to be selected/deselected.</td>
   <td id="examplecheckbox">
    <pre class="brush: html hidden">
&lt;input  type="checkbox" name="checkbox"/&gt;</pre>
    {{EmbedLiveSample("examplecheckbox",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/color", "color")}}</td>
   <td>A control for specifying a color; opening a color picker when active in supporting browsers.</td>
   <td id="examplecolor">
    <pre class="brush: html hidden">
&lt;input  type="color" name="color"/&gt;</pre>
    {{EmbedLiveSample("examplecolor",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/date", "date")}}</td>
   <td>A control for entering a date (year, month, and day, with no time). Opens a date picker or numeric wheels for year, month, day when active in supporting browsers.</td>
   <td id="exampledate">
    <pre class="brush: html hidden">
&lt;input  type="date" name="date"/&gt;</pre>
    {{EmbedLiveSample("exampledate",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/datetime-local", "datetime-local")}}</td>
   <td>A control for entering a date and time, with no time zone. Opens a date picker or numeric wheels for date- and time-components when active in supporting browsers.</td>
   <td id="exampledtl">
    <pre class="brush: html hidden">
&lt;input  type="datetime-local" name="datetime-local"/&gt;</pre>
    {{EmbedLiveSample("exampledtl",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/email", "email")}}</td>
   <td>A field for editing an email address. Looks like a <code>text</code> input, but has validation parameters and relevant keyboard in supporting browsers and devices with dynamic keyboards.</td>
   <td id="exampleemail">
    <pre class="brush: html hidden">
&lt;input type="email" name="email"/&gt;</pre>
    {{EmbedLiveSample("exampleemail",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/file", "file")}}</td>
   <td>A control that lets the user select a file. Use the {{anch('attr-accept', 'accept')}} attribute to define the types of files that the control can select.</td>
   <td id="examplefile">
    <pre class="brush: html hidden">
&lt;input type="file" accept="image/*, text/*" name="file"/&gt;</pre>
    {{EmbedLiveSample("examplefile",'100%',55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/hidden", "hidden")}}</td>
   <td>A control that is not displayed but whose value is submitted to the server. There is an example in the next column, but it's hidden!</td>
   <td id="examplehidden">
    <pre class="brush: html hidden">
&lt;input id="userId" name="userId" type="hidden" value="abc123"&gt;</pre>
    {{EmbedLiveSample("examplehidden",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/image", "image")}}</td>
   <td>A graphical <code>submit</code> button. Displays an image defined by the <code>src</code> attribute. The {{anch('attr-alt', 'alt')}} attribute displays if the image {{anch('attr-src', 'src')}} is missing.</td>
   <td id="exampleimage">
    <pre class="brush: html hidden">
&lt;input type="image" name="image" src="" alt="image input"/&gt;</pre>
    {{EmbedLiveSample("exampleimage",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/month", "month")}}</td>
   <td>A control for entering a month and year, with no time zone.</td>
   <td id="examplemonth">
    <pre class="brush: html hidden">
&lt;input type="month" name="month"/&gt;</pre>
    {{EmbedLiveSample("examplemonth",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/number", "number")}}</td>
   <td>A control for entering a number. Displays a spinner and adds default validation when supported. Displays a numeric keypad in some devices with dynamic keypads.</td>
   <td id="examplenumber">
    <pre class="brush: html hidden">
&lt;input  type="number" name="number"/&gt;</pre>
    {{EmbedLiveSample("examplenumber",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/password", "password")}}</td>
   <td>A single-line text field whose value is obscured. Will alert user if site is not secure.</td>
   <td id="examplepassword">
    <pre class="brush: html hidden">
&lt;input  type="password" name="password"/&gt;</pre>
    {{EmbedLiveSample("examplepassword",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/radio", "radio")}}</td>
   <td>A radio button, allowing a single value to be selected out of multiple choices with the same {{anch('attr-name', 'name')}} value.</td>
   <td id="exampleradio">
    <pre class="brush: html hidden">
&lt;input type="radio" name="radio"/&gt;</pre>
    {{EmbedLiveSample("exampleradio",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/range", "range")}}</td>
   <td>A control for entering a number whose exact value is not important. Displays as a range widget defaulting to the middle value. Used in conjunction {{anch('attr-min', 'min')}} and {{anch('attr-max', 'max')}} to define the range of acceptable values.</td>
   <td id="examplerange">
    <pre class="brush: html hidden">
&lt;input type="range" name="range" min="0" max="25"/&gt;</pre>
    {{EmbedLiveSample("examplerange",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/reset", "reset")}}</td>
   <td>A button that resets the contents of the form to default values. Not recommended.</td>
   <td id="examplereset">
    <pre class="brush: html hidden">
&lt;input  type="reset" name="reset"/&gt;</pre>
    {{EmbedLiveSample("examplereset",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/search", "search")}}</td>
   <td>A single-line text field for entering search strings. Line-breaks are automatically removed from the input value. May include a delete icon in supporting browsers that can be used to clear the field. Displays a search icon instead of enter key on some devices with dynamic keypads.</td>
   <td id="examplesearch">
    <pre class="brush: html hidden">
&lt;input  type="search" name="search"/&gt;</pre>
    {{EmbedLiveSample("examplesearch",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/submit", "submit")}}</td>
   <td>A button that submits the form.</td>
   <td id="examplesubmit">
    <pre class="brush: html hidden">
&lt;input type="submit" name="submit"/&gt;</pre>
    {{EmbedLiveSample("examplesubmit",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/tel", "tel")}}</td>
   <td>A control for entering a telephone number. Displays a telephone keypad in some devices with dynamic keypads.</td>
   <td id="exampletel">
    <pre class="brush: html hidden">
&lt;input  type="tel" name="tel"/&gt;</pre>
    {{EmbedLiveSample("exampletel",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/text", "text")}}</td>
   <td>The default value. A single-line text field. Line-breaks are automatically removed from the input value.</td>
   <td id="exampletext">
    <pre class="brush: html hidden">
&lt;input type="text" name="text"/&gt;</pre>
    {{EmbedLiveSample("exampletext",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/time", "time")}}</td>
   <td>A control for entering a time value with no time zone.</td>
   <td id="exampletime">
    <pre class="brush: html hidden">
&lt;input  type="time" name="time"/&gt;</pre>
    {{EmbedLiveSample("exampletime",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/url", "url")}}</td>
   <td>A field for entering a URL. Looks like a <code>text</code> input, but has validation parameters and relevant keyboard in supporting browsers and devices with dynamic keyboards.</td>
   <td id="exampleurl">
    <pre class="brush: html hidden">
&lt;input type="url" name="url"/&gt;</pre>
    {{EmbedLiveSample("exampleurl",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <td>{{HTMLElement("input/week", "week")}}</td>
   <td>A control for entering a date consisting of a week-year number and a week number with no time zone.</td>
   <td id="exampleweek">
    <pre class="brush: html hidden">
&lt;input type="week" name="week"/&gt;</pre>
    {{EmbedLiveSample("exampleweek",200,55,"","", "nobutton")}}</td>
  </tr>
  <tr>
   <th colspan="3">Obsolete values</th>
  </tr>
  <tr>
   <td>{{HTMLElement("input/datetime", "datetime")}}</td>
   <td>{{deprecated_inline}} A control for entering a date and time (hour, minute, second, and fraction of a second) based on UTC time zone.</td>
   <td id="exampledatetime">
    <pre class="brush: html hidden">
&lt;input type="datetime" name="datetime"/&gt;</pre>
    {{EmbedLiveSample("exampledatetime",200,75,"","", "nobutton")}}</td>
  </tr>
 </tbody>
</table>

<h2 id="Attributes">Attributes</h2>

<p>The <code>&lt;input&gt;</code> element is so powerful because of its attributes; the {{htmlattrxref("type", "input")}} attribute, described with examples above, being the most important. Since every <code>&lt;input&gt;</code> element, regardless of type, is based on the {{domxref("HTMLInputElement")}} interface, they technically share the exact same set of attributes. However, in reality, most attributes have an effect on only a specific subset of input types. In addition, the way some attributes impact an input depends on the input type, impacting different input types in different ways.</p>

<p>This section provides a table listing all the attributes with a brief description. This table is followed by a list describing each attribute in greater detail, along with which input types they are associated with. Those that are common to most or all input types are defined in greater detail below. Attributes that are unique to particular input types—or attributes which are common to all input types but have special behaviors when used on a given input type—are instead documented on those types' pages. This element includes the <a href="/en-US/docs/Web/HTML/Global_attributes">global attributes</a>. Those with extra importance as it relates to <code>&lt;input&gt;</code> are highlighted.</p>

<table class="no-markdown">
 <caption>Attributes for the <code>&lt;input&gt;</code> element include <a href="/en-US/docs/Web/HTML/Global_attributes">global HTML attributes</a> and:</caption>
 <thead>
  <tr>
   <th scope="col">Attribute</th>
   <th scope="col">Type or Types</th>
   <th scope="col">Description</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{htmlattrxref("accept", "input", "", 1)}}</td>
   <td>file</td>
   <td>Hint for expected file type in file upload controls</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("alt", "input", "", 1)}}</td>
   <td>image</td>
   <td>alt attribute for the image type. Required for accessibility</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("autocomplete", "input", "", 1)}}</td>
   <td>all</td>
   <td>Hint for form autofill feature</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("autofocus", "input", "", 1)}}</td>
   <td>all</td>
   <td>Automatically focus the form control when the page is loaded</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("capture", "input", "", 1)}}</td>
   <td>file</td>
   <td>Media capture input method in file upload controls</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("checked", "input", "", 1)}}</td>
   <td>radio, checkbox</td>
   <td>Whether the command or control is checked</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("dirname", "input", "", 1)}}</td>
   <td>text, search</td>
   <td>Name of form field to use for sending the element's directionality in form submission</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("disabled", "input", "", 1)}}</td>
   <td>all</td>
   <td>Whether the form control is disabled</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("form", "input", "", 1)}}</td>
   <td>all</td>
   <td>Associates the control with a form element</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("formaction", "input", "", 1)}}</td>
   <td>image, submit</td>
   <td>URL to use for form submission</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("formenctype", "input", "", 1)}}</td>
   <td>image, submit</td>
   <td>Form data set encoding type to use for form submission</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("formmethod", "input", "", 1)}}</td>
   <td>image, submit</td>
   <td>HTTP method to use for form submission</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("formnovalidate", "input", "", 1)}}</td>
   <td>image, submit</td>
   <td>Bypass form control validation for form submission</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("formtarget", "input", "", 1)}}</td>
   <td>image, submit</td>
   <td>Browsing context for form submission</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("height", "input", "", 1)}}</td>
   <td>image</td>
   <td>Same as <code>height</code> attribute for {{htmlelement('img')}}; vertical dimension</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("list", "input", "", 1)}}</td>
   <td>almost all</td>
   <td>Value of the id attribute of the {{htmlelement('datalist')}} of autocomplete options</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("max", "input", "", 1)}}</td>
   <td>numeric types</td>
   <td>Maximum value</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("maxlength", "input", "", 1)}}</td>
   <td>password, search, tel, text, url</td>
   <td>Maximum length (number of characters) of <code>value</code></td>
  </tr>
  <tr>
   <td>{{htmlattrxref("min", "input", "", 1)}}</td>
   <td>numeric types</td>
   <td>Minimum value</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("minlength", "input", "", 1)}}</td>
   <td>password, search, tel, text, url</td>
   <td>Minimum length (number of characters) of <code>value</code></td>
  </tr>
  <tr>
   <td>{{htmlattrxref("multiple", "input", "", 1)}}</td>
   <td>email, file</td>
   <td>Boolean. Whether to allow multiple values</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("name", "input", "", 1)}}</td>
   <td>all</td>
   <td>Name of the form control. Submitted with the form as part of a name/value pair.</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("pattern", "input", "", 1)}}</td>
   <td>password, text, tel</td>
   <td>Pattern the <code>value</code> must match to be valid</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("placeholder", "input", "", 1)}}</td>
   <td>password, search, tel, text, url</td>
   <td>Text that appears in the form control when it has no value set</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("readonly", "input", "", 1)}}</td>
   <td>almost all</td>
   <td>Boolean. The value is not editable</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("required", "input", "", 1)}}</td>
   <td>almost all</td>
   <td>Boolean. A value is required or must be check for the form to be submittable</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("size", "input", "", 1)}}</td>
   <td>email, password, tel, text</td>
   <td>Size of the control</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("src", "input", "", 1)}}</td>
   <td>image</td>
   <td>Same as <code>src</code> attribute for {{htmlelement('img')}}; address of image resource</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("step", "input", "", 1)}}</td>
   <td>numeric types</td>
   <td>Incremental values that are valid.</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("type", "input", "", 1)}}</td>
   <td>all</td>
   <td>Type of form control</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("value", "input", "", 1)}}</td>
   <td>all</td>
   <td>The initial value of the control.</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("width", "input", "", 1)}}</td>
   <td>image</td>
   <td>Same as <code>width</code> attribute for {{htmlelement('img')}}</td>
  </tr>
 </tbody>
</table>

<p>A few additional non-standard attributes are listed following the descriptions of the standard attributes.</p>

<h3 id="Individual_attributes">Individual attributes</h3>

<dl>
 <dt>{{htmlattrdef("accept")}}</dt>
 <dd>
 <p>Valid for the <code>file</code> input type only, the <code>accept</code> attribute defines which file types are selectable in a <code>file</code> upload control. See the {{HTMLElement("input/file", "file")}} input type.</p>
 </dd>
 <dt>{{htmlattrdef("alt")}}</dt>
 <dd>
 <p>Valid for the <code>image</code> button only, the <code>alt</code> attribute provides alternative text for the image, displaying the value of the attribute if the image {{htmlattrxref("scr", "input", "", 1)}} is missing or otherwise fails to load. See the {{HTMLElement("input/image", "image")}} input type.</p>
 </dd>
 <dt>{{htmlattrdef("autocomplete")}}</dt>
 <dd>
 <p>(<strong>Not</strong> a Boolean attribute!) The <code><a href="/en-US/docs/Web/HTML/Attributes/autocomplete">autocomplete</a></code> attribute takes as its value a space-separated string that describes what, if any, type of autocomplete functionality the input should provide. A typical implementation of autocomplete recalls previous values entered in the same input field, but more complex forms of autocomplete can exist. For instance, a browser could integrate with a device's contacts list to autocomplete <code>email</code> addresses in an email input field. See {{SectionOnPage("/en-US/docs/Web/HTML/Attributes/autocomplete", "Values")}} for permitted values.</p>

 <p>The <code>autocomplete</code> attribute is valid on <code>hidden</code>, <code>text</code>, <code>search</code>, <code>url</code>, <code>tel</code>, <code>email</code>, <code>date</code>, <code>month</code>, <code>week</code>, <code>time</code>, <code>datetime-local</code>, <code>number</code>, <code>range</code>, <code>color</code>, and <code>password</code>. This attribute has no effect on input types that do not return numeric or text data, being valid for all input types except <code>checkbox</code>, <code>radio</code>, <code>file</code>, or any of the button types.</p>

 <p>See <a href="/en-US/docs/Web/HTML/Attributes/autocomplete">The HTML autocomplete attribute</a> for additional information, including information on password security and how <code>autocomplete</code> is slightly different for <code>hidden</code> than for other input types.</p>
 </dd>
 <dt>{{htmlattrdef("autofocus")}}</dt>
 <dd>
 <p>A Boolean attribute which, if present, indicates that the input should automatically have focus when the page has finished loading (or when the {{HTMLElement("dialog")}} containing the element has been displayed).</p>

 <div class="note">
 <p><strong>Note:</strong> An element with the <code>autofocus</code> attribute may gain focus before the {{domxref("Window/DOMContentLoaded_event", "DOMContentLoaded")}} event is fired.</p>
 </div>

 <p>No more than one element in the document may have the <code>autofocus</code> attribute. If put on more than one element, the first one with the attribute receives focus.</p>

 <p>The <code>autofocus</code> attribute cannot be used on inputs of type <code>hidden</code>, since hidden inputs cannot be focused.</p>

 <div class="warning">
 <p><strong>Warning:</strong> Automatically focusing a form control can confuse visually-impaired people using screen-reading technology and people with cognitive impairments. When <code>autofocus</code> is assigned, screen-readers "teleport" their user to the form control without warning them beforehand.</p>
 </div>

 <p>Use careful consideration for accessibility when applying the <code>autofocus</code> attribute. Automatically focusing on a control can cause the page to scroll on load. The focus can also cause dynamic keyboards to display on some touch devices. While a screen reader will announce the label of the form control receiving focus, the screen reader will not announce anything before the label, and the sighted user on a small device will equally miss the context created by the preceding content.</p>
 </dd>
 <dt>{{htmlattrdef("capture")}}</dt>
 <dd>
 <p>Introduced in the HTML Media Capture specification and valid for the <code>file</code> input type only, the <code>capture</code> attribute defines which media—microphone, video, or camera—should be used to capture a new file for upload with <code>file</code> upload control in supporting scenarios. See the {{HTMLElement("input/file", "file")}} input type.</p>
 </dd>
 <dt>{{htmlattrdef("checked")}}</dt>
 <dd>
 <p>Valid for both <code>radio</code> and <code>checkbox</code> types, <code>checked</code> is a Boolean attribute. If present on a <code>radio</code> type, it indicates that the radio button is the currently selected one in the group of same-named radio buttons. If present on a <code>checkbox</code> type, it indicates that the checkbox is checked by default (when the page loads). It does <em>not</em> indicate whether this checkbox is currently checked: if the checkbox’s state is changed, this content attribute does not reflect the change. (Only the <a href="/en-US/docs/Web/API/HTMLInputElement"><code>HTMLInputElement</code>’s <code>checked</code> IDL attribute</a> is updated.)</p>

 <div class="note">
 <p><strong>Note:</strong> Unlike other input controls, a checkboxes and radio buttons value are only included in the submitted data if they are currently <code>checked</code>. If they are, the name and the value(s) of the checked controls are submitted.</p>

 <p>For example, if a checkbox whose <code>name</code> is <code>fruit</code> has a <code>value</code> of <code>cherry</code>, and the checkbox is checked, the form data submitted will include <code>fruit=cherry</code>. If the checkbox isn't active, it isn't listed in the form data at all. The default <code>value</code> for checkboxes and radio buttons is <code>on</code>.</p>
 </div>
 </dd>
 <dt>{{htmlattrdef("dirname")}}</dt>
 <dd>
 <p>Valid for <code>text</code> and <code>search</code> input types only, the <code>dirname</code> attribute enables the submission of the directionality of the element. When included, the form control will submit with two name/value pairs: the first being the {{htmlattrxref("name", "input")}} and {{htmlattrxref("value", "input")}}, the second being the value of the <code>dirname</code> as the name with the value of <code>ltr</code> or <code>rtl</code> being set by the browser.</p>

 <pre class="brush: html">&lt;form action="page.html" method="post"&gt;
  &lt;label&gt;Fruit: &lt;input type="text" name="fruit" dirname="fruit.dir" value="cherry"&gt;&lt;/label&gt;
  &lt;input type="submit"/&gt;
&lt;/form&gt;
&lt;!-- page.html?fruit=cherry&amp;fruit.dir=ltr --&gt;
</pre>

 <p>When the form above is submitted, the input cause both the <code>name</code> / <code>value</code> pair of <code>fruit=cherry</code> and the <code>dirname</code> / direction pair of <code>fruit.dir=ltr</code> to be sent.</p>
 </dd>
 <dt>{{htmlattrdef("disabled")}}</dt>
 <dd>
 <p>A Boolean attribute which, if present, indicates that the user should not be able to interact with the input. Disabled inputs are typically rendered with a dimmer color or using some other form of indication that the field is not available for use.</p>

 <p>Specifically, disabled inputs do not receive the {{domxref("Element/click_event", "click")}} event, and disabled inputs are not submitted with the form.</p>

 <div class="note">
 <p><strong>Note:</strong> Although not required by the specification, Firefox will by default <a href="https://stackoverflow.com/questions/5985839/bug-with-firefox-disabled-attribute-of-input-not-resetting-when-refreshing">persist the dynamic disabled state</a> of an <code>&lt;input&gt;</code> across page loads. Use the {{htmlattrxref("autocomplete", "input")}} attribute to control this feature.</p>
 </div>
 </dd>
 <dt>{{htmlattrdef("form")}}</dt>
 <dd>
 <p>A string specifying the {{HTMLElement("form")}} element with which the input is associated (that is, its <strong>form owner</strong>). This string's value, if present, must match the {{htmlattrxref("id")}} of a <code>&lt;form&gt;</code> element in the same document. If this attribute isn't specified, the <code>&lt;input&gt;</code> element is associated with the nearest containing form, if any.</p>

 <p>The <code>form</code> attribute lets you place an input anywhere in the document but have it included with a form elsewhere in the document.</p>

 <div class="note">
 <p><strong>Note:</strong> An input can only be associated with one form.</p>
 </div>
 </dd>
 <dt>{{htmlattrdef('formaction')}}</dt>
 <dd>
 <p>Valid for the <code>image</code> and <code>submit</code> input types only. See the {{HTMLElement("input/submit", "submit")}} input type for more information.</p>
 </dd>
 <dt>{{htmlattrdef('formenctype')}}</dt>
 <dd>
 <p>Valid for the <code>image</code> and <code>submit</code> input types only. See the {{HTMLElement("input/submit", "submit")}} input type for more information.</p>
 </dd>
 <dt>{{htmlattrdef('formmethod')}}</dt>
 <dd>
 <p>Valid for the <code>image</code> and <code>submit</code> input types only. See the {{HTMLElement("input/submit", "submit")}} input type for more information.</p>
 </dd>
 <dt>{{htmlattrdef('formnovalidate')}}</dt>
 <dd>
 <p>Valid for the <code>image</code> and <code>submit</code> input types only. See the {{HTMLElement("input/submit", "submit")}} input type for more information.</p>
 </dd>
 <dt>{{htmlattrdef('formtarget')}}</dt>
 <dd>
 <p>Valid for the <code>image</code> and <code>submit</code> input types only. See the {{HTMLElement("input/submit", "submit")}} input type for more information.</p>
 </dd>
 <dt>{{htmlattrdef("height")}}</dt>
 <dd>
 <p>Valid for the <code>image</code> input button only, the <code>height</code> is the height of the image file to display to represent the graphical submit button. See the {{HTMLElement("input/image", "image")}} input type.</p>
 </dd>
 <dt>{{htmlattrdef("id")}}</dt>
 <dd>
 <p>Global attribute valid for all elements, including all the input types, it defines a unique identifier (ID) which must be unique in the whole document. Its purpose is to identify the element when linking. The value is used as the value of the {{htmlelement('label')}}'s <code>for</code> attribute to link the label with the form control. See {{htmlelement('label')}}.</p>
 </dd>
 <dt>{{htmlattrdef("inputmode")}}</dt>
 <dd>
 <p>Global value valid for all elements, it provides a hint to browsers as to the type of virtual keyboard configuration to use when editing this element or its contents. Values include <code>none</code>, <code>text</code>, <code>tel</code>, <code>url</code>, <code>email</code>, <code>numeric</code>, <code>decimal</code>, and <code>search</code>.</p>
 </dd>
 <dt>{{htmlattrdef("list")}}</dt>
 <dd>
 <p>The value given to the <code>list</code> attribute should be the {{domxref("Element.id", "id")}} of a {{HTMLElement("datalist")}} element located in the same document. The <code>&lt;datalist&gt;</code> provides a list of predefined values to suggest to the user for this input. Any values in the list that are not compatible with the {{htmlattrxref("type", "input")}} are not included in the suggested options. The values provided are suggestions, not requirements: users can select from this predefined list or provide a different value.</p>

 <p>It is valid on <code>text</code>, <code>search</code>, <code>url</code>, <code>tel</code>, <code>email</code>, <code>date</code>, <code>month</code>, <code>week</code>, <code>time</code>, <code>datetime-local</code>, <code>number</code>, <code>range</code>, and <code>color</code>.</p>

 <p>Per the specifications, the <code>list</code> attribute is not supported by the <code>hidden</code>, <code>password</code>, <code>checkbox</code>, <code>radio</code>, <code>file</code>, or any of the button types.</p>

 <p>Depending on the browser, the user may see a custom color palette suggested, tic marks along a range, or even a input that opens like a {{HTMLElement("select")}} but allows for non-listed values. Check out the <a href="/en-US/docs/Web/HTML/Element/datalist#browser_compatibility">browser compatibility table</a> for the other input types.</p>

 <p>See the {{htmlelement('datalist')}} element.</p>
 </dd>
 <dt>{{htmlattrdef("max")}}</dt>
 <dd>
 <p>Valid for <code>date</code>, <code>month</code>, <code>week</code>, <code>time</code>, <code>datetime-local</code>, <code>number</code>, and <code>range</code>, it defines the greatest value in the range of permitted values. If the {{htmlattrxref("value", "input")}} entered into the element exceeds this, the element fails <a href="/en-US/docs/Web/Guide/HTML/Constraint_validation">constraint validation</a>. If the value of the <code>max</code> attribute isn't a number, then the element has no maximum value.</p>

 <p>There is a special case: if the data type is periodic (such as for dates or times), the value of <code>max</code> may be lower than the value of <code>min</code>, which indicates that the range may wrap around; for example, this allows you to specify a time range from 10 PM to 4 AM.</p>
 </dd>
 <dt>{{htmlattrdef("maxlength")}}</dt>
 <dd>
 <p>Valid for <code>text</code>, <code>search</code>, <code>url</code>, <code>tel</code>, <code>email</code>, and <code>password</code>, it defines the maximum number of characters (as UTF-16 code units) the user can enter into the field. This must be an integer value <code>0</code> or higher. If no <code>maxlength</code> is specified, or an invalid value is specified, the field has no maximum length. This value must also be greater than or equal to the value of <code>minlength</code>.</p>

 <p>The input will fail <a href="/en-US/docs/Web/Guide/HTML/Constraint_validation">constraint validation</a> if the length of the text entered into the field is greater than <code>maxlength</code> UTF-16 code units long. By default, browsers prevent users from entering more characters than allowed by the <code>maxlength</code> attribute. See {{anch("Client-side validation")}} for more information.</p>
 </dd>
 <dt>{{htmlattrdef("min")}}</dt>
 <dd>
 <p>Valid for <code>date</code>, <code>month</code>, <code>week</code>, <code>time</code>, <code>datetime-local</code>, <code>number</code>, and <code>range</code>, it defines the most negative value in the range of permitted values. If the {{htmlattrxref("value", "input")}} entered into the element is less than this this, the element fails <a href="/en-US/docs/Web/Guide/HTML/Constraint_validation">constraint validation</a>. If the value of the <code>min</code> attribute isn't a number, then the element has no minimum value.</p>

 <p>This value must be less than or equal to the value of the <code>max</code> attribute. If the <code>min</code> attribute is present but is not specified or is invalid, no <code>min</code> value is applied. If the <code>min</code> attribute is valid and a non-empty value is less than the minimum allowed by the <code>min</code> attribute, constraint validation will prevent form submission. See {{anch("Client-side validation")}} for more information.</p>

 <p>There is a special case: if the data type is periodic (such as for dates or times), the value of <code>max</code> may be lower than the value of <code>min</code>, which indicates that the range may wrap around; for example, this allows you to specify a time range from 10 PM to 4 AM.</p>
 </dd>
 <dt>{{htmlattrdef("minlength")}}</dt>
 <dd>
 <p>Valid for <code>text</code>, <code>search</code>, <code>url</code>, <code>tel</code>, <code>email</code>, and <code>password</code>, it defines the minimum number of characters (as UTF-16 code units) the user can enter into the entry field. This must be an non-negative integer value smaller than or equal to the value specified by <code>maxlength</code>. If no <code>minlength</code> is specified, or an invalid value is specified, the input has no minimum length.</p>

 <p>The input will fail <a href="/en-US/docs/Web/Guide/HTML/Constraint_validation">constraint validation</a> if the length of the text entered into the field is fewer than <code>minlength</code> UTF-16 code units long, preventing form submission. See {{anch("Client-side validation")}} for more information.</p>
 </dd>
 <dt>{{htmlattrdef("multiple")}}</dt>
 <dd>
 <p>The Boolean <code>multiple</code> attribute, if set, means the user can enter comma separated email addresses in the email widget or can choose more than one file with the <code>file</code> input. See the {{HTMLElement("input/email", "email")}} and {{HTMLElement("input/file", "file")}} input type.</p>
 </dd>
 <dt>{{htmlattrdef("name")}}</dt>
 <dd>
 <p>A string specifying a name for the input control. This name is submitted along with the control's value when the form data is submitted.</p>

 <p>Consider the <code>name</code> a required attribute (even though it's not). If an input has no <code>name</code> specified, or <code>name</code> is empty, the input's value is not submitted with the form! (Disabled controls, unchecked radio buttons, unchecked checkboxes, and reset buttons are also not sent.)</p>

 <p>There are two special cases:</p>

 <ol>
  <li><code>_charset_</code> : If used as the name of an <code>&lt;input&gt;</code> element of type {{HTMLElement("input/hidden", "hidden")}}, the input's <code>value</code> is automatically set by the {{Glossary("user agent")}} to the character encoding being used to submit the form.</li>
  <li><code>isindex</code>: For historical reasons, the name <code><a href="https://html.spec.whatwg.org/multipage/form-control-infrastructure.html#attr-fe-name">isindex</a></code> is not allowed.</li>
 </ol>

 <p>The <a href="#htmlattrdefname"><code>name</code></a> attribute creates a unique behavior for radio buttons.</p>

 <p>Only one radio button in a same-named group of radio buttons can be checked at a time. Selecting any radio button in that group automatically deselects any currently-selected radio button in the same group. The value of that one checked radio button is sent along with the name if the form is submitted,</p>

 <p>When tabbing into a series of same-named group of radio buttons, if one is checked, that one will receive focus. If they aren't grouped together in source order, if one of the group is checked, tabbing into the group starts when the first one in the group is encountered, skipping all those that aren't checked. In other words, if one is checked, tabbing skips the unchecked radio buttons in the group. If none are checked, the radio button group receives focus when the first button in the same name group is reached.</p>

 <p>Once one of the radio buttons in a group has focus, using the arrow keys will navigate through all the radio buttons of the same name, even if the radio buttons are not grouped together in the source order.</p>

 <p>When an input element is given a <code>name</code>, that name becomes a property of the owning form element's {{domxref("HTMLFormElement.elements")}} property. If you have an input whose <code>name</code> is set to <code>guest</code> and another whose <code>name</code> is <code>hat-size</code>, the following code can be used:</p>

 <pre class="brush: js">let form = document.querySelector("form");

let guestName = form.elements.guest;
let hatSize = form.elements["hat-size"];
</pre>

 <p>When this code has run, <code>guestName</code> will be the {{domxref("HTMLInputElement")}} for the <code>guest</code> field, and <code>hatSize</code> the object for the <code>hat-size</code> field.</p>

 <div class="warning">
 <p><strong>Warning:</strong> Avoid giving form elements a <code>name</code> that corresponds to a built-in property of the form, since you would then override the predefined property or method with this reference to the corresponding input.</p>
 </div>
 </dd>
 <dt>{{htmlattrdef("pattern")}}</dt>
 <dd>
 <p>The <code>pattern</code> attribute, when specified, is a regular expression that the input's {{htmlattrxref("value", "input")}} must match in order for the value to pass <a href="/en-US/docs/Web/Guide/HTML/Constraint_validation">constraint validation</a>. It must be a valid JavaScript regular expression, as used by the {{jsxref("RegExp")}} type, and as documented in our <a href="/en-US/docs/Web/JavaScript/Guide/Regular_Expressions">guide on regular expressions</a>; the <code>'u'</code> flag is specified when compiling the regular expression, so that the pattern is treated as a sequence of Unicode code points, instead of as ASCII. No forward slashes should be specified around the pattern text.</p>

 <p>If the <code>pattern</code> attribute is present but is not specified or is invalid, no regular expression is applied and this attribute is ignored completely. If the pattern attribute is valid and a non-empty value does not match the pattern, constraint validation will prevent form submission.</p>

 <div class="note">
 <p><strong>Note:</strong> If using the <code>pattern</code> attribute, inform the user about the expected format by including explanatory text nearby. You can also include a {{htmlattrxref("title", "input")}} attribute to explain what the requirements are to match the pattern; most browsers will display this title as a tooltip. The visible explanation is required for accessibility. The tooltip is an enhancement.</p>
 </div>

 <p>See {{anch("Client-side validation")}} for more information.</p>
 </dd>
 <dt>{{htmlattrdef("placeholder")}}</dt>
 <dd>
 <p>The <code>placeholder</code> attribute is a string that provides a brief hint to the user as to what kind of information is expected in the field. It should be a word or short phrase that provides a hint as to the expected type of data, rather than an explanation or prompt. The text <em>must not</em> include carriage returns or line feeds. So for example if a field is expected to capture a user's first name, and its label is "First Name", a suitable placeholder might be "e.g. Mustafa".</p>

 <div class="note">
 <p><strong>Note:</strong> The <code>placeholder</code> attribute is not as semantically useful as other ways to explain your form, and can cause unexpected technical issues with your content. See {{anch("Labels")}} for more information.</p>
 </div>
 </dd>
 <dt>{{htmlattrdef("readonly")}}</dt>
 <dd>
 <p>A Boolean attribute which, if present, indicates that the user should not be able to edit the value of the input. The <code>readonly</code> attribute is supported by the <code>text</code>, <code>search</code>, <code>url</code>, <code>tel</code>, <code>email</code>, <code>date</code>, <code>month</code>, <code>week</code>, <code>time</code>, <code>datetime-local</code>, <code>number</code>, and <code>password</code> input types.</p>

 <p>See the <a href="/en-US/docs/Web/HTML/Attributes/readonly">HTML attribute: <code>readonly</code></a> for more information.</p>
 </dd>
 <dt>{{htmlattrdef("required")}}</dt>
 <dd>
 <p><code>required</code> is a Boolean attribute which, if present, indicates that the user must specify a value for the input before the owning form can be submitted. The <code>required</code> attribute is supported by <code>text</code>, <code>search</code>, <code>url</code>, <code>tel</code>, <code>email</code>, <code>date</code>, <code>month</code>, <code>week</code>, <code>time</code>, <code>datetime-local</code>, <code>number</code>, <code>password</code>, <code>checkbox</code>, <code>radio</code>, and <code>file</code> inputs.</p>

 <p>See {{anch("Client-side validation")}} and the <a href="/en-US/docs/Web/HTML/Attributes/required">HTML attribute: <code>required</code></a> for more information.</p>
 </dd>
 <dt>{{htmlattrdef("size")}}</dt>
 <dd>Valid for <code>email</code>, <code>password</code>, <code>tel</code>, and <code>text</code> <code>input</code> types only. Specifies how much of the input is shown. Basically creates same result as setting CSS <code>width</code> property with a few specialities. The actual unit of the value depends on the input type. For <code>password</code> and <code>text</code>, it is a number of characters (or <code>em</code> units) with a default value of <code>20</code>, and for others, it is <code>pixel</code>s. CSS width takes precedence over size attribute.</dd>
 <dt>{{htmlattrdef("src")}}</dt>
 <dd>
 <p>Valid for the <code>image</code> input button only, the <code>src</code> is string specifying the URL of the image file to display to represent the graphical submit button. See the {{HTMLElement("input/image", "image")}} input type.</p>
 </dd>
 <dt>{{htmlattrdef("step")}}</dt>
 <dd>
 <p>Valid for the numeric input types, including <code>number</code>, date/time input types, and <code>range</code>, the <code><a href="/en-US/docs/Web/HTML/Attributes/step">step</a></code> attribute is a number that specifies the granularity that the value must adhere to.</p>

 <p>If not explicitly included:</p>

 <ul>
  <li><code>step</code> defaults to 1 for <code>number</code> and <code>range</code>.</li>
  <li>For the date/time input types, <code>step</code> is expressed in seconds, with the <strong>default step being 60 seconds</strong>. The step scale factor is 1000 (which converts the seconds to milliseconds, as used in other algorithms).</li>
 </ul>

 <p>The value must be a positive number—integer or float—or the special value <code>any</code>, which means no stepping is implied, and any value is allowed (barring other constraints, such as <code>{{anch("min")}}</code> and <code>{{anch("max")}}</code>).</p>

 <p>If <code>any</code> is not explicity set, valid values for the <code>number</code>, date/time input types, and <code>range</code> input types are equal to the basis for stepping — the <code>{{anch("min")}}</code> value and increments of the step value, up to the <code>{{anch("max")}}</code> value, if specified.</p>

 <p>For example, if you have <code>&lt;input type="number" min="10" step="2"&gt;</code>, then any even integer, <code>10</code> or greater, is valid. If omitted, <code>&lt;input type="number"&gt;</code>, any integer is valid, but floats (like <code>4.2</code>) are not valid, because <code>step</code> defaults to <code>1</code>. For <code>4.2</code> to be valid, <code>step</code> would have had to be set to <code>any</code>, 0.1, 0.2, or any the <code>min</code> value would have had to be a number ending in <code>.2</code>, such as <code>&lt;input type="number" min="-5.2"&gt;</code></p>

 <div class="note">
 <p><strong>Note:</strong> When the data entered by the user doesn't adhere to the stepping configuration, the value is considered invalid in contraint validation and will match the <code>:invalid</code> pseudoclass.</p>
 </div>

 <p>See {{anch("Client-side validation")}} for more information.</p>
 </dd>
 <dt>{{htmlattrdef("tabindex")}}</dt>
 <dd>
 <p>Global attribute valid for all elements, including all the input types, an integer attribute indicating if the element can take input focus (is focusable), if it should participate to sequential keyboard navigation. As all input types except for input of type hidden are focusable, this attribute should not be used on form controls, because doing so would require the management of the focus order for all elements within the document with the risk of harming usability and accessibility if done incorrectly.</p>
 </dd>
 <dt>{{htmlattrdef('title')}}</dt>
 <dd>
 <p>Global attribute valid for all elements, including all input types, containing a text representing advisory information related to the element it belongs to. Such information can typically, but not necessarily, be presented to the user as a tooltip. The title should NOT be used as the primary explanation of the purpose of the form control. Instead, use the {{htmlelement('label')}} element with a <code>for</code> attribute set to the form control's {{htmlattrdef('id')}} attribute. See {{anch("Labels")}} below.</p>
 </dd>
 <dt>{{htmlattrdef("type")}}</dt>
 <dd>
 <p>A string specifying the type of control to render. For example, to create a checkbox, a value of <code>checkbox</code> is used. If omitted (or an unknown value is specified), the input type <code>text</code> is used, creating a plaintext input field.</p>

 <p>Permitted values are listed in <a href="#input_types">Input types</a> above.</p>
 </dd>
 <dt>{{htmlattrdef("value")}}</dt>
 <dd>
 <p>The input control's value. When specified in the HTML, this is the initial value, and from then on it can be altered or retrieved at any time using JavaScript to access the respective {{domxref("HTMLInputElement")}} object's <code>value</code> property. The <code>value</code> attribute is always optional, though should be considered mandatory for <code>checkbox</code>, <code>radio</code>, and <code>hidden</code>.</p>
 </dd>
 <dt>{{htmlattrdef("width")}}</dt>
 <dd>
 <p>Valid for the <code>image</code> input button only, the <code>width</code> is the width of the image file to display to represent the graphical submit button. See the {{HTMLElement("input/image", "image")}} input type.</p>
 </dd>
</dl>

<h3 id="Non-standard_attributes">Non-standard attributes</h3>

<p>The following non-standard attributes are also available on some browsers. As a general rule, you should avoid using them unless it can't be helped.</p>

<table class="no-markdown">
 <thead>
  <tr>
   <th scope="col">Attribute</th>
   <th scope="col">Description</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{htmlattrxref("autocorrect", "input", "", 1)}}</td>
   <td>A string indicating whether or not autocorrect is <code>on</code> or <code>off</code>. <strong>Safari only.</strong></td>
  </tr>
  <tr>
   <td>{{htmlattrxref("incremental", "input", "", 1)}}</td>
   <td>Whether or not to send repeated {{domxref("HTMLInputElement/search_event", "search")}} events to allow updating live search results while the user is still editing the value of the field. <strong>WebKit and Blink only (Safari, Chrome, Opera, etc.).</strong></td>
  </tr>
  <tr>
   <td>{{htmlattrxref("mozactionhint", "input", "", 1)}}</td>
   <td>A string indicating the type of action that will be taken when the user presses the <kbd>Enter</kbd> or <kbd>Return</kbd> key while editing the field; this is used to determine an appropriate label for that key on a virtual keyboard. <strong>Firefox for Android only</strong>.</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("orient", "input", "", 1)}}</td>
   <td>Sets the orientation of the range slider. <strong>Firefox only</strong>.</td>
  </tr>
  <tr>
   <td>{{htmlattrxref("results", "input", "", 1)}}</td>
   <td>The maximum number of items that should be displayed in the drop-down list of previous search queries. <strong>Safari only.</strong></td>
  </tr>
  <tr>
   <td>{{htmlattrxref("webkitdirectory", "input", "", 1)}}</td>
   <td>A Boolean indicating whether or not to only allow the user to choose a directory (or directories, if {{htmlattrxref("multiple", "input", "", 1)}} is also present)</td>
  </tr>
 </tbody>
</table>

<dl>
 <dt>{{htmlattrdef("autocorrect")}} {{non-standard_inline}}</dt>
 <dd>
   <p>A Safari extension, the <code>autocorrect</code> attribute is a string which indicates whether or not to activate automatic correction while the user is editing this field. Permitted values are:</p>

   <dl>
    <dt><code>on</code></dt>
    <dd>Enable automatic correction of typos, as well as processing of text substitutions if any are configured.</dd>
    <dt><code>off</code></dt>
    <dd>Disable automatic correction and text substitutions.</dd>
   </dl>
 </dd>
 <dt>{{htmlattrdef("incremental")}} {{non-standard_inline}}</dt>
 <dd>
   <p>The Boolean attribute <code>incremental</code> is a WebKit and Blink extension (so supported by Safari, Opera, Chrome, etc.) which, if present, tells the {{Glossary("user agent")}} to process the input as a live search. As the user edits the value of the field, the user agent sends {{event("search")}} events to the {{domxref("HTMLInputElement")}} object representing the search box. This allows your code to update the search results in real time as the user edits the search.</p>

   <p>If <code>incremental</code> is not specified, the {{event("search")}} event is only sent when the user explicitly initiates a search (such as by pressing the <kbd>Enter</kbd> or <kbd>Return</kbd> key while editing the field).</p>

   <p>The <code>search</code> event is rate-limited so that it is not sent more frequently than an implementation-defined interval.</p>
 </dd>
 <dt>{{htmlattrdef("mozactionhint")}} {{non-standard_inline}}</dt>
 <dd>
   <p>A Mozilla extension, supported by Firefox for Android, which provides a hint as to what sort of action will be taken if the user presses the <kbd>Enter</kbd> or <kbd>Return</kbd> key while editing the field. This information is used to decide what kind of label to use on the <kbd>Enter</kbd> key on the virtual keyboard.</p>

   <div class="note">
   <p><strong>Note:</strong> This <a href="https://html.spec.whatwg.org/#input-modalities:-the-enterkeyhint-attribute">has been standardized</a> as the global attribute {{htmlattrxref("enterkeyhint")}}, but is not yet widely implemented. To see the status of the change being implemented in Firefox, see {{bug(1490661)}}.</p>
   </div>

   <p>Permitted values are: <code>go</code>, <code>done</code>, <code>next</code>, <code>search</code>, and <code>send</code>. The browser decides, using this hint, what label to put on the enter key.</p>
 </dd>
 <dt>{{htmlattrdef("orient")}} {{non-standard_inline}}</dt>
 <dd>
   <p>Similar to the -moz-orient non-standard CSS property impacting the {{htmlelement('progress')}} and {{htmlelement('meter')}} elements, the <code>orient</code> attribute defines the orientation of the range slider. Values include <code>horizontal</code>, meaning the range is rendered horizontally, and <code>vertical</code>, where the range is rendered vertically.</p>
 </dd>
 <dt>{{htmlattrdef("results")}} {{non-standard_inline}}</dt>
 <dd>
   <p>The <code>results</code> attribute—supported only by Safari—is a numeric value that lets you override the maximum number of entries to be displayed in the {{HTMLElement("input")}} element's natively-provided drop-down menu of previous search queries.</p>

   <p>The value must be a non-negative decimal number. If not provided, or an invalid value is given, the browser's default maximum number of entries is used.</p>
 </dd>
 <dt>{{htmlattrdef("webkitdirectory")}} {{non-standard_inline}}</dt>
 <dd>
   <p>The Boolean <code>webkitdirectory</code> attribute, if present, indicates that only directories should be available to be selected by the user in the file picker interface. See {{domxref("HTMLInputElement.webkitdirectory")}} for additional details and examples.</p>

   <p>Though originally implemented only for WebKit-based browsers, <code>webkitdirectory</code> is also usable in Microsoft Edge as well as Firefox 50 and later. However, even though it has relatively broad support, it is still not standard and should not be used unless you have no alternative.</p>
 </dd>
</dl>

<h2 id="Methods">Methods</h2>

<p>The following methods are provided by the {{domxref("HTMLInputElement")}} interface which represents <code>&lt;input&gt;</code> elements in the DOM. Also available are those methods specified by the parent interfaces, {{domxref("HTMLElement")}}, {{domxref("Element")}}, {{domxref("Node")}}, and {{domxref("EventTarget")}}.</p>

<dl>
 <dt>{{domxref("HTMLInputElement.checkValidity", "checkValidity()")}}</dt>
 <dd>Immediately runs the validity check on the element, triggering the document to fire the {{domxref("HTMLInputElement.invalid_event", "invalid")}} event at the element if the value isn't valid.</dd>
 <dt>{{domxref("HTMLFormElement.reportValidity", "reportValidity()")}}</dt>
 <dd>Returns <code>true</code> if the element's value passes validity checks; otherwise, returns <code>false</code>.</dd>
 <dt>{{domxref("HTMLInputElement.select", "select()")}}</dt>
 <dd>Selects the entire content of the <code>&lt;input&gt;</code> element, if the element's content is selectable. For elements with no selectable text content (such as a visual color picker or calendar date input), this method does nothing.</dd>
 <dt>{{domxref("HTMLInputElement.setCustomValidity", "setCustomValidity()")}}</dt>
 <dd>Sets a custom message to display if the input element's value isn't valid.</dd>
 <dt>{{domxref("HTMLInputElement.setRangeText", "setRangeText()")}}</dt>
 <dd>Sets the contents of the specified range of characters in the input element to a given string. A <code>selectMode</code> parameter is available to allow controlling how the existing content is affected.</dd>
 <dt>{{domxref("HTMLInputElement.setSelectionRange", "setSelectionRange()")}}</dt>
 <dd>Selects the specified range of characters within a textual input element. Does nothing for inputs which aren't presented as text input fields.</dd>
 <dt>{{domxref("HTMLInputElement.stepDown", "stepDown()")}}</dt>
 <dd>Decrements the value of a numeric input by one, by default, or by the specified number of units.</dd>
 <dt>{{domxref("HTMLInputElement.stepUp", "stepUp()")}}</dt>
 <dd>Increments the value of a numeric input by one or by the specified number of units.</dd>
</dl>

<h2 id="CSS">CSS</h2>

<p>Inputs, being replaced elements, have a few features not applicable to non form elements. There are CSS selectors that can specification target form controls based on their UI features, also known as UI pseudo-classes. The input element can also be targeted by type with attribute selectors. There are some properties that are especially useful as well.</p>

<h3 id="UI_pseudo-classes">UI pseudo-classes</h3>

<table class="no-markdown">
 <caption>Captions super relevant to the <code>&lt;input&gt;</code> element:</caption>
 <thead>
  <tr>
   <th>Pseudo-class</th>
   <th>Description</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{Cssxref(":enabled")}}</td>
   <td>Any currently enabled element that can be activated (selected, clicked on, typed into, etc.) or accept focus and also has a disabled state, in which it can't be activated or accept focus.</td>
  </tr>
  <tr>
   <td>{{Cssxref(":disabled")}}</td>
   <td>Any currently disabled element that has an enabled state, meaning it otherwise could be activated (selected, clicked on, typed into, etc.) or accept focus were it not disabled.</td>
  </tr>
  <tr>
   <td>{{Cssxref(":read-only")}}</td>
   <td>Element not editable by the user</td>
  </tr>
  <tr>
   <td>{{Cssxref(":read-write")}}</td>
   <td>Element that is editable by the user.</td>
  </tr>
  <tr>
   <td>{{Cssxref(":placeholder-shown")}}</td>
   <td>Element that is currently displaying {{htmlattrxref("placeholder", "input", "placeholder text", 1)}}, including <code>&lt;input&gt;</code> and {{HTMLElement("textarea")}} elements with the {{htmlattrxref("placeholder", "input", "", 1)}} attribute present that has, as of yet, no value.</td>
  </tr>
  <tr>
   <td>{{Cssxref(":default")}}</td>
   <td>Form elements that are the default in a group of related elements. Matches {{HTMLElement("input/checkbox", "checkbox")}} and {{HTMLElement("input/radio", "radio")}} input types that were checked on page load or render.</td>
  </tr>
  <tr>
   <td>{{Cssxref(":checked")}}</td>
   <td>Matches {{HTMLElement("input/checkbox", "checkbox")}} and {{HTMLElement("input/radio", "radio")}} input types that are currently checked (and the ({{HTMLElement("option")}} in a {{HTMLElement("select")}} that is currently selected).</td>
  </tr>
  <tr>
   <td>{{Cssxref(":indeterminate")}}</td>
   <td>{{HTMLElement("input/checkbox", "checkbox")}} elements whose indeterminate property is set to true by JavaScript, {{HTMLElement("input/radio", "radio")}} elements, when all radio buttons with the same name value in the form are unchecked, and {{HTMLElement("progress")}} elements in an indeterminate state</td>
  </tr>
  <tr>
   <td>{{Cssxref(":valid")}}</td>
   <td>Form controls that can have constraint validation applied and are currently valid.</td>
  </tr>
  <tr>
   <td>{{Cssxref(":invalid")}}</td>
   <td>Form controls that have constraint validation applied and are currently not valid. Matches a form control whose value doesn't match the constraints set on it by it's attributes, such as {{ htmlattrxref("required", "input", "", 1)}}, {{ htmlattrxref("pattern", "input", "", 1)}} , {{ htmlattrxref("step", "input", "", 1)}} and {{ htmlattrxref("max", "input", "", 1)}}.</td>
  </tr>
  <tr>
   <td>{{Cssxref(":in-range")}}</td>
   <td>A non-empty input whose current value is within the range limits specified by the {{anch('htmlattrdefmin', 'min')}} and {{anch('htmlattrdefmax', 'max')}} attributes and the {{anch('htmlattrdefstep', 'step')}} .</td>
  </tr>
  <tr>
   <td>{{Cssxref(":out-of-range")}}</td>
   <td>A non-empty input whose current value is NOT within the range limits specified by the {{ htmlattrxref("min", "input", "", 1)}} and {{ htmlattrxref("max", "input", "", 1)}} attributes or does not adher to the {{ htmlattrxref("step", "input", "", 1)}} constraint.</td>
  </tr>
  <tr>
   <td>{{Cssxref(":required")}}</td>
   <td><code>&lt;input&gt;</code>, {{HTMLElement("select")}}, or {{HTMLElement("textarea")}} element that has the {{ htmlattrxref("required", "input", "", 1)}} attribute set on it. Only matches elements that can be required. The attribute included on a non-requirable element will not make for a match.</td>
  </tr>
  <tr>
   <td>{{Cssxref(":optional")}}</td>
   <td><code>&lt;input&gt;</code>, {{HTMLElement("select")}}, or {{HTMLElement("textarea")}} element that does NOT have the {{ htmlattrxref("required", "input", "", 1)}} attribute set on it. Does not match elements that can't be required.</td>
  </tr>
  <tr>
   <td>{{Cssxref(":blank")}}</td>
   <td><code>&lt;input&gt;</code> and {{HTMLElement("textarea")}} elements that currently have no value.</td>
  </tr>
  <tr>
   <td>{{Cssxref(":user-invalid")}}</td>
   <td>Similar to <code>:invalid</code>, but is activated on blur. Matches invalid input but only after the user interaction, such as by focusing on the control, leaving the control, or attempting to submit the form containing the invalid control.</td>
  </tr>
 </tbody>
</table>

<h4>Pseudo-classes example</h4>

<p>We can style a checkbox label based on whether the checkbox is checked or not. In this example, we are styling the {{cssxref('color')}} and {{cssxref('font-weight')}} of the {{htmlelement('label')}} that comes immediately after a checked input. We haven't applied any styles if the <code>input</code> is not checked.</p>

<pre class="brush: html hidden">&lt;input id="checkboxInput" type="checkbox"&gt;
&lt;label for="checkboxInput"&gt;Toggle the checkbox on and off&lt;/label&gt;
</pre>

<pre class="brush: css">input:checked + label {
  color: red;
  font-weight: bold;
}
</pre>

<p>{{EmbedLiveSample('Pseudo-classes_example', 500, 80)}}</p>

<h3 id="Attribute_selectors">Attribute selectors</h3>

<p>It is possible to target different types of form controls based on their {{ htmlattrxref("type", "input", "", 1)}} using <a href="/en-US/docs/Learn/CSS/Building_blocks/Selectors/Attribute_selectors">attribute selectors</a>. CSS attribute selectors match elements based on either just the presence of a attribute or the value of a given attribute.</p>

<pre class="brush: css">/* matches a password input */
input[type="password"] {}

/* matches a form control whose valid values are limited to a range of values*/
input[min][max] {}

/* matches a form control with a pattern attribute */
 input[pattern] {}</pre>

<h3 id="placeholder">::placeholder</h3>

<p>By default, the appearance of placeholder text is a translucent or light gray. The {{cssxref('::placeholder')}} pseudo-element is the input's {{ htmlattrxref("placeholder", "input", "placeholder text", 1)}}. It can be styled with a limited subset of CSS properties.</p>

<pre class="brush: css">::placeholder {
  color: blue;
}</pre>

<p>Only the subset of CSS properties that apply to the {{cssxref("::first-line")}} pseudo-element can be used in a rule using <code>::placeholder</code> in its selector.</p>

<h3 id="appearance">appearance</h3>

<p>The {{cssxref("appearance")}} property enables the displaying of (almost) any element as a platform-native style based on the operating system's theme as well as the removal of any platform-native styling with the <code>none</code> value.</p>

<p>You could make a <code>&lt;div&gt;</code> look like a radio button with <code>div {appearance: radio;} </code>or a radio look like a checkbox with <code>[type="checkbox] {appearance: checkbox;}</code>, but don't.</p>

<p>Setting <code>appearance: none</code> removes platform native borders, but not functionality.</p>

<h3 id="caret-color">caret-color</h3>

<p>A property specific to text entry-related elements is the CSS {{cssxref("caret-color")}} property, which lets you set the color used to draw the text input caret:</p>

<h4 id="HTML">HTML</h4>

<pre class="brush: html">&lt;label for="textInput"&gt;Note the red caret:&lt;/label&gt;
&lt;input id="textInput" class="custom" size="32"&gt;
</pre>

<h4 id="CSS_2">CSS</h4>

<pre class="brush: css">input.custom {
  caret-color: red;
  font: 16px "Helvetica", "Arial", "sans-serif"
}
</pre>

<h4 id="Result">Result</h4>

<p>{{EmbedLiveSample('caret-color', 500, 80)}}</p>

<h3 id="object-position_and_object-fit">object-position and object-fit</h3>

<p>In certain cases (typically involving non-textual inputs and specialized interfaces), the <code>&lt;input&gt;</code> element is a <a href="/en-US/docs/Web/CSS/Replaced_element">replaced element</a>. When it is, the position and size of the element's size and positioning within its frame can be adjusted using the CSS {{cssxref("object-position")}} and {{cssxref("object-fit")}} properties</p>

<h3 id="Styling">Styling</h3>

<p>For more information about adding color to elements in HTML, see:</p>

<ul>
 <li><a href="/en-US/docs/Web/HTML/Applying_color">Applying color to HTML elements using CSS</a>.</li>
</ul>

<p>Also see:</p>

<ul>
 <li><a href="/en-US/docs/Learn/Forms/Styling_web_forms">Styling HTML forms</a></li>
 <li><a href="/en-US/docs/Learn/Forms/Advanced_form_styling">Advanced styling for HTML forms</a> and</li>
 <li>the<a href="/en-US/docs/Learn/Forms/Property_compatibility_table_for_form_controls"> compatibility table of CSS properties</a>.</li>
</ul>

<h2 id="Additional_features">Additional features</h2>

<h3 id="Labels">Labels</h3>

<p>Labels are needed to associate assistive text with an <code>&lt;input&gt;</code>. The {{HTMLElement("label")}} element provides explanatory information about a form field that is <em>always</em> appropriate (aside from any layout concerns you have). It's never a bad idea to use a <code>&lt;label&gt;</code> to explain what should be entered into an <code>&lt;input&gt;</code> or {{HTMLElement("textarea")}}.</p>

<h4 id="Associated_labels">Associated labels</h4>

<p>The semantic pairing of <code>&lt;input&gt;</code> and <code>&lt;label&gt;</code> elements is useful for assistive technologies such as screen readers. By pairing them using the <code>&lt;label&gt;</code>'s {{htmlattrxref("for", "label")}} attribute, you bond the label to the input in a way that lets screen readers describe inputs to users more precisely.</p>

<p>It does not suffice to have plain text adjacent to the <code>&lt;input&gt;</code> element,. Rather, usability and accessibility requires the inclusion of either implicit or explicit {{HTMLElement("label")}}:</p>

<pre class="brush: html">&lt;!-- inaccessible --&gt;
&lt;p&gt;Enter your name: &lt;input id="name" type="text" size="30"&gt;&lt;/p&gt;

&lt;!-- implicit label --&gt;
&lt;p&gt;&lt;label&gt;Enter your name: &lt;input id="name" type="text" size="30"&gt;&lt;/label&gt;&lt;/p&gt;

&lt;!-- explicit label --&gt;
&lt;p&gt;&lt;label for="name"&gt;Enter your name: &lt;/label&gt;&lt;input id="name" type="text" size="30"&gt;&lt;/p&gt;</pre>

<p>The first example is inaccessible: no relationship exists between the prompt and the <code>&lt;input&gt;</code> element.</p>

<p>In addition to an accessible name, the label provides a larger 'hit' area for mouse and touch screen users to click on or touch. By pairing a <code>&lt;label&gt;</code> with an <code>&lt;input&gt;</code>, clicking on either one will focus the <code>&lt;input&gt;</code>. If you use plain text to "label" your input, this won't happen. Having the prompt part of the activation area for the input is helpful for people with motor control conditions.</p>

<p>As web developers, it's important that we never assume that people will know all the things that we know. The diversity of people using the web—and by extension your website—practically guarantees that some of your site's visitors will have some variation in thought processes and/or circumstances that leads them to interpret your forms very differently from you without clear and properly-presented labels.</p>

<h4 id="Placeholders_are_not_accessible">Placeholders are not accessible</h4>

<p>The {{htmlattrxref("placeholder", "input", "", 1)}} attribute lets you specify text that appears within the <code>&lt;input&gt;</code> element's content area itself when it is empty. The placeholder should never be required to understand your forms. It is not a label, and should not be used as a substitute, because it isn't. The placeholder is used to provide a hint as to what an inputted value should look like, not an explanation or prompt.</p>

<p>Not only is the placeholder not accessible to screen readers, but once the user enters any text into the form control, or if the form control already has a value, the placeholder disappears. Browsers with automatic page translation features may skip over attributes when translating, meaning the <code>placeholder</code> may not get translated.</p>

<div class="notecard note">
<p><strong>Note:</strong> Don't use the {{htmlattrxref("placeholder", "input", "", 1)}} attribute if you can avoid it. If you need to label an <code>&lt;input&gt;</code> element, use the {{HTMLElement("label")}} element.</p>
</div>

<h3 id="Client-side_validation">Client-side validation</h3>

<div class="notecard warning">
<p><strong>Warning:</strong> Client-side validation is useful, but it does <em>not</em> guarantee that the server will receive valid data. If the data must be in a specific format, <em>always</em> verify it also on the server-side, and return a <a href="/en-US/docs/Web/HTTP/Status/400"><code>400</code> HTTP response</a> if the format is invalid.</p>
</div>

<p>In addition to using CSS to style inputs based on the {{cssxref(":valid")}} or {{cssxref(":invalid")}} UI states based on the current state of each input, as noted in the {{anch('UI pseudo-classes')}} section above, the browser provides for client-side validation on (attempted) form submission. On form submission, if there is a form control that fails constraint validation, supporting browsers will display an error message on the first invalid form control; displaying a default message based on the error type, or a message set by you.</p>

<p>Some input types and other attributes place limits on what values are valid for a given input. For example, <code>&lt;input type="number" min="2" max="10" step="2"&gt;</code> means only the number 2, 4, 6, 8, or 10 are valid. Several errors could occur, including a <code>rangeUnderflow</code> error if the value is less than 2, <code>rangeOverflow</code> if greater than 10, <code>stepMismatch</code> if the value is a number between 2 and 10, but not an even integer (does not match the requirements of the <code>step</code> attribute), or <code>typeMismatch</code> if the value is not a number.</p>

<p>For the input types whose domain of possible values is periodic (that is, at the highest possible value, the values wrap back around to the beginning rather than ending), it's possible for the values of the {{htmlattrxref("max", "input", "", 1)}} and {{htmlattrxref("min", "input", "", 1)}} properties to be reversed, which indicates that the range of permitted values starts at <code>min</code>, wraps around to the lowest possible value, then continues on until <code>max</code> is reached. This is particularly useful for dates and times, such as when you want to allow the range to be from 8 PM to 8 AM:</p>

<pre class="brush: html">&lt;input type="time" min="20:00" max="08:00" name="overnight"&gt;</pre>

<p>Specific attributes and their values can lead to a specific error {{domxref('ValidityState')}}:</p>

<table class="no-markdown">
 <caption>Validity object errors depend on the {{htmlelement('input')}} attributes and their values:</caption>
 <thead>
  <tr>
   <th scope="col">Attribute</th>
   <th scope="col">Relevant property</th>
   <th scope="col">Description</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{ htmlattrxref("max", "input", "", 1)}}</td>
   <td>{{domxref('validityState.rangeOverflow')}}</td>
   <td>Occurs when the value is greater than the maximum value as defined by the <code>max</code> attribute</td>
  </tr>
  <tr>
   <td>{{ htmlattrxref("maxlength", "input", "", 1)}}</td>
   <td>{{domxref('validityState.tooLong')}}</td>
   <td>Occurs when the number of characters is greater than the number allowed by the <code>maxlength</code> property</td>
  </tr>
  <tr>
   <td>{{ htmlattrxref("min", "input", "", 1)}}</td>
   <td>{{domxref('validityState.rangeUnderflow')}}</td>
   <td>Occurs when the value is less than the minimum value as defined by the <code>min</code> attribute</td>
  </tr>
  <tr>
   <td>{{ htmlattrxref("minlength", "input", "", 1)}}</td>
   <td>{{domxref('validityState.tooShort')}}</td>
   <td>Occurs when the number of characters is less than the number required by the <code>minlength</code> property</td>
  </tr>
  <tr>
   <td>{{ htmlattrxref("pattern", "input", "", 1)}}</td>
   <td>{{domxref('validityState.patternMismatch')}}</td>
   <td>Occurs when a pattern attribute is included with a valid regular expression and the <code>value</code> does not match it.</td>
  </tr>
  <tr>
   <td>{{ htmlattrxref("required", "input", "", 1)}}</td>
   <td>{{domxref('validityState.valueMissing')}}</td>
   <td>Occurs when the <code>required</code> attribute is present but the value is <code>null</code> or radio or checkbox is not checked.</td>
  </tr>
  <tr>
   <td>{{ htmlattrxref("step", "input", "", 1)}}</td>
   <td>{{domxref('validityState.stepMismatch')}}</td>
   <td>The value doesn't match the step increment. Increment default is <code>1</code>, so only integers are valid on<code> type="number"</code> is step is not included. <code>step="any"</code> will never throw this error.</td>
  </tr>
  <tr>
   <td>{{ htmlattrxref("type", "input", "", 1)}}</td>
   <td>{{domxref('validityState.typeMismatch')}}</td>
   <td>Occurs when the value is not of the correct type, for example a email does not contain an <code>@</code> or a url doesn't contain a protocol.</td>
  </tr>
 </tbody>
</table>

<p>If a form control doesn't have the <code>required</code> attribute, no value, or an empty string, is not invalid. Even if the above attributes are present, with the exception of <code>required</code>, and empty string will not lead to an error.</p>

<p>We can set limits on what values we accept, and supporting browsers will natively validate these form values and alert the user if there is a mistake when the form is submitted.</p>

<p>In addition to the errors described in the table above, the <code>validityState</code> interface contains the <code>badInput</code>, <code>valid</code>, and <code>customError</code> boolean readonly properties. The validity object includes:</p>

<ul>
 <li>{{domxref('validityState.valueMissing')}}</li>
 <li>{{domxref('validityState.typeMismatch')}}</li>
 <li>{{domxref('validityState.patternMismatch')}}</li>
 <li>{{domxref('validityState.tooLong')}}</li>
 <li>{{domxref('validityState.tooShort')}}</li>
 <li>{{domxref('validityState.rangeUnderflow')}}</li>
 <li>{{domxref('validityState.rangeOverflow')}}</li>
 <li>{{domxref('validityState.stepMismatch')}}</li>
 <li>{{domxref('validityState.badInput')}}</li>
 <li>{{domxref('validityState.valid')}}</li>
 <li>{{domxref('validityState.customError')}}</li>
</ul>

<p>For each of these Boolean properties, a value of <code>true</code> indicates that the specified reason validation may have failed is true, with the exception of the <code>valid</code> property, which is <code>true</code> if the element's value obeys all constraints.</p>

<p>If there is an error, supporting browsers will both alert the user and prevent the form from being submitted. A word of caution: if a custom error is set to a truthy value (anything other than the empty string or <code>null</code>), the form will be prevented from being submitted. If there is no custom error message, and none of the other properties return true, <code>valid</code> will be true, and the form can be submitted.</p>

<pre class="brush: js">function validate(input) {
  let validityState_object = input.validity;
  if(validityState_object.valueMissing) {
     input.setCustomValidity('A value is required');
  } else if (input.rangeUnderflow) {
    input.setCustomValidity('Your value is too low');
  } else if (input.rangeOverflow) {
    input.setCustomValidity('Your value is too high');
  } else {
    input.setCustomValidity('');
  }
}</pre>

<p>The last line, setting the custom validity message to the error string is vital. If the user makes an error, and the validity is set, it will fail to submit, even if all of the values are valid, until the message is <code>null</code>.</p>

<h4>Custom validation error example</h4>

<p>If you want to present a custom error message when a field fails to validate, you need to use the <a href="/en-US/docs/Web/API/Constraint_validation#constraint_validation_interfaces">Constraint validation features</a> available on <code>&lt;input&gt;</code> (and related) elements. Take the following form:</p>

<pre class="brush: html">&lt;form&gt;
  &lt;label for="name"&gt;Enter username (upper and lowercase letters): &lt;/label&gt;
  &lt;input type="text" name="name" id="name" required pattern="[A-Za-z]+"&gt;
  &lt;button&gt;Submit&lt;/button&gt;
&lt;/form&gt;</pre>

<p>The basic HTML form validation features will cause this to produce a default error message if you try to submit the form with either no valid filled in, or a value that does not match the <code>pattern</code>.</p>

<p>If you wanted to instead display custom error messages, you could use JavaScript like the following:</p>

<pre class="brush: js">const nameInput = document.querySelector('input');
const form = document.querySelector('form');

nameInput.addEventListener('input', () =&gt; {
  nameInput.setCustomValidity('');
  nameInput.checkValidity();
});

nameInput.addEventListener('invalid', () =&gt; {
  if(nameInput.value === '') {
    nameInput.setCustomValidity('Enter your username!');
  } else {
    nameInput.setCustomValidity('Usernames can only contain upper and lowercase letters. Try again!');
  }
});</pre>

<p>The example renders like so:</p>

<p>{{EmbedLiveSample('Custom_validation_error_example')}}</p>

<p>In brief:</p>

<ul>
 <li>We check the valid state of the input element every time its value is changed by running the <code>checkValidity()</code> method via the <code>input</code> event handler.</li>
 <li>If the value is invalid, an <code>invalid</code> event is raised, and the <code>invalid</code> event handler function is run. Inside this function we work out whether the value is invalid because it is empty, or because it doesn't match the pattern, using an <code>if()</code> block, and set a custom validity error message.</li>
 <li>As a result, if the input value is invalid when the submit button is pressed, one of the custom error messages will be shown.</li>
 <li>If it is valid, it will submit as you'd expect. For this to happen, the custom validity has to be cancelled, by invoking <code>setCustomValidity()</code> with an empty string value. We therefore do this every time the <code>input</code> event is raised. If you don't do this, and a custom validity was previously set, the input will register as invalid, even if it current contains a valid value on submission.</li>
</ul>

<div class="notecard note">
<p><strong>Note:</strong> Always validate input constraints both client side and server side. Constraint validation doesn't remove the need for validation on the <em>server side</em>. Invalid values can still be sent by older browsers or by bad actors.</p>
</div>

<div class="notecard note">
<p><strong>Note:</strong> Firefox supported a proprietary error attribute — <code>x-moz-errormessage</code> — for many versions, which allowed you set custom error messages in a similar way. This has been removed as of version 66 (see {{bug(1513890)}}).</p>
</div>

<h3 id="Localization">Localization</h3>

<p>The allowed inputs for certain <code>&lt;input&gt;</code> types depend on the locale. In some locales, 1,000.00 is a valid number, while in other locales the valid way to enter this number is 1.000,00.</p>

<p>Firefox uses the following heuristics to determine the locale to validate the user's input (at least for <code>type="number"</code>):</p>

<ul>
 <li>Try the language specified by a <code>lang</code>/<code>xml:lang</code> attribute on the element or any of its parents.</li>
 <li>Try the language specified by any <code>Content-Language</code> HTTP header. Or,</li>
 <li>If none specified, use the browser's locale.</li>
</ul>

<h3 id="Technical_summary">Technical summary</h3>

<table class="properties">
 <tbody>
  <tr>
   <th scope="row"><a href="/en-US/docs/Web/Guide/HTML/Content_categories">Content categories</a></th>
   <td><a href="/en-US/docs/Web/Guide/HTML/Content_categories#flow_content">Flow content</a>, listed, submittable, resettable, form-associated element, <a href="/en-US/docs/Web/Guide/HTML/Content_categories#phrasing_content">phrasing content</a>. If the {{htmlattrxref("type", "input")}} is not <code>hidden</code>, then labelable element, palpable content.</td>
  </tr>
  <tr>
   <th scope="row">Permitted content</th>
   <td>None, it is an {{Glossary("empty element")}}.</td>
  </tr>
  <tr>
   <th scope="row">Tag omission</th>
   <td>Must have a start tag and must not have an end tag.</td>
  </tr>
  <tr>
   <th scope="row">Permitted parents</th>
   <td>Any element that accepts <a href="/en-US/docs/Web/Guide/HTML/Content_categories#phrasing_content">phrasing content</a>.</td>
  </tr>
  <tr>
   <th scope="row">Implicit ARIA role</th>
   <td>
    <ul>
     <li><code>type=button</code>: <code><a href="/en-US/docs/Web/Accessibility/ARIA/Roles/button_role">button</a></code></li>
     <li><code>type=checkbox</code>: <code><a href="/en-US/docs/Web/Accessibility/ARIA/Roles/checkbox_role">checkbox</a></code></li>
     <li><code>type=email</code>
      <ul>
       <li>with no <code>list</code> attribute: <code><a href="/en-US/docs/Web/Accessibility/ARIA/Roles/textbox_role">textbox</a></code></li>
       <li>with <code>list</code> attribute: {{ARIARole("combobox")}}</li>
      </ul>
     </li>
     <li><code>type=image</code>: <code><a href="/en-US/docs/Web/Accessibility/ARIA/Roles/button_role">button</a></code></li>
     <li><code>type=number</code>: {{ARIARole("spinbutton")}}</li>
     <li><code>type=radio</code>: {{ARIARole("radio")}}</li>
     <li><code>type=range</code>: {{ARIARole("slider")}}</li>
     <li><code>type=reset</code>: <code><a href="/en-US/docs/Web/Accessibility/ARIA/Roles/button_role">button</a></code></li>
     <li><code>type=search</code>
      <ul>
       <li>with no <code>list</code> attribute: {{ARIARole("searchbox")}}</li>
       <li>with <code>list</code> attribute: {{ARIARole("combobox")}}</li>
      </ul>
     </li>
     <li><code>type=submit</code>: <code><a href="/en-US/docs/Web/Accessibility/ARIA/Roles/button_role">button</a></code></li>
     <li><code>type=tel</code>
      <ul>
       <li>with no <code>list</code> attribute: <code><a href="/en-US/docs/Web/Accessibility/ARIA/Roles/textbox_role">textbox</a></code></li>
       <li>with <code>list</code> attribute: {{ARIARole("combobox")}}</li>
      </ul>
     </li>
     <li><code>type=text</code>
      <ul>
       <li>with no <code>list</code> attribute: <code><a href="/en-US/docs/Web/Accessibility/ARIA/Roles/textbox_role">textbox</a></code></li>
       <li>with <code>list</code> attribute: {{ARIARole("combobox")}}</li>
      </ul>
     </li>
     <li><code>type=url</code>
      <ul>
       <li>with no <code>list</code> attribute: <code><a href="/en-US/docs/Web/Accessibility/ARIA/Roles/textbox_role">textbox</a></code></li>
       <li>with <code>list</code> attribute: {{ARIARole("combobox")}}</li>
      </ul>
     </li>
     <li><code>type=color|date|datetime-local|file|hidden|month|password|time|week</code>: <a href="https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role">no corresponding role</a></li>
    </ul>
   </td>
  </tr>
  <tr>
   <th scope="row">Permitted ARIA roles</th>
   <td>
    <ul>
     <li><code>type=button</code>: {{ARIARole("link")}}, {{ARIARole("menuitem")}}, {{ARIARole("menuitemcheckbox")}}, {{ARIARole("menuitemradio")}}, {{ARIARole("option")}}, {{ARIARole("radio")}}, {{ARIARole("switch")}}, {{ARIARole("tab")}}</li>
     <li><code>type=checkbox</code>: {{ARIARole("button")}} when used with <code>aria-pressed</code>, {{ARIARole("menuitemcheckbox")}}, {{ARIARole("option")}}, {{ARIARole("switch")}}</li>
     <li><code>type=image</code>: {{ARIARole("link")}}, {{ARIARole("menuitem")}}, {{ARIARole("menuitemcheckbox")}}, {{ARIARole("menuitemradio")}}, {{ARIARole("radio")}}, {{ARIARole("switch")}}</li>
     <li><code>type=radio</code>: {{ARIARole("menuitemradio")}}</li>
     <li><code>type=text</code> with no <code>list</code> attribute: {{ARIARole("combobox")}}, {{ARIARole("searchbox")}}, {{ARIARole("spinbutton")}}</li>
     <li><code>type=color|date|datetime|datetime-local|email|file|hidden|month|number|password|range|reset|search|submit|tel|url|week</code> or <code>text</code> with <code>list</code> attribute: no <code>role</code> permitted</li>
    </ul>
   </td>
  </tr>
  <tr>
   <th scope="row">DOM interface</th>
   <td>{{domxref("HTMLInputElement")}}</td>
  </tr>
 </tbody>
</table>

<h2 id="Accessibility_concerns">Accessibility concerns</h2>

<h3 id="Labels_2">Labels</h3>

<p>When including inputs, it is an accessibility requirement to add labels along side. This is needed so those who use assistive technologies can tell what the input is for. Also, clicking or touching a label gives focus to the label's associated form control. This improves the accessibility and usability for sighted users, increases the area a user can click or touch to activate the form control. This is especially useful (and even needed) for radio buttons and checkboxes, which are tiny. For more information about labels in general see {{anch("Labels")}} .</p>

<p>The following is an example of how to associate the <code>&lt;label&gt;</code> with an <code>&lt;input&gt;</code> element in the above style. You need to give the <code>&lt;input&gt;</code> an <code>id</code> attribute. The <code>&lt;label&gt;</code> then needs a <code>for</code> attribute whose value is the same as the input's <code>id</code>.</p>

<pre class="brush: html">&lt;label for="peas"&gt;Do you like peas?&lt;/label&gt;
&lt;input type="checkbox" name="peas" id="peas"&gt;
</pre>

<h3 id="Size">Size</h3>

<p>Interactive elements such as form input should provide an area large enough that it is easy to activate them. This helps a variety of people, including people with motor control issues and people using non-precise forms of input such as a stylus or fingers. A minimum interactive size of 44×44 <a href="https://www.w3.org/TR/WCAG21/#dfn-css-pixels">CSS pixels</a> is recommended.</p>

<ul>
 <li><a href="https://www.w3.org/WAI/WCAG21/Understanding/target-size.html">Understanding Success Criterion 2.5.5: Target Size | W3C Understanding WCAG 2.1</a></li>
 <li><a href="https://adrianroselli.com/2019/06/target-size-and-2-5-5.html">Target Size and 2.5.5 | Adrian Roselli</a></li>
 <li><a href="https://www.a11yproject.com/posts/2018-11-21-large-touch-targets/">Quick test: Large touch targets - The A11Y Project</a></li>
</ul>

<h2 id="Specifications">Specifications</h2>

<p>{{Specifications}}</p>

<h2 id="Browser_compatibility">Browser compatibility</h2>

<p>{{Compat}}</p>

<h2 id="See_also">See also</h2>

<ul>
 <li><a href="/en-US/docs/Web/Guide/HTML/Constraint_validation">Form constraint validation</a></li>
 <li><a href="/en-US/docs/Learn/Forms/Your_first_form">Your first HTML form</a></li>
 <li><a href="/en-US/docs/Learn/Forms/How_to_structure_a_web_form">How to structure an HTML form</a></li>
 <li><a href="/en-US/docs/Learn/Forms/Basic_native_form_controls">The native form widgets</a></li>
 <li><a href="/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data">Sending form data</a></li>
 <li><a href="/en-US/docs/Learn/Forms/Form_validation">Form data validation</a></li>
 <li><a href="/en-US/docs/Learn/Forms/How_to_build_custom_form_controls">How to build custom form widgets</a></li>
 <li><a href="/en-US/docs/Learn/Forms/HTML_forms_in_legacy_browsers">HTML forms in legacy browsers</a></li>
 <li><a href="/en-US/docs/Learn/Forms/Styling_web_forms">Styling HTML forms</a></li>
 <li><a href="/en-US/docs/Learn/Forms/Advanced_form_styling">Advanced styling for HTML forms</a></li>
 <li><a href="/en-US/docs/Learn/Forms/Property_compatibility_table_for_form_controls">CSS property compatibility table</a></li>
</ul>