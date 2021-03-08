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
  textarea: "    "

---
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

.gatewayNew .licenseOverview .box {
    width: 96px;
}

.box .machineName{ text-align: left;width: 100%;display: inline-block;}
.gatewayNew .gatewayContent a{
    color:#000000;
    display:block;
    width: 180px;   
    margin: 0px auto 10px auto;
    text-align:left;
}
.gatewayNew .gatewayContent a::before{
    margin-right:5px;
    content:url("/jquery-ui-1.12.1.custom/arrow2.png");
    float:left;
}

.gatewayNew .gatewayContent a.noafter::before{
    content:none;
}

.gatewayNew .gatewayContent .dashHeading{
    line-height: 50px; font-size: 14px; width: 180px; 
    margin: 0px auto 10px auto;
    height:55px;
    border-bottom:1px solid #b1b1b1;
    
    
}
.innerHeading{
    text-align:center;
    padding:0 18%;
}
    .innerHeading span {
        display:inline-block;
        height:50px;
        float:left;
    }
    .innerHeading img{
        display:inline-block;
        float:left;
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
             
                <li class="menuOn"><a href="/gateway/overview">Dashboard</a></li>
              <li ><a href="/gateway/licenses">Licenses</a></li>
                <li class="myorders"><a href="/gateway/orders">Open Orders</a></li>
                <li ><a href="/gateway/profile">Profile</a></li>
                <li ><a href="/gateway/buy">Buy</a></li>
                <li><a href="/gateway/application-downloads">Downloads</a></li>
                <li><a href="/gateway/kubernetes">Kubernetes</a></li>
                <li><a href="/logout">Logout</a></li>


            </ul>



        </div>
        <div class="gatewayContent">
            <div class="licenseOverview">
             
                
                
              <div class="sf_cols">
    <div class="sf_colsOut sf_4cols_1_25">
        <div id="cphMain_C031_Col00" class="sf_colsIn sf_4cols_1in_25">
                        <div class="dashHeading"><div class="innerHeading"><img src="/jquery-ui-1.12.1.custom/buy.png" /> <span style="">Buy</span></div></div>
            <div style="clear:both"></div>
                        <a href="/gateway/orders" class=" " >I have an order</a>
                        <a href="/gateway/buy/license-wizard" class=" " >License Upgrade</a>
            
                        <a href="/gateway/licenses" class=" " >License Renewal</a>
            
            
        </div>
    </div>
    <div class="sf_colsOut sf_4cols_2_25">
        <div id="cphMain_C031_Col01" class="sf_colsIn sf_4cols_2in_25">  
             <div class="dashHeading"><div class="innerHeading"><img src="/jquery-ui-1.12.1.custom/contact.png"/> <span style="">Contact</span> </div></div>
            <div style="clear:both"></div>
            <a href="https://support.pyramidanalytics.com/hc/en-us" class=" " target="_blank"> Contact Support</a>
           <a href="/free-trial/request-demo" class="" style="">Schedule Demo</a>
            
            <a href="/gateway/edit-profile" class=" "  style="width: 180px;  margin: 0px auto 20px auto">Profile Update</a>
        </div>
    </div>
    <div class="sf_colsOut sf_4cols_3_25">
        <div id="cphMain_C031_Col02" class="sf_colsIn sf_4cols_3in_25">
            <div class="dashHeading"><div class="innerHeading"><img src="/jquery-ui-1.12.1.custom/help.png" /> <span style="">Help</span> </div></div>
             <div style="clear:both"></div>
                <a href="https://help.pyramidanalytics.com/Content/Root/general/Welcome.htm" class=" " target="_blank" >Online help</a>

            <a href="https://help.pyramidanalytics.com/Content/Root/Guides/installation/Installer%20Overview.htm" class=" " target="_blank">Installation Guide</a>
            
            
            <a href="#" class=" " target="_blank"  id="forumLink" >Community Forum Login</a>
            
            
            
        </div>
    </div>
    <div class="sf_colsOut sf_4cols_4_25">
        <div id="cphMain_C031_Col03" class="sf_colsIn sf_4cols_4in_25">
                       <div class="dashHeading" style=" margin-bottom:0;"><div class="innerHeading"><img src="/jquery-ui-1.12.1.custom/downloads.png" style="display:inline;"/> <span style="">Download</span> </div></div>
            <div style="clear:both"></div>
            
                    
            
            <a href="/gateway/application-downloads" class=""  style="width: 180px;  padding: 12px 5px 0px 5px; margin: 0px auto 0px auto;  ">Latest Software</a>
     
                        <a id="" href="https://play.google.com/store/apps/details?id=pyramid.analytics"  class="" style="    padding: 10px 5px 10px 5px;"><img style="width:16px; float:left;" src="https://www.pyramidanalytics.com/images/default-source/pyramid-2020/google77bf9b4e7dd26215b1eeff00002b9892.svg?sfvrsn=cc6df9c9_2" alt="google"/> <span style=" display: inline-block;
    height: 16px; float: left; line-height:16px; margin-left:10px; ">Google Play</span></a>
                 <a id="" href="https://itunes.apple.com/app/id1355475947"  class="" style="     padding: 10px 5px 10px 5px;"><img style="width:16px; float:left;" src="https://www.pyramidanalytics.com/images/default-source/pyramid-2020/apple61bf9b4e7dd26215b1eeff00002b9892.svg?sfvrsn=cf6df9c9_2" alt="apple"/> <span style=" display: inline-block;
    height: 16px; float: left; line-height:16px; margin-left:10px; ">Apple Store</span></a>
       <a id="" href="/gateway/kubernetes"  class="" style="     padding: 10px 5px 0px 5px;"><img  style="width:16px; float:left;" src="https://www.pyramidanalytics.com/images/default-source/pyramid-2020/kubernetes.svg?sfvrsn=cd6df9c9_2" alt="kubernetes"/> <span style=" display: inline-block;
    height: 16px; float: left; line-height:16px; margin-left:10px; ">Kubernetes Setup</span></a>
       
            
        </div>
    </div>
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


<script type="text/javascript">


    




   

    function getForumLink() {
        var customerId = readCookie('CustomerId');
        var contactId = readCookie('ContactId');

        var quoteString = "customerId=" + customerId + "&contactId=" + contactId;

        serviceGet(quoteString, '<%=ConfigurationManager.AppSettings["restServicApiURL"]%>/ForumbeeSsoLink', function (data) {
          //  alert(data);
            $("#forumLink").attr('href',data);
            //  alert(data);
        });
    }

    $(document).ready(function () {

        getForumLink();

        var ut = readCookie("userType");
        

        $("#loadOrder").button().on("click", function () {

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
                    text: "Checkout",
                    "class": "btn btn_orange",
                    click: function () {
                        window.location = "/gateway/buy?eqid=" + $("#quoteid").val();





                    }
                },

            ]


        });
     
        

        $("#getQuote").click(function () {
            window.location = "/gateway/buy?eqid="+$("#quoteid").val();
        });

        
  


    });


</script>




