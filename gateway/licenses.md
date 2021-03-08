---
heading: Licenses
sub_heading: Engineering and Health Sciences
show_footer_cta: true
title: Licenses
banner_image: ''
hero_button:
  text: ''
  href: ''
page_sections: []
published: false

---
<%@ Control Language="C#" AutoEventWireup="true" CodeBehind="DisplayCustomerLicenses.ascx.cs" Inherits="SitefinityWebApp.UserControls.Gateway.DisplayCustomerLicenses" %>


<style>


 
    
  .gatewayNew  .butt{


        text-align: left;
        padding: 4px;
        margin-right: 3px;
        cursor: pointer;
      line-height: 20px;
      display: inline-flex;

    }

 .gatewayNew   .img {
        vertical-align: text-bottom;
    }

  .gatewayNew  .customer {
        margin-bottom: 10px;
        border-bottom: 1px solid #b2b2b2;
        margin-bottom: 30px;
    }

 .gatewayNew   .prov {
        background-color:rgb(220, 242, 255)
    }

 .gatewayNew  .exp {
        background-color:rgb(255, 234, 234)
    }

  .gatewayNew  .test {
        background-color:rgb(215, 255, 198)
    }

   .gatewayNew  .dev {
        background-color:rgb(243, 211, 255)

    }


  .gatewayNew  .def {
      background-color: rgb(255, 235, 178);
    }

.gatewayNew   .pending {
       background-color: #f0ffff;
    }


.gatewayNew .licenseOverview .box .boxValue {
    line-height: normal;
}

.pLics{ margin-top: 30px;}





.box .machineName{ text-align: left;width: 180px;display: inline-block;overflow: visible;}
.box2 { width: 50px;float: left; margin-left:6px;}
    .box2 .boxTitle {
        text-transform: none;
        color: #dfc592;
        height: 20px;
        font-size: 12px;
    }
.gatewayNew .licenseOverview .box{ border: none;}
        .readonly {
            background: transparent!important;
            border: 0 !important;
            color: #777777 !important;
            height: 20px !important;
            padding-left: 0px !important;
            width: 180px !important;
            float: left;
            margin-bottom: 0px!important;
        }

        .editable {
            background: #ffffff;
            border: 1px solid #cccccc;
            color: #000000;
            height: 20px;
            padding-left: 5px;
            width: 180px;
              margin-bottom: 0px!important;
        }

        

</style>


 <script>
      var currentUrl = (location.pathname + location.search).substr(1);
    LoggedInCheck(readCookie('CustomerId'), readCookie('ContactId'), currentUrl, "/login/");
 </script>

<div class="gatewayNew">
    <div class="" style="float: left; width: 100%">
        <div class="gatewayMenu">
            <ul>
                 
                <li ><a href="/gateway/overview">Dashboard</a></li>
              <li class="menuOn"><a href="/gateway/licenses">Licenses</a></li>
                <li class=""><a href="/gateway/orders">Open Orders</a></li>
                <li ><a href="/gateway/profile">Profile</a></li>
                <li ><a href="/gateway/buy">Buy</a></li>
                <li><a href="/gateway/application-downloads">Downloads</a></li>
                <li><a href="/gateway/kubernetes">Kubernetes</a></li>
                <li><a href="/logout">Logout</a></li>


            </ul>



        </div>
        <div class="gatewayContent">
            <div class="licenseOverview">
             
                
                  <div class="contactHeading">
                      <h3><i class="fa fa-key" aria-hidden="true"></i> License Overview</h3>

                    </div>
                    <div style="float: right;">
                   <a  id="go" class="btn btn_orange" style="color: #ffffff; ">I have an order</a>
                         
                <input type="button" id="trialJump" value="Get Trial" class="btn btn_green" style="width: 155px;"/>
                        <input type="button" id="betakeysJump" value="Get Beta Keys" class="btn " style="width: 155px; color: #ffffff; background: #000000; display: none;"/>
                    </div>
                 <div class="spacer" style="clear: both;"></div>
                <hr />
            
                <div class="noLicensesMessage" style="display: none;" >You currently have no licenses in your account. <br/><br /> You can either <a href="/gateway/buy">Buy</a> Seats or <a href="/gateway/application-downloads">Download</a> the community edition.</div>
            
                   <div class="cLics" style="display: none;">
                  <h4 style="color:gray">Current Licenses</h4>
                <div id="Licenses"></div>
                    </div>
                <div class="pLics" style="display: none;">
                <h4 style="color:gray">Licenses Pending Approval/Processing</h4>
                <div id="PendingLicenses"></div>
              </div>
              

            </div>

        </div>

    </div>
    <div class="spacer" style="clear: both;"></div>
</div>


<div id="dialog-message" title="Load your order">
   <div style="margin-bottom: 10px; font-size: 14px; ">Please enter the Order # you received</div>
   
			  <div style="margin-bottom: 10px; font-size: 14px; ">Order Id</div>
				    <input id="quoteid" class="good_input" style="background: #f2f2f2; color: #626262;" name="" type="text" placeholder="00000000-0000-0000-0000-000000000000" />
</div>


<div id="mk-message" title="Enter your machine key">
  <div style="margin-bottom: 10px; font-size: 14px; ">Your machine key is required to get your license keys</div>
   
			
				      <textarea  name="machinekey"   id="machinekey"  placeholder="Paste your machine key here" style="width: 410px; height: 80px; margin-bottom: 10px; background: #f2f2f2; color: #626262; font-size: 14px; "></textarea>
                          
                              <div id="ValidationComments" class="comment" style="font-size: 14px; padding: 3px 0px;  color:#b63128; display: none;  line-height: normal!important;"></div>

   <div style="font-size: 14px; color: #ababab;"> Need help finding your machine key? <a href="https://help.pyramidanalytics.com/Content/Root/Guides/installation/activation/New%0Deployments.htm" target="_blank">click here</a></div>
</div>


<div id="switch-message" title="Switching Server">
  <div style="margin-bottom: 10px; font-size: 14px; ">Paste your deactivation key below</div>
   
			
				      <textarea  name="machinekey"   id="deactkey"  placeholder="Paste your deactivation key here" style="width: 410px; height: 80px; margin-bottom: 10px; background: #f2f2f2; color: #626262; font-size: 14px; "></textarea>
                          
                              <div id="ValidationComments" class="comment" style="font-size: 14px; padding: 3px 0px;  color:#b63128; display: none;  line-height: normal!important;"></div>

    <div style="margin-bottom: 10px; font-size: 14px; ">Paste your NEW machine key below</div>
   
			
				      <textarea  name="machinekey"   id="newMachinekey"  placeholder="Paste your NEW machine key here" style="width: 410px; height: 80px; margin-bottom: 10px; background: #f2f2f2; color: #626262; font-size: 14px; "></textarea>
                          
                              <div id="ValidationComments" class="comment" style="font-size: 14px; padding: 3px 0px;  color:#b63128; display: none;  line-height: normal!important;"></div>


   <div style="font-size: 14px; color: #ababab;"> Need help finding your machine key? <a href="https://help.pyramidanalytics.com/Content/Root/Guides/installation/activation/New%0Deployments.htm" target="_blank">click here</a></div>
</div>


<div id="response-message" title="Action Status">
  
	<div id="genResponseComment" style="text-align: center;"></div>
</div>

<script type="text/javascript">

    var noCurrentlicensesFlag = false;
    var noPendinglicensesFlag = false;


    $("#go").on("click", function () {
      
            $("#dialog-message").dialog("open");
        
    });

    $("#dialog-message").dialog({
        resizable: false,
        height: "auto",
        autoOpen: false,
        modal: true,
        width: 450,
      //  dialogClass: "no-close",
        overlay:
            {
                opacity: 0.5,
                background: "black"
            },
        open: function () {

            // $(".info").html($(this).data('downloadId'));
        },
        buttons: [
            {
            text:"Load",
            "class": "btn btn_orange",
            click: function () {
                window.location = "/gateway/buy?eqid=" + $("#quoteid").val().replace(/\s+/, "");


    
                
    
            }
        },
          
        ]


    });


    $("#response-message").dialog({
        resizable: false,
        height: "auto",
        autoOpen: false,
        modal: true,
        width: 450,
        //  dialogClass: "no-close",
        overlay:
            {
                opacity: 0.5,
                background: "black"
            },
        open: function () {

            // $(".info").html($(this).data('downloadId'));
        },
        buttons: [
            {
                text: "OK",
                "class": "btn btn_orange",
                click: function () {


                    $(this).dialog("close");

                }
            },

        ]


    });


    $("#mk-message").dialog({
        resizable: false,
        height: "auto",
        autoOpen: false,
        modal: true,
        width: 490,
        //  dialogClass: "no-close",
        overlay:
            {
                opacity: 0.5,
                background: "black"
            },
        open: function () {

            // $(".info").html($(this).data('downloadId'));
        },
        buttons: [
            {
                text: "Generate",
                "class": "btn btn_orange",
                click: function () {

                    $(".loaderWrapper").show();
                    processDefferedMachineKey($("#machinekey").val(), $(this).data('contractId'));

                }
            },

        ]


    });


    $("#switch-message").dialog({
        resizable: false,
        height: "auto",
        autoOpen: false,
        modal: true,
        width: 450,
        //  dialogClass: "no-close",
        overlay:
            {
                opacity: 0.5,
                background: "black"
            },
        open: function () {
         
            // $(".info").html($(this).data('downloadId'));
        },
        buttons: [
            {
                text: "Switch",
                "class": "btn btn_orange",
                id: "switchButton",
                click: function () {

                    $("#switchButton").attr("disabled", true).addClass("ui-state-disabled");

                    SwitchKey($(this).data('ContractId'), $("#deactkey").val(), $("#newMachinekey").val());
                    
                    

                }
            },

        ]


    });


    function processDefferedMachineKey(mk, contractId) {


    



        var quoteString = "mk=" + encodeURIComponent(mk) + "&contractId=" + contractId;




        serviceGet(quoteString, '<%=ConfigurationManager.AppSettings["restServicApiURL"]%>/DeferredKeyGenerator', function (data) {

            //on success redirect check for machine key
            // alert(data);
            if (data.Success) {
                $(".loaderWrapper").show();
                location.reload();
            } else {
                $("#ValidationComments").show();
                $("#ValidationComments").html("<i class=\"fa fa-exclamation-triangle\" aria-hidden=\"true\"></i> We are unable to validate this machine key. It is either in use already or it is not a valid key.<div style=\"margin:10px 0;\"> Contact <a style=\"color:blue;\" href=\"mailto:sales@pyramidanalytics.com?cc=ilan@pyramidanalytics.com&subject=Machine%20Key%20Problem%20Id:%20" + quoteid + "&body=%20Machine%20Key%20is%20" + machinekey + "%0D%0AEnter%20your%20Message%20here%20and%20click%20send!\">sales@pyramidanalytics.com</a> if you need help.</div>");
                $(".loaderWrapper").hide();
            }
            




        });



        
    }
    function checkoutCommunity() {

        var ContactId = readCookie('ContactId'); //$('#ContactId').val();
        var CustomerId = readCookie('CustomerId'); //$('#CustomerId').val();



        var quoteString = "ServerType=" + 1 + "&SupportType=" + 0 + "&ProSeats=" + 3 + "&ViewerSeats=" + 0 + "&ContactId=" + ContactId + "&CustomerId=" + CustomerId + "&LicenseTerm=" + 12 + "&ExistingContractId=" + "" + "&isRenewal=" + "false";




        serviceGet(quoteString, '<%=ConfigurationManager.AppSettings["restServicApiURL"]%>/GenerateQuote', function (data) {

            //on success redirect check for machine key
            // alert(data);

            window.location.href = "/gateway/buy/machinekey?qid=" + data;




        });





    };


    function quickQuote(trialFlag) {

        var ContactId = readCookie('ContactId'); //$('#ContactId').val();
        var CustomerId = readCookie('CustomerId'); //$('#CustomerId').val();



        var quoteString = "customerId=" + CustomerId + "&contactId=" + ContactId + "&isTrial=" + trialFlag;

        serviceGet(quoteString, '<%=ConfigurationManager.AppSettings["restServicApiURL"]%>/QuickGenerateQuote', function (data) {

            window.location.href = "/gateway/buy/machinekey?qid=" + data;


        });





    };


    function populateLicensesRows(row, selector, pendingFlag) {

        var ServerType = "Free";
        switch (row.ServerType) {
        case 2:
            ServerType = "Standard";
            break;
        case 4:
            ServerType = "Enterprise";
            break;
        default:
            ServerType = "Community";
        }


        var SupportLevel = "Free";

        switch (row.SupportType) {
        case 0:
            SupportLevel = "None";
            break;
        case 1:
            SupportLevel = "Silver";
            break;
        case 2:
            SupportLevel = "Gold";
            break;
        case 3:
            SupportLevel = "Platinum";
            break;
        }

        var highlight = "";

        switch (row.LicenseType) {
        case "Trial":
        case "Full":
        case "Community":
        case "Non-Commercial":
            highlight = "";
            break;
        case "Provisional":
            highlight = " prov";
            break;
        case "Developer":
                highlight = " dev";
                break;
        case "Testing":
                highlight = " test";
                break;
        case "Expired":
            highlight = " exp";
            break;
        }

        //alert(row.PaymentStatus);
        switch (row.PaymentStatus) {
        case 0:
            highlight = " pending";
            break;

        }




        var dt = new Date(parseInt(row.DropDeadDate.substr(6)));
        var options = {  year: 'numeric', month: 'short', day: 'numeric' };
        var finalDate = dt.toLocaleDateString('en-US', options);


        var licType = row.LicenseType;

        var machineName = row.MachineName;
        var contractTitle = "";
        
        if (row.ContractTitle == null) {
            contractTitle = "";
     
        } else {
            contractTitle = row.ContractTitle;
        }
        console.log(contractTitle);
        if (machineName == "##deferred##") {
            highlight = " def";
            machineName = "Defered";
        }
        var optionButtons;
        if (row.IsKeyDeferred) {
            optionButtons = "<li class=\"box2\"><span class='butt mkInsert' id='" + row.ContractId + "' ><img src=\"/App_Themes/Pyramid/img/gatewayIcons/keys.png\"  class='img' alt='Download' style='height:16px;'/></span></li>";
        } else {
            optionButtons = "<li class=\"box2\"><span class='butt download' id='" + row.KeyFileId + "' ><img src=\"/App_Themes/Pyramid/img/gatewayIcons/keys.png\"  class='img' alt='Download' style='height:16px;'/></span></li>";
        }

        optionButtons += "<li class=\"box2\"><span class='butt renew' id='" + row.ContractId + "' ><img src=\"/App_Themes/Pyramid/img/gatewayIcons/renew.png\" class='img' alt='Renew' style='height:16px;'/></a></span></li>";

        if (licType != "Non-Commercial") {
            optionButtons += "<li class=\"box2\"><span class='butt upgrade' id='" + row.ContractId + "' ><img src=\"/App_Themes/Pyramid/img/gatewayIcons/upgrade.png\" class='img' alt='Upgrade' style='height:16px;' /> </a></span></li>";
        } else {
            optionButtons += "<li class=\"box2\">&nbsp;</li>";
        }

  

        if (licType != "Expired") {
            optionButtons += "<li class=\"box2\"><span target='_blank' class='butt switch  ' style=''  id='" + row.ContractId + "' ><img src=\"/App_Themes/Pyramid/img/gatewayIcons/serverSwitch.png\"  class='img' alt='Switch' style='height:16px;'/></span></li>";
        } else {
            optionButtons += "<li class=\"box2\">&nbsp;</li>";
        }

      

        if (pendingFlag) {
            finalDate = "Pending Approval";
            optionButtons = "";
            licType = "";

        }
      
        var template = "<div style='' class='" + highlight + "'  id=\"" + row.ContractId + "\">" +
            "<div id='" + row.ContractId + "' style='margin-top:5px; width: 234px; padding-left: 5px;'><div class='editContractTitle' style='display: inline-block; width:20px; height:18px;  text-align:center; cursor:pointer; float:left;'><i class='fa fa-pencil'></i></div><div class='saveContractTitle' style='width:20px; height:18px; float:left; text-align:center; cursor:pointer; display:none; '><i class='fa fa-save'></i></div></div><input type='text' id='ContractTitle_" + row.ContractId + "' readonly='readonly'  placeholder='Enter a Contract title' class='readonly " + highlight + "' style='width:130px; height:20px; float:left;' value='" + contractTitle + "'   />" +
            "<div style='clear:both;'></div>"+
            "<ul >" +
           "   <li class=\"box\">" +
      
            "      <span class=\"boxValue machineName\">" + machineName + "</span></li>" +
            "   <li class=\"box\">" +

            "      <span class=\"boxValue\">" + licType + "</span></li>" +
            "   <li class=\"box\">" +
            
            "      <span class=\"boxValue\">" + ServerType + "</span></li>" +
            "  <li class=\"box\">" +
        
            "      <span class=\"boxValue\">" + row.ProSeats.xformat(0) + "</span></li>" +
            "  <li class=\"box\">" +
           
            "      <span class=\"boxValue\">" + row.ViewerSeats.xformat(0) + "</span></li>" +
            "  <li class=\"box\">" +

            "      <span class=\"boxValue\">" + finalDate + "</span></li>" +
            "  <li class=\"box\" style='border-right:1px solid #000000; margin-right:5px;'>" +
     
            "      <span class=\"boxValue\">" + SupportLevel + "</span></li>" +
            
            optionButtons +
     
            "</ul>" +
        
            " <div style=\"clear: both;\"></div>" +
            "</div>";

        selector.append(template);

    }

    function populateOrderRows(row, selector, pendingFlag) {

       


        var dt = new Date(parseInt(row.QuoteExpirationDate.substr(6)));
        var options = { year: 'numeric', month: 'short', day: 'numeric' };
        var finalDate = dt.toLocaleDateString('en-US', options);

        var highlight = "";

      
        var optionButtons;
        optionButtons = "<li class=\"box2\"><span class='butt buynow' id='" + row.QuoteId + "' ><img src=\"/App_Themes/Pyramid/img/gatewayIcons/keys.png\"  class='img' alt='Download' style='height:16px;'/></span></li>";
  

        var template = "<div style='' class='" + highlight + "'  id=\"" + row.QuoteId + "\">" +
         
            "<ul >" +
       
            "   <li class=\"box\" style=\"width:250px; text-align:left;\">" +

            "      <span class=\"boxValue\">" + row.QuoteId + "</span></li>" +
        
            "  <li class=\"box\">" +

            "      <span class=\"boxValue\">" + row.ProSeatCount + "</span></li>" +
            "  <li class=\"box\">" +

            "      <span class=\"boxValue\">" + row.ViewerSeatCount + "</span></li>" +
            "  <li class=\"box\">" +

            "      <span class=\"boxValue\">" + finalDate + "</span></li>" +
            "  <li class=\"box\" style='border-right:1px solid #000000; margin-right:5px;'>" +

            "      <span class=\"boxValue\">" + row.SupportType + "</span></li>" +

            optionButtons +

            "</ul>" +

            " <div style=\"clear: both;\"></div>" +
            "</div>";
     
        selector.append(template);

    }

    function Renew(id) {

        window.location = "/gateway/buy/productoptions/?rcid=" + id;
    }

    function Upgrade(id) {

        window.location = "/gateway/buy/productoptions/?ecid=" + id;
    }

    function Switch(id) {

        window.location = "/gateway/switch-server?cid=" + id;
    }

    function Download(id) {
        
        getZipData(id, "PyramidLicenseKeys", '<%=ConfigurationManager.AppSettings["restServicApiURL"]%>',"/GetKeyZipData", "keyId", "pli");
        

    }

    
    function SwitchKey(contractId, deactivationKey, newMachineKey) {

        $(".loaderWrapper").show();
        var datastring = "contractId=" + contractId + "&deactivationKey=" + encodeURIComponent(deactivationKey) + "&newMachineKey=" + encodeURIComponent(newMachineKey);
        serviceGet(datastring, '<%=ConfigurationManager.AppSettings["restServicApiURL"]%>/ServerSwitch', function (data) {

            var icon = '<i class="fa fa-check-circle-o" aria-hidden="true" style="font-size: 75px; color: green; -webkit-text-stroke: 6px white;  "></i><br>';

            if (!data.Success) {
                icon = '<i class="fa fa-times-circle-o" aria-hidden="true" style="font-size: 75px; color: red; -webkit-text-stroke: 6px white;  "></i><br>';
            }
            $("#genResponseComment").html(icon+data.Message);
            $("#response-message").dialog("open");


           $("#switch-message").dialog("close");
      
            $("#switchButton").attr("disabled", false).removeClass("ui-state-disabled");
          $(".loaderWrapper").hide();


        });
    };


    function LoadLicensePackages() {
        var customerId = readCookie('CustomerId');
        $(".cLics").hide();
        $(".pLics").hide();
        $(".loaderWrapper").show();
        var quoteString = "customerId=" + customerId;

        serviceGet(quoteString, '<%=ConfigurationManager.AppSettings["restServicApiURL"]%>/GetLicenseInfo', function (data) {

            //  alert(data);
            var template = "<div class=\"boxHeadings\">" +
                
                    "<ul>" +
             "   <li class=\"box\">" +
                    "      <div class=\"boxTitle machineName\">Machine Name</div>" +
                "</li>"+
                    "   <li class=\"box\">" +
                    "      <div class=\"boxTitle\">License</div>" +
                "</li>" +
                    "   <li class=\"box\">" +
                    "      <div class=\"boxTitle\">Server Type</div>" +
            "</li>" +
                    "  <li class=\"box\">" +
                    "      <div class=\"boxTitle\">Pro Seats</div>" +
               "</li>" +
                    "  <li class=\"box\">" +
                    "      <div class=\"boxTitle\">Viewer Seats</div>" +
           "</li>" +
                    "  <li class=\"box\">" +
                    "      <div class=\"boxTitle\">Expiration</div>" +
               "</li>" +
                    "  <li class=\"box\"  style='border-right:1px solid #000000;  margin-right:5px;'>" +
                    "      <div class=\"boxTitle\">Support</div>" +
              "</li>" +
              "  <li class=\"box2\">" +
                    "      <div class=\"boxTitle\">Keys</div>" +
              "</li>" +
              "  <li class=\"box2\">" +
                    "      <div class=\"boxTitle\">Renew</div>" +
              "</li>" +
              "  <li class=\"box2\">" +
                    "      <div class=\"boxTitle\">Upgrade</div>" +
              "</li>" +
              "  <li class=\"box2\">" +
                    "      <div class=\"boxTitle\">Switch</div>" +
              "</li>" +
                   
                    "</ul>" +
                    " <div style=\"clear: both;\"></div>" +
                    "</div>";
            $("#Licenses").append(template);



            for (var i = 0; i < data.ContractItems.length; i++) {
            
                populateLicensesRows(data.ContractItems[i], $("#Licenses"), false);

            }
            if (data.ContractItems.length == 0) {
                noCurrentlicensesFlag = true;
                $(".cLics").hide();

            } else {
                $(".cLics").show();
             
                noCurrentlicensesFlag = false;
            }
      
            LoadPendingLicensePackages();

         

        });
    };


    function LoadPendingLicensePackages() {
        var customerId = readCookie('CustomerId');
       
        $(".loaderWrapper").show();
        var quoteString = "customerId=" + customerId;

        serviceGet(quoteString, '<%=ConfigurationManager.AppSettings["restServicApiURL"]%>/GetPendingLicenseInfo', function (data) {

            //  alert(data);
            for (var i = 0; i < data.ContractItems.length; i++) {
                populateLicensesRows(data.ContractItems[i], $("#PendingLicenses"), true);
            }
            if (data.ContractItems.length == 0) {
                noPendinglicensesFlag = true;
                $(".pLics").hide();

            } else {
                $(".pLics").show();
                noPendinglicensesFlag = false;
            }


            if (noPendinglicensesFlag && noCurrentlicensesFlag) {
                $(".noLicensesMessage").show();
            } else {
                $(".noLicensesMessage").hide();
            }

            $(".loaderWrapper").hide();

        });
    };


    


    function updateContractTitle(ContractId, newContractTitle) {
        $(".loaderWrapper").show();
        var quoteString = "contractId=" + ContractId + "&title=" + newContractTitle;

        serviceGet(quoteString, '<%=ConfigurationManager.AppSettings["restServicApiURL"]%>/UpdateContractTitle', function (data) {

            $(".loaderWrapper").hide();

            $("#ContractTitle").prop("readonly", true).addClass("readonly").removeClass("editable");
            $("#saveContractTitle").hide();
            $("#editContractTitle").show();
           // jalert("Contract Title Updated", data.Message);



        });
    }

    $(document).ready(function () {

  

        LoadLicensePackages();

        
        $('body').on('click', '.fa-pencil', function (event) {
         //   alert($(event.target).closest('.fa-pencil').find('.contractTitle').attr("id"));
            //.closest(".contractTitle").attr('id'));

        });

        $('body').on('click', '.renew', function (event) {
            Renew($(this).attr('id'));

        });

        $('body').on('click', '.upgrade', function (event) {
            Upgrade($(this).attr('id'));

        });

        $('body').on('click', '.switch', function (event) {
           
           $("#switch-message").data("ContractId", $(this).attr('id')).dialog("open");
        });


        $('body').on('click', '.download', function (event) {

            Download($(this).attr('id'));

        });

        $('body').on('click', '.mkInsert', function (event) {

            $("#mk-message").data("contractId", $(this).attr('id')).dialog("open");

        });

        


        $("#communityJump").click(function () {
            quickQuote(false);
        });

        $("#trialJump").click(function () {
            quickQuote(true);
        });


        $("#betakeysJump").click(function () {
            quickQuote(true);
        });

        

        $("#getQuote").click(function () {
            window.location = "/gateway/buy?eqid="+$("#quoteid").val();
        });

        $(".saveContractTitle").hide();
        $("body").on("click", ".editContractTitle", function () {
            
            var container_id = $(this).parent().attr('id');
            var inputField = $("#ContractTitle_" + container_id).prop("readonly", false).addClass("editable").removeClass("readonly");
          //  alert(container_id);
            //  $("#ContractTitle");
              $(this).hide();
              $("#" + container_id + " .saveContractTitle").css("display", "inline-block");

        });
        $("body").on("click", ".saveContractTitle", function () {
            
            var containerId = $(this).parent().attr('id');
            
            var inputFieldValue = $("#ContractTitle_" + containerId).prop("readonly", true).addClass("readonly").removeClass("editable").val();
            //alert(inputFieldValue);
            $(this).hide();
            $("#" + containerId + " .editContractTitle").css("display", "inline-block");
            updateContractTitle(containerId, inputFieldValue);
        });



    });


</script>




