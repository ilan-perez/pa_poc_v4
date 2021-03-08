---
heading: Dashboard
sub_heading: "..."
show_footer_cta: true
title: Dashboard
banner_image: ''
hero_button:
  text: ''
  href: ''
page_sections:
- template: textarea
  textarea: "    <style>\n    \n    \n     \n        \n      .gatewayNew  .butt{\n
    \   \n    \n            text-align: left;\n            padding: 4px;\n            margin-right:
    3px;\n            cursor: pointer;\n          line-height: 20px;\n          display:
    inline-flex;\n    \n        }\n    \n     .gatewayNew   .img {\n            vertical-align:
    text-bottom;\n        }\n    \n      .gatewayNew  .customer {\n            margin-bottom:
    10px;\n            border-bottom: 1px solid #b2b2b2;\n            margin-bottom:
    30px;\n        }\n    \n     .gatewayNew   .prov {\n            background-color:rgb(220,
    242, 255)\n        }\n    \n     .gatewayNew  .exp {\n            background-color:rgb(255,
    234, 234)\n        }\n    \n      .gatewayNew  .test {\n            background-color:rgb(215,
    255, 198)\n        }\n    \n       .gatewayNew  .dev {\n            background-color:rgb(243,
    211, 255)\n    \n        }\n    \n    \n      .gatewayNew  .def {\n          background-color:
    rgb(255, 235, 178);\n        }\n    \n    .gatewayNew   .pending {\n           background-color:
    #f0ffff;\n        }\n    \n    \n    .gatewayNew .licenseOverview .box .boxValue
    {\n        line-height: normal;\n    }\n    \n    .pLics{ margin-top: 30px;}\n
    \   \n    .gatewayNew .licenseOverview .box {\n        width: 96px;\n    }\n    \n
    \   .box .machineName{ text-align: left;width: 100%;display: inline-block;}\n
    \   .gatewayNew .gatewayContent a{\n        color:#000000;\n        display:block;\n
    \       width: 180px;   \n        margin: 0px auto 10px auto;\n        text-align:left;\n
    \   }\n    .gatewayNew .gatewayContent a::before{\n        margin-right:5px;\n
    \       content:url(\"/jquery-ui-1.12.1.custom/arrow2.png\");\n        float:left;\n
    \   }\n    \n    .gatewayNew .gatewayContent a.noafter::before{\n        content:none;\n
    \   }\n    \n    .gatewayNew .gatewayContent .dashHeading{\n        line-height:
    50px; font-size: 14px; width: 180px; \n        margin: 0px auto 10px auto;\n        height:55px;\n
    \       border-bottom:1px solid #b1b1b1;\n        \n        \n    }\n    .innerHeading{\n
    \       text-align:center;\n        padding:0 18%;\n    }\n        .innerHeading
    span {\n            display:inline-block;\n            height:50px;\n            float:left;\n
    \       }\n        .innerHeading img{\n            display:inline-block;\n            float:left;\n
    \       }\n    </style>\n    \n    \n     <script>\n          var currentUrl =
    (location.pathname + location.search).substr(1);\n          LoggedInCheck(readCookie('CustomerId'),
    readCookie('ContactId'), currentUrl, \"/login/\");\n     </script>\n    \n    <div
    class=\"gatewayNew\">\n        <div class=\"\" style=\"float: left; width: 100%\">\n
    \           <div class=\"gatewayMenu\">\n                <ul>\n                 \n
    \                   <li class=\"menuOn\"><a href=\"/gateway/overview\">Dashboard</a></li>\n
    \                 <li ><a href=\"/gateway/licenses\">Licenses</a></li>\n                    <li
    class=\"myorders\"><a href=\"/gateway/orders\">Open Orders</a></li>\n                    <li
    ><a href=\"/gateway/profile\">Profile</a></li>\n                    <li ><a href=\"/gateway/buy\">Buy</a></li>\n
    \                   <li><a href=\"/gateway/application-downloads\">Downloads</a></li>\n
    \                   <li><a href=\"/gateway/kubernetes\">Kubernetes</a></li>\n
    \                   <li><a href=\"/logout\">Logout</a></li>\n    \n    \n                </ul>\n
    \   \n    \n    \n            </div>\n            <div class=\"gatewayContent\">\n
    \               <div class=\"licenseOverview\">\n                 \n                    \n
    \                   \n                  <div class=\"sf_cols\">\n        <div
    class=\"sf_colsOut sf_4cols_1_25\">\n            <div id=\"cphMain_C031_Col00\"
    class=\"sf_colsIn sf_4cols_1in_25\">\n                            <div class=\"dashHeading\"><div
    class=\"innerHeading\"><img src=\"/jquery-ui-1.12.1.custom/buy.png\" /> <span
    style=\"\">Buy</span></div></div>\n                <div style=\"clear:both\"></div>\n
    \                           <a href=\"/gateway/orders\" class=\" \" >I have an
    order</a>\n                            <a href=\"/gateway/buy/license-wizard\"
    class=\" \" >License Upgrade</a>\n                \n                            <a
    href=\"/gateway/licenses\" class=\" \" >License Renewal</a>\n                \n
    \               \n            </div>\n        </div>\n        <div class=\"sf_colsOut
    sf_4cols_2_25\">\n            <div id=\"cphMain_C031_Col01\" class=\"sf_colsIn
    sf_4cols_2in_25\">  \n                 <div class=\"dashHeading\"><div class=\"innerHeading\"><img
    src=\"/jquery-ui-1.12.1.custom/contact.png\"/> <span style=\"\">Contact</span>
    </div></div>\n                <div style=\"clear:both\"></div>\n                <a
    href=\"https://support.pyramidanalytics.com/hc/en-us\" class=\" \" target=\"_blank\">
    Contact Support</a>\n               <a href=\"/free-trial/request-demo\" class=\"\"
    style=\"\">Schedule Demo</a>\n                \n                <a href=\"/gateway/edit-profile\"
    class=\" \"  style=\"width: 180px;  margin: 0px auto 20px auto\">Profile Update</a>\n
    \           </div>\n        </div>\n        <div class=\"sf_colsOut sf_4cols_3_25\">\n
    \           <div id=\"cphMain_C031_Col02\" class=\"sf_colsIn sf_4cols_3in_25\">\n
    \               <div class=\"dashHeading\"><div class=\"innerHeading\"><img src=\"/jquery-ui-1.12.1.custom/help.png\"
    /> <span style=\"\">Help</span> </div></div>\n                 <div style=\"clear:both\"></div>\n
    \                   <a href=\"https://help.pyramidanalytics.com/Content/Root/general/Welcome.htm\"
    class=\" \" target=\"_blank\" >Online help</a>\n    \n                <a href=\"https://help.pyramidanalytics.com/Content/Root/Guides/installation/Installer%20Overview.htm\"
    class=\" \" target=\"_blank\">Installation Guide</a>\n                \n                \n
    \               <a href=\"#\" class=\" \" target=\"_blank\"  id=\"forumLink\"
    >Community Forum Login</a>\n                \n                \n                \n
    \           </div>\n        </div>\n        <div class=\"sf_colsOut sf_4cols_4_25\">\n
    \           <div id=\"cphMain_C031_Col03\" class=\"sf_colsIn sf_4cols_4in_25\">\n
    \                          <div class=\"dashHeading\" style=\" margin-bottom:0;\"><div
    class=\"innerHeading\"><img src=\"/jquery-ui-1.12.1.custom/downloads.png\" style=\"display:inline;\"/>
    <span style=\"\">Download</span> </div></div>\n                <div style=\"clear:both\"></div>\n
    \               \n                        \n                \n                <a
    href=\"/gateway/application-downloads\" class=\"\"  style=\"width: 180px;  padding:
    12px 5px 0px 5px; margin: 0px auto 0px auto;  \">Latest Software</a>\n         \n
    \                           <a id=\"\" href=\"https://play.google.com/store/apps/details?id=pyramid.analytics\"
    \ class=\"\" style=\"    padding: 10px 5px 10px 5px;\"><img style=\"width:16px;
    float:left;\" src=\"https://www.pyramidanalytics.com/images/default-source/pyramid-2020/google77bf9b4e7dd26215b1eeff00002b9892.svg?sfvrsn=cc6df9c9_2\"
    alt=\"google\"/> <span style=\" display: inline-block;\n        height: 16px;
    float: left; line-height:16px; margin-left:10px; \">Google Play</span></a>\n                     <a
    id=\"\" href=\"https://itunes.apple.com/app/id1355475947\"  class=\"\" style=\"
    \    padding: 10px 5px 10px 5px;\"><img style=\"width:16px; float:left;\" src=\"https://www.pyramidanalytics.com/images/default-source/pyramid-2020/apple61bf9b4e7dd26215b1eeff00002b9892.svg?sfvrsn=cf6df9c9_2\"
    alt=\"apple\"/> <span style=\" display: inline-block;\n        height: 16px; float:
    left; line-height:16px; margin-left:10px; \">Apple Store</span></a>\n           <a
    id=\"\" href=\"/gateway/kubernetes\"  class=\"\" style=\"     padding: 10px 5px
    0px 5px;\"><img  style=\"width:16px; float:left;\" src=\"https://www.pyramidanalytics.com/images/default-source/pyramid-2020/kubernetes.svg?sfvrsn=cd6df9c9_2\"
    alt=\"kubernetes\"/> <span style=\" display: inline-block;\n        height: 16px;
    float: left; line-height:16px; margin-left:10px; \">Kubernetes Setup</span></a>\n
    \          \n                \n            </div>\n        </div>\n    </div>\n
    \                 \n    \n                </div>\n    \n            </div>\n    \n
    \       </div>\n        <div class=\"spacer\" style=\"clear: both;\"></div>\n
    \   </div>\n    \n    \n    \n    <div id=\"dialog-message\" title=\"Load your
    order\">\n       <div style=\"margin-bottom: 10px; font-size: 14px; \">Please
    enter the Order # you received</div>\n       \n    \t\t\t  <div style=\"margin-bottom:
    10px; font-size: 14px; \">Order Id</div>\n    \t\t\t\t    <input id=\"quoteid\"
    class=\"good_input\" style=\"background: #f2f2f2; color: #626262;\" name=\"\"
    type=\"text\" placeholder=\"00000000-0000-0000-0000-000000000000\" />\n    </div>\n
    \   \n    \n    <script type=\"text/javascript\">\n    \n    \n        \n    \n
    \   \n    \n    \n       \n    \n        function getForumLink() {\n            var
    customerId = readCookie('CustomerId');\n            var contactId = readCookie('ContactId');\n
    \   \n            var quoteString = \"customerId=\" + customerId + \"&contactId=\"
    + contactId;\n    \n            serviceGet(quoteString, '<%=ConfigurationManager.AppSettings[\"restServicApiURL\"]%>/ForumbeeSsoLink',
    function (data) {\n              //  alert(data);\n                $(\"#forumLink\").attr('href',data);\n
    \               //  alert(data);\n            });\n        }\n    \n        $(document).ready(function
    () {\n    \n            getForumLink();\n    \n            var ut = readCookie(\"userType\");\n
    \           \n    \n            $(\"#loadOrder\").button().on(\"click\", function
    () {\n    \n                $(\"#dialog-message\").dialog(\"open\");\n    \n            });\n
    \   \n            $(\"#dialog-message\").dialog({\n                resizable:
    false,\n                height: \"auto\",\n                autoOpen: false,\n
    \               modal: true,\n                width: 450,\n                //
    \ dialogClass: \"no-close\",\n                overlay:\n                    {\n
    \                       opacity: 0.5,\n                        background: \"black\"\n
    \                   },\n                open: function () {\n    \n                    //
    $(\".info\").html($(this).data('downloadId'));\n                },\n                buttons:
    [\n                    {\n                        text: \"Checkout\",\n                        \"class\":
    \"btn btn_orange\",\n                        click: function () {\n                            window.location
    = \"/gateway/buy?eqid=\" + $(\"#quoteid\").val();\n    \n    \n    \n    \n    \n
    \                       }\n                    },\n    \n                ]\n    \n
    \   \n            });\n         \n            \n    \n            $(\"#getQuote\").click(function
    () {\n                window.location = \"/gateway/buy?eqid=\"+$(\"#quoteid\").val();\n
    \           });\n    \n            \n      \n    \n    \n        });\n    \n    \n
    \   </script>\n    \n    \n    \n    \n    "
published: false

---
