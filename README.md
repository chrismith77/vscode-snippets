# Email UI - Code Snippets
*These snippets use the current Email UI best practice techniques. If you'd like to add additional snippets you can use this [snippets generator](https://snippet-generator.app/) site to help convert your code to the proper snippet format. **Please** add both Sublime Text and VS Code versions.*

# Table of Contents
 1. [Installation](#markdown-header-installation)
 2. [Conditionals](#markdown-header-conditionals)
 3. [CTAs](#markdown-header-ctas)
 4. [Images](#markdown-header-images)
 5. [Layouts](#markdown-header-layouts)

---
## Installation
Both Sublime Text 3 and VS Code versions of each are available.

#### Sublime Text 3 Installation
Clone this repo into your ST3 User Packages location. The location path should look similar to:
##### PC Path
```
C:\Users\<username>\AppData\Roaming\Sublime Text 3\Packages\User
```
##### Mac Path
```
~/Library/Application Support/Sublime Text 3/Packages/User
```
Once installed all you need to do to use the snippets is type the **Tab Trigger** text in the file you're working in and hit tab.

#### VS Code Installation
Clone this repo into your VSCode User location. The location path should look similar to:
*Do not change the name of the repo, VSCode looks for the "snippets" folder for the snippets file*
##### PC Path
```
C:\Users\<username>\AppData\Roaming\Code\User
```
##### Mac Path
```
~/Library/Application Support/Code/User
```
Once installed all you need to do to use the snippets is type the **Tab Trigger** text in the file you're working in and hit tab.

---
## Elements

##### Button - Standard
*This is the standard button code for a ghost or solid button.*

**Tab Trigger:** `btn_standard`
```html
<table border="0" cellpadding="0" cellspacing="0" role="presentation">
  <tr>
    <td class="cta-btn" align="center">
      <a href="#tbd" alias="CTA_Btn" target="_blank" style="background-color: #ed553b; border: 1px solid #ed553b; color: #ffffff; display: inline-block; font-size: 14px; line-height: 1.2; padding: 12px 25px; text-decoration: none;">
        <span class="btn-text">
          Cta Button
        </span>
      </a>
    </td>
  </tr>
</table>
```

##### Image - Responsive
*This is the standard code to ensure the image is responsive.*

**Tab Trigger:** `image_responsive`
```html
<img src="https://via.placeholder.com/640x200/f5f5f5/cacaca?text=640+x+Variable" alt="Image Alt" width="640" style="border: 0; display: block; margin: 0; max-width: 640px; width: 100%;" />
```

#### Link - Text
*This is the standard text link code, the alias is needed for SFMC tracking.*

**Tab Trigger:** `link_text`
```html
<a href="#tbd" alias="" target="_blank" style="color: #cc0000; text-decoration: none;">Link Text</a>
```

##### Lorem ipsum - Large
*A double paragraph of lorem ipsum text.*
**Tab Trigger:** `ipsum_large`
```html
<p style="margin: 0 0 15px;">
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent convallis fermentum sapien vitae ultricies. Suspendisse sit amet arcu lacus. Aliquam mollis vitae enim vel facilisis. Pellentesque ultrices suscipit dolor, sed placerat ipsum placerat ac. Proin dictum in quam et gravida.
</p>
<p style="margin: 0 0 15px;">
  Phasellus iaculis sapien id sapien faucibus, auctor aliquet justo pellentesque. In consequat sem at turpis luctus dictum. Donec sit amet mi ut neque porttitor iaculis. Ut tincidunt nisi pretium laoreet lobortis. Morbi vitae tellus eget risus bibendum vulputate at in purus. Duis fringilla tortor sit amet varius porta.
</p>
```

##### Lorem ipsum - Small
*A single paragraph of lorem ipsum text.*
**Tab Trigger:** `ipsum_small`
```html
<p style="margin: 0 0 15px;">
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent convallis fermentum sapien vitae ultricies.
</p>
```

#### SFMC strings - Common
*Commonly used personalization strings.*

**Tab Trigger:** `sfmc_strings_common`
```html
# Date
Current day:   %%xtday%%
Current month: %%xtmonth%%
Current year:  %%xtyear%%
# Standard links
View online:         %%view_email_url%%
Forward to a friend: %%ftaf_url%%
Subscription center: %%subscription_center_url%%
Profile center:      %%profile_center_url%%
Unsubscribe center:  %%unsub_center_url%%
```

#### SFMC strings - Sender info
*Personalization strings specific to the sender.*

**Tab Trigger:** `sfmc_strings_sender`
```html
# Sender info
Business name:    %%member_busname%%
Physical address: %%member_addr%%
                  %%member_city%%
                  %%member_state%%
                  %%member_postalcode%%
                  %%member_country%%
```

#### SFMC strings - Subscriber info
*Personalization strings specific to the subscriber.*

**Tab Trigger:** `sfmc_strings_subscriber`
```html
# Subscriber info
Email address: %%emailaddr%%
First name:    %firstname%%
Last name:     %%lastname%%
```

---
## Layouts

#### Fixed width table
**Tab Trigger:** `tbl`
```html
<table border="0" cellpadding="0" cellspacing="0" role="presentation">
  <tr>
    <td align="center" style="width: 640px;">
      Contents
    </td>
  </tr>
</table>
```

#### Full width table
**Tab Trigger:** `tbl%`
```html
<table border="0" cellpadding="0" cellspacing="0" role="presentation" width="100%">
  <tr>
    <td align="center" style="padding: 0;">
      Contents
    </td>
  </tr>
</table>
```

#### Hybrid 2 Column
**Tab Trigger:** `hybrid_2`
```html
<table class="block-class" border="0" cellpadding="0" cellspacing="0" role="presentation" width="100%">
  <tr>
    <td class="stack-wrapper" align="center">
      <!--[if true]>
      <table border="0" cellpadding="0" cellspacing="0" role="presentation">
        <tr>
          <td align="center" valign="top" style="width: 300px;">
      <![endif]-->
            <div class="column">
              <table border="0" cellpadding="0" cellspacing="0" role="presentation" width="100%">
                <tr>
                  <td align="center">
                    Content
                  </td>
                </tr>
              </table>
            </div>
      <!--[if true]>
          </td>
          <td align="center" valign="top" style="width: 300px;">
      <![endif]-->
            <div class="column">
              <table border="0" cellpadding="0" cellspacing="0" role="presentation" width="100%">
                <tr>
                  <td align="center">
                    Content
                  </td>
                </tr>
              </table>
            </div>
      <!--[if true]>
          </td>
        </tr>
      </table>
      <![endif]-->
    </td>
  </tr>
</table>
```

#### Hybrid 3 Column
**Tab Trigger:** `hybrid_3`
```html
<table class="block-class" border="0" cellpadding="0" cellspacing="0" role="presentation" width="100%">
  <tr>
    <td class="stack-wrapper" align="center">
      <!--[if true]>
      <table border="0" cellpadding="0" cellspacing="0" role="presentation">
        <tr>
          <td align="center" valign="top" style="width: 200px;">
      <![endif]-->
            <div class="column">
              <table border="0" cellpadding="0" cellspacing="0" role="presentation" width="100%">
                <tr>
                  <td align="center">
                    Content
                  </td>
                </tr>
              </table>
            </div>
      <!--[if true]>
          </td>
          <td align="center" valign="top" style="width: 200px;">
      <![endif]-->
            <div class="column">
              <table border="0" cellpadding="0" cellspacing="0" role="presentation" width="100%">
                <tr>
                  <td align="center">
                    Content
                  </td>
                </tr>
              </table>
            </div>
      <!--[if true]>
          </td>
          <td align="center" valign="top" style="width: 200px;">
      <![endif]-->
            <div class="column">
              <table border="0" cellpadding="0" cellspacing="0" role="presentation" width="100%">
                <tr>
                  <td align="center">
                    Content
                  </td>
                </tr>
              </table>
            </div>
      <!--[if true]>
          </td>
        </tr>
      </table>
      <![endif]-->
    </td>
  </tr>
</table>
```

#### Hybrid 4 Column
**Tab Trigger:** `hybrid_4`
```html
<table class="block-class" border="0" cellpadding="0" cellspacing="0" role="presentation" width="100%">
  <tr>
    <td class="stack-wrapper" align="center">
      <!--[if true]>
      <table border="0" cellpadding="0" cellspacing="0" role="presentation">
        <tr>
          <td align="center" valign="top" style="width: 315px;">
      <![endif]-->
            <div class="column">
              <table border="0" cellpadding="0" cellspacing="0" role="presentation" width="100%">
                <tr>
                  <td align="center">
                    Content
                  </td>
                  <td style="width: 10px;">&nbsp;</td>
                  <td align="center">
                    Content
                  </td>
                </tr>
              </table>
            </div>
      <!--[if true]>
          </td>
          <td style="width: 10px;">&nbsp;</td>
          <td align="center" valign="top" style="width: 315px;">
      <![endif]-->
            <div class="column">
              <table border="0" cellpadding="0" cellspacing="0" role="presentation" width="100%">
                <tr>
                  <td align="center">
                    Content
                  </td>
                  <td style="width: 10px;">&nbsp;</td>
                  <td align="center">
                    Content
                  </td>
                </tr>
              </table>
            </div>
      <!--[if true]>
          </td>
        </tr>
      </table>
      <![endif]-->
    </td>
  </tr>
</table>
```

---
## MSO
*Everything you need to wrangle that pesky Outlook. Here's a handy [cheatsheet](https://litmus.com/community/learning/8-outlook-overview) full of other useful Outlook hackeries.*

### Conditionals
#### MSO conditional
*This conditional is used to target Outlook desktop versions 2000-Present.*

**Tab Trigger:** `mso_conditional`
```html
<!--[if true]>

<![endif]-->
```

#### MSO conditional - Specific versions
*This conditional is used to target a specific range of Outlook desktop versions.*

**Tab Trigger:** `mso_conditional_specific`
```html
<%#
  Options:
  Condition [
    lt  = less than
    gt  = greater than
    lte = less than or equal to
    gte = greater than or equal to
  ]

  Outlook Versions [
    9  = 2000
    10 = 2002
    11 = 2003
    12 = 2007
    14 = 2010
    15 = 2013
    16 = 2016+
  ]
%>
<!--[if gte mso 12]>

<![endif]-->
```

#### MSO conditional - Start table block
*This is the opening Outlook only table code block.*

**Tab Trigger:** `mso_conditional_start`
```html
<!--[if true]>
<table border="0" cellpadding="0" cellspacing="0" role="presentation">
  <tr>
    <td align="center" style="padding: 0; width: 640px;">
<![endif]-->
```

#### MSO conditional - End table block
*This is the closing Outlook only table code block.*

**Tab Trigger:** `mso_conditional_end`
```html
<!--[if true]>
    </td>
  </tr>
</table>
<![endif]-->
```

#### Not MSO conditional
*This conditional is used to bypass Outlook desktop versions 2000-Present.*

**Tab Trigger:** `!mso`
```html
<!--[if false]><!-->

<!--<![endif]--> 
```

### Elements
#### MSO background image
**Tab Trigger:** `mso_bg_image`
*Use this when you need to display background images in Outlook.*
```html
<table border="0" cellpadding="0" cellspacing="0" role="presentation">
  <tr>
    <td class="bgImage-wrapper" align="center" background="url" height="400" valign="top" style="background: url('url') top left / cover no-repeat #000000; background-size: cover; height: inherit; width: 640px;">
      <!--[if true]>
        <v:image xmlns:v="urn:schemas-microsoft-com:vml" fill="true" stroke="false" style="border: 0; display: inline-block; height: 400px; width: 640px;" src="url" />
          <v:rect xmlns:v="urn:schemas-microsoft-com:vml" fill="true" stroke="false" style="border: 0; display: inline-block; height: 400px; position: absolute; width: 640px;">
            <v:fill opacity="0%" color="#000000" />
              <v:textbox inset="0,0,0,0">
      <![endif]-->
                <div>
                  <table border="0" cellpadding="0" cellspacing="0" role="presentation" width="100%">
                    <tr>
                      <td height="400" align="center" valign="middle" style="height: 400px;">
                        Content
                      </td>
                    </tr>
                  </table>
                </div>
      <!--[if true]>
              </v:textbox>
            </v:fill>
          </v:rect>
        </v:image>
      <![endif]-->
    </td>
  </tr>
</table>
```

#### MSO button - Ghost pill shape 
*This button is built to work with Middleman. Some settings are adjusted automatically based off of the font size that you choose.*
**Tab Trigger:** `mso_btn_ghost_pill`
```html
<%
  # Button sizes
  btn_Width    = 200
  btnFont_Size = 20 # Even numbers are preferable
  # Aesthetics
  btnBorder_Color     = data.config.branding.colors[0]
  btnBorder_Radius    = btnFont_Size + 2
  btnBorder_Size      = 2
  btnFont_Color       = data.config.branding.colors[0]
  btnFont_LetterSpace = '0.05em'
  btnFont_Transform   = 'uppercase' # Options [capitalize, lowercase, uppercase], or leave blank
  btnFont_Weight      = 'normal' # Options [lighter, normal, bold, bolder, 100 - 900]
  # Conditional styles
  fontWeight = ''
  textTransform = ''
  if btnFont_Weight != 'normal'
    fontWeight = 'font-weight: ' + btnFont_Weight + '; '
  end
  if btnFont_Transform != ''
    textTransform = 'text-transform: ' + btnFont_Transform + '; '
  end
%>
<!--[if true]>
<v:roundrect xmlns:v="urn:schemas-microsoft-com:vml" xmlns:w="urn:schemas-microsoft-com:office:word", arcsize="50%" filled="false" strokecolor="<%= btnBorder_Color %>" strokeweight="<%= btnBorder_Size %>px" style="width: <%= btn_Width - (btnBorder_Size * 2) %>px;">
  <v:textbox inset="0, 0, 0, 0" style="mso-fit-shape-to-text: true;">
    <center style="line-height: <%= btnFont_Size - 2 %>px;">
<![endif]-->
      <a class="cta-btn" href="#tbd" alias="" target="_blank" style="border: <%= btnBorder_Size %>px solid <%= btnBorder_Color %>; border-radius: <%= btnBorder_Radius %>px; box-sizing: border-box; color: <%= btnFont_Color %>; display: inline-block; font-size: <%= btnFont_Size %>px; <%= fontWeight %>letter-spacing: <%= btnFont_LetterSpace %>; line-height: 1; max-width: <%= btn_Width %>px; padding: <%= (btnFont_Size / 2).round - 2 %>px 0; text-decoration: none; <%= textTransform %>width: 100%; mso-border-alt: none; mso-padding-alt: 0; mso-text-raise: -5px;">
        Button Text
      </a>
<!--[if true]>
   </center>
  </v:textbox>
</v:roundrect>
<![endif]-->
```

#### MSO button - Ghost rounded corners 
*This button is built to work with Middleman. Some settings are adjusted automatically based off of the font size that you choose.*
**Tab Trigger:** `mso_btn_ghost_pill`
```html
<%
  # Button sizes
  btn_Width    = 200
  btnFont_Size = 20 # Even numbers are preferable
  # Aesthetics
  btnBorder_Color     = data.config.branding.colors[0]
  btnBorder_Radius    = 8 # The radius should not exceed 3/4 of the font size
  btnBorder_Size      = 2
  btnFont_Color       = data.config.branding.colors[0]
  btnFont_LetterSpace = '0.05em'
  btnFont_Transform   = 'uppercase' # Options [capitalize, lowercase, uppercase], or leave blank
  btnFont_Weight      = 'normal' # Options [lighter, normal, bold, bolder, 100 - 900]
  # Conditional styles
  fontWeight = ''
  textTransform = ''
  if btnFont_Weight != 'normal'
    fontWeight = 'font-weight: ' + btnFont_Weight + '; '
  end
  if btnFont_Transform != ''
    textTransform = 'text-transform: ' + btnFont_Transform + '; '
  end
%>
<!--[if true]>
<v:roundrect xmlns:v="urn:schemas-microsoft-com:vml" xmlns:w="urn:schemas-microsoft-com:office:word", arcsize="<%= (btnBorder_Radius * 1.875).round %>%" filled="false" strokecolor="<%= btnBorder_Color %>" strokeweight="<%= btnBorder_Size %>px" style="width: <%= btn_Width - (btnBorder_Size * 2) %>px;">
  <v:textbox inset="0, 0, 0, 0" style="mso-fit-shape-to-text: true;">
    <center style="line-height: <%= (btnFont_Size * 1.65).round %>px;">
<![endif]-->
      <a class="cta-btn" href="#tbd" alias="" target="_blank" style="border: <%= btnBorder_Size %>px solid <%= btnBorder_Color %>; border-radius: <%= btnBorder_Radius %>px; box-sizing: border-box; color: <%= btnFont_Color %>; display: inline-block; font-size: <%= btnFont_Size %>px; <%= fontWeight %>letter-spacing: <%= btnFont_LetterSpace %>; line-height: 1; max-width: <%= btn_Width %>px; padding: <%= (btnFont_Size / 2).round - 2 %>px 0; text-decoration: none; <%= textTransform %>width: 100%; mso-border-alt: none; mso-padding-alt: 0; mso-text-raise: 2px;">
        Button Text
      </a>
<!--[if true]>
   </center>
  </v:textbox>
</v:roundrect>
<![endif]-->
```

#### MSO button - Solid pill shape
*This button is built to work with Middleman. Some settings are adjusted automatically based off of the font size that you choose.*
**Tab Trigger:** `mso_btn_ghost_pill`
```html
<%
  # Button sizes
  btn_Width    = 200
  btnFont_Size = 20 # Even numbers are preferable
  # Aesthetics
  btnBg_Color         = data.config.branding.colors[0]
  btnBorder_Radius    = btnFont_Size + 2
  btnBorder_Size      = 2
  btnFont_Color       = data.config.branding.colors[4]
  btnFont_LetterSpace = '0.05em'
  btnFont_Transform   = 'uppercase' # Options [capitalize, lowercase, uppercase], or leave blank
  btnFont_Weight      = 'normal' # Options [lighter, normal, bold, bolder, 100 - 900]
  # Conditional styles
  fontWeight = ''
  textTransform = ''
  if btnFont_Weight != 'normal'
    fontWeight = 'font-weight: ' + btnFont_Weight + '; '
  end
  if btnFont_Transform != ''
    textTransform = 'text-transform: ' + btnFont_Transform + '; '
  end
%>
<!--[if true]>
<v:roundrect xmlns:v="urn:schemas-microsoft-com:vml" xmlns:w="urn:schemas-microsoft-com:office:word", arcsize="50%" fillcolor="<%= btnBg_Color %>" strokecolor="<%= btnBg_Color %>" strokeweight="<%= btnBorder_Size %>px" style="width: <%= btn_Width - (btnBorder_Size * 2) %>px;">
  <v:textbox inset="0, 0, 0, 0" style="mso-fit-shape-to-text: true;">
    <center style="line-height: <%= btnFont_Size - 2 %>px;">
<![endif]-->
      <a class="cta-btn" href="#tbd" alias="" target="_blank" style="background-color: <%= btnBg_Color %>; border-radius: <%= btnBorder_Radius %>px; box-sizing: border-box; color: <%= btnFont_Color %>; display: inline-block; font-size: <%= btnFont_Size %>px; <%= fontWeight %>letter-spacing: <%= btnFont_LetterSpace %>; line-height: 1; max-width: <%= btn_Width %>px; padding: <%= (btnFont_Size / 2).round %>px 0; text-decoration: none; <%= textTransform %>width: 100%; mso-padding-alt: 0; mso-text-raise: -5px;">
        Button Text
      </a>
<!--[if true]>
   </center>
  </v:textbox>
</v:roundrect>
<![endif]-->
```

#### MSO button - Solid rounded corners
*This button is built to work with Middleman. Some settings are adjusted automatically based off of the font size that you choose.*
**Tab Trigger:** `mso_btn_ghost_pill`
```html
<%
  # Button sizes
  btn_Width    = 200
  btnFont_Size = 20 # Even numbers are preferable
  # Aesthetics
  btnBg_Color         = data.config.branding.colors[0]
  btnBorder_Radius    = 8 # The radius should not exceed 3/4 of the font size
  btnBorder_Size      = 2
  btnFont_Color       = data.config.branding.colors[4]
  btnFont_LetterSpace = '0.05em'
  btnFont_Transform   = 'uppercase' # Options [capitalize, lowercase, uppercase], or leave blank
  btnFont_Weight      = 'normal' # Options [lighter, normal, bold, bolder, 100 - 900]
  # Conditional styles
  fontWeight = ''
  textTransform = ''
  if btnFont_Weight != 'normal'
    fontWeight = 'font-weight: ' + btnFont_Weight + '; '
  end
  if btnFont_Transform != ''
    textTransform = 'text-transform: ' + btnFont_Transform + '; '
  end
%>
<!--[if true]>
<v:roundrect xmlns:v="urn:schemas-microsoft-com:vml" xmlns:w="urn:schemas-microsoft-com:office:word", arcsize="<%= (btnBorder_Radius * 1.875).round %>%" fillcolor="<%= btnBg_Color %>" strokecolor="<%= btnBg_Color %>" strokeweight="<%= btnBorder_Size %>px" style="width: <%= btn_Width - (btnBorder_Size * 2) %>px;">
  <v:textbox inset="0, 0, 0, 0" style="mso-fit-shape-to-text: true;">
    <center style="line-height: <%= (btnFont_Size * 1.65).round %>px;">
<![endif]-->
      <a class="cta-btn" href="#tbd" alias="" target="_blank" style="background-color: <%= btnBg_Color %>; border-radius: <%= btnBorder_Radius %>px; box-sizing: border-box; color: #ffffff; display: inline-block; font-size: <%= btnFont_Size %>px; <%= fontWeight %>letter-spacing: <%= btnFont_LetterSpace %>; line-height: 1; max-width: <%= btn_Width %>px; padding: <%= (btnFont_Size / 2).round %>px 0; text-decoration: none; <%= textTransform %>width: 100%; mso-padding-alt: 0; mso-text-raise: 2px;">
        Button Text
      </a>
<!--[if true]>
   </center>
  </v:textbox>
</v:roundrect>
<![endif]-->
```

---
## Utilities

#### SFMC AMPscript - Script tag
**Tab Trigger:** `sfmc_amp_script_tag`
```html
%%[/* AMPscript block title */]%%
<script runat="server" language="ampscript">
  
</script>
```

#### Show and Hide
**Tab Trigger:** `show_hide`
```html
<%# Desktop Content %>
<div class="desktop-content" style="display: none; height: 0; overflow: hidden;">
  <!-- dump whatever you need to show up on desktop in here | there's no need to style any of this content to try and hide it, the DIV takes care of that -->
</div>
<%# End Desktop Content %>

<%# Mobile Content %>
<!--[if false]><!-->
<div class="mobile-content">
  <!-- Dump whatever you need to show up on mobile in here -->
</div>
<!--<![endif]-->
<%# End Mobile Content %>
```