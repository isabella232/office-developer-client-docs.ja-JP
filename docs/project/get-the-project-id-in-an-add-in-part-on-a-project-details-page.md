---
title: プロジェクト詳細ページのアドインの部分でプロジェクト ID を取得する
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: アドインパーツは、ホスティングページから完全に分離された iframe 要素にホストされます。 プロジェクト詳細ページ (PDP) のアドインパーツから現在のプロジェクトに関する情報を取得するには、postMessage メソッド、イベントリスナー、およびメッセージからプロジェクト ID を解析するイベントハンドラーを使用できます。
ms.openlocfilehash: ffaf9cb7dac783a754b2d56b5ece4d5a7a0319be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322597"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a><span data-ttu-id="ec483-104">プロジェクト詳細ページのアドインの部分でプロジェクト ID を取得する</span><span class="sxs-lookup"><span data-stu-id="ec483-104">Get the project ID in an add-in part on a Project Details Page</span></span>

<span data-ttu-id="ec483-105">アドインパーツは、ホスティングページから完全に分離された**iframe**要素にホストされます。</span><span class="sxs-lookup"><span data-stu-id="ec483-105">Add-in parts are hosted in **iframe** elements that are fully isolated from the hosting page.</span></span> <span data-ttu-id="ec483-106">プロジェクト詳細ページ (PDP) のアドインパーツから現在のプロジェクトに関する情報を取得するには、 **postMessage**メソッド、イベントリスナー、およびメッセージからプロジェクト ID を解析するイベントハンドラーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ec483-106">To get information about the current project from an add-in part on Project Details Page (PDP), you can use the **window.postMessage** method, an event listener, and an event handler that parses out the project ID from the message.</span></span> 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a><span data-ttu-id="ec483-107">プロジェクト ID を取得する SharePoint ホスト型アドインパーツを作成するための前提条件</span><span class="sxs-lookup"><span data-stu-id="ec483-107">Prerequisites for creating a SharePoint-hosted add-in part that gets the project ID</span></span>
<span data-ttu-id="ec483-108"><a name="Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="ec483-108"></span></span>

<span data-ttu-id="ec483-109">この記事のコード例を使用するには、次のいずれかが必要になります。</span><span class="sxs-lookup"><span data-stu-id="ec483-109">To use the code example in this article, you'll need either of the following:</span></span>
  
- <span data-ttu-id="ec483-110">SharePoint 2013 および Project Server 2013。アドイン分離用に構成されています。</span><span class="sxs-lookup"><span data-stu-id="ec483-110">SharePoint 2013 and Project Server 2013, configured for add-in isolation.</span></span> <span data-ttu-id="ec483-111">リモートで開発している場合、サーバーはアドインのサイドロードをサポートする必要があります。または、開発者向けサイトにアドインをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec483-111">If you're developing remotely, the server must support sideloading of add-ins or you must install the add-in on a Developer Site.</span></span>
  
- <span data-ttu-id="ec483-112">SharePoint online と Project online</span><span class="sxs-lookup"><span data-stu-id="ec483-112">SharePoint Online and Project Online</span></span>
    
    - <span data-ttu-id="ec483-113">visual studio 2013、visual studio 2012 (Office Developer Tools for visual studio 2013、または Napa</span><span class="sxs-lookup"><span data-stu-id="ec483-113">Visual Studio 2013, Visual Studio 2012 with Office Developer Tools for Visual Studio 2013, or Napa</span></span>
        
    - <span data-ttu-id="ec483-114">ログオン ユーザーの次の十分なアクセス許可。</span><span class="sxs-lookup"><span data-stu-id="ec483-114">Sufficient permissions for the logged-on user:</span></span>
        
        - <span data-ttu-id="ec483-115">開発用コンピュータのローカル管理者権限。</span><span class="sxs-lookup"><span data-stu-id="ec483-115">Local administrator permissions on the development computer.</span></span>
            
        - <span data-ttu-id="ec483-116">少なくとも1つのプロジェクトへの読み取りアクセス権。</span><span class="sxs-lookup"><span data-stu-id="ec483-116">Read access to at least one project.</span></span>
            
        - <span data-ttu-id="ec483-117">Project Web App サイトのページを編集する権限。</span><span class="sxs-lookup"><span data-stu-id="ec483-117">Permission to edit pages on the Project Web App site.</span></span>
            
        - <span data-ttu-id="ec483-118">システム アカウント以外の誰かとしてログオンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec483-118">You must be logged on as someone other than the system account.</span></span> <span data-ttu-id="ec483-119">システムアカウントにアドインをインストールする権限がありません。</span><span class="sxs-lookup"><span data-stu-id="ec483-119">The system account does not have permission to install an add-in.</span></span>
    
<span data-ttu-id="ec483-120">project 用アドインの詳細については、「project [Server 2013 用のアドインを作成するための前提条件](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ec483-120">See [Prerequisites for creating an add-in for Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) for more information about add-ins for Project.</span></span> <span data-ttu-id="ec483-121">オンプレミスの設定 (必要に応じてループバックチェックを無効にする方法を含む) に関するガイダンスについては[、「SharePoint アドインのオンプレミスの開発環境をセットアップ](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ec483-121">See [Set up an on-premises development environment for SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) for guidance about on-premises setup (including how to disable the loopback check, if necessary).</span></span> <span data-ttu-id="ec483-122">リモートで開発している場合は、「[リモートシステムで SharePoint 用アプリを開発](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ec483-122">If you're developing remotely, see [Developing apps for SharePoint on a remote system](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).</span></span>
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a><span data-ttu-id="ec483-123">SharePoint ホスト型アドインとクライアント web パーツを作成する</span><span class="sxs-lookup"><span data-stu-id="ec483-123">Create the SharePoint-hosted add-in and client web part</span></span>
<span data-ttu-id="ec483-124"><a name="CreateApp"> </a></span><span class="sxs-lookup"><span data-stu-id="ec483-124"></span></span>

1. <span data-ttu-id="ec483-125">Visual Studio を開き、[**ファイル** > ] [**新しい** > **プロジェクト**] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="ec483-125">Open Visual Studio and choose **File** > **New** > **Project**.</span></span>
    
2. <span data-ttu-id="ec483-126">[ **新しいプロジェクト**] ダイアログ ボックスで、上部のドロップダウン リストから [ **.NET Framework 4.5**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec483-126">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
3. <span data-ttu-id="ec483-127">[**テンプレート**] リストで、[ **Visual C#** > **Office/sharepoint** > **アドイン** > **アドイン (sharepoint 用) 2013**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec483-127">In the **Templates** list, choose **Visual C#** > **Office/SharePoint** > **Add-ins** > **Add-in for SharePoint 2013**.</span></span>
    
4. <span data-ttu-id="ec483-128">アドインに GetProjectIdAddinPart という名前を指定し、[ **OK** ] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ec483-128">Name the add-in GetProjectIdAddinPart, and then choose the **OK** button.</span></span> 
    
5. <span data-ttu-id="ec483-129">[ **SharePoint 用アドインの新規作成**] ダイアログボックスで、デバッグに使用する PWA サイトの URL を入力します (例: _https://contoso.com/sites/pwasite/_)。</span><span class="sxs-lookup"><span data-stu-id="ec483-129">In the **New add-in for SharePoint** dialog box, enter the URL of the PWA site that you want to use for debugging (for example:  _https://contoso.com/sites/pwasite/_).</span></span>
    
6. <span data-ttu-id="ec483-130">[ **SharePoint ホスト型**] オプションを選択してアドインをホストし、[**完了**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ec483-130">Choose the **SharePoint-hosted** option to host your add-in, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="ec483-131">**ソリューションエクスプローラー**で、GetProjectIdAddinPart プロジェクトのショートカットメニューを開き、[**新しい項目**の**追加** > ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec483-131">In **Solution Explorer**, open the shortcut menu for the GetProjectIdAddinPart project, and then choose **Add** > **New Item**.</span></span>
    
8. <span data-ttu-id="ec483-132">[**新しいアイテムの追加**] ダイアログボックスで、[**クライアント web パーツ (ホスト web)**] を選択し、web パーツ GetProjectId に名前を指定して、[**追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ec483-132">In the **Add New Item** dialog box, choose **Client web part (Host Web)**, name the web part GetProjectId, and then choose the **Add** button.</span></span> 
    
9. <span data-ttu-id="ec483-133">[**クライアント web パーツの作成**] ダイアログボックスで、[**新しいクライアント web パーツページを作成する**] オプションを選択し、[**完了**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ec483-133">In the **Create Client web part** dialog box, choose the **Create a new client web part page** option, and then choose the **Finish** button.</span></span> 
    
## <a name="get-the-project-id-in-the-add-in-part"></a><span data-ttu-id="ec483-134">アドインパーツのプロジェクト ID を取得する</span><span class="sxs-lookup"><span data-stu-id="ec483-134">Get the project ID in the add-in part</span></span>
<span data-ttu-id="ec483-135"><a name="GetProjectId"> </a></span><span class="sxs-lookup"><span data-stu-id="ec483-135"></span></span>

<span data-ttu-id="ec483-136">GetProjectId アドインパーツは、クライアント web パーツの GetProjectId ページでカスタムコードを定義します。</span><span class="sxs-lookup"><span data-stu-id="ec483-136">The GetProjectId add-in part defines its custom code in the GetProjectId.aspx page of the client web part.</span></span> <span data-ttu-id="ec483-137">メッセージを受け取って処理するロジックは、ページの**head**要素で定義され、ページコントロールはページの**body**要素で定義されます。</span><span class="sxs-lookup"><span data-stu-id="ec483-137">The logic that receives and handles the message is defined in the **head** element of the page and the page controls are defined in the **body** element of the page.</span></span> 
  
1. <span data-ttu-id="ec483-138">GetProjectId web パーツページ ( **Pages**フォルダー内) を開きます。</span><span class="sxs-lookup"><span data-stu-id="ec483-138">Open the GetProjectId.aspx web part page (in the **Pages** folder).</span></span> 
    
2. <span data-ttu-id="ec483-139">ページの**head**要素で、 **script**タグ間のコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="ec483-139">In the **head** element of the page, replace the code between the **script** tags with the following code.</span></span> 
    
   ```js
        'use strict';
        // Define global variables.
        var hostUrl = '';
        var projectUid;
        // Set the style of the client web part page to be consistent with the host web.
                (function () {
                    var hostUrl = '';
                    var link = document.createElement('link');
                    link.setAttribute('rel', 'stylesheet');
                    if (document.URL.indexOf('?') != -1) {
                        var params = document.URL.split('?')[1].split('&');
                        for (var i = 0; i < params.length; i++) {
                            var p = decodeURIComponent(params[i]);
                            if (/^SPHostUrl=/i.test(p)) {
                                hostUrl = p.split('=')[1];
                                link.setAttribute('href', hostUrl + '/_layouts/15/defaultcss.ashx');
                                break;
                            }
                        }
                    }
                    if (hostUrl == '') {
                        link.setAttribute('href', '/_layouts/15/1033/styles/themable/corev15.css');
                    }
                    document.head.appendChild(link);
                })();
        // Get the message.
        function getProjectUid() {
            window.parent.postMessage('getprojectuid', hostUrl);
        }
        getProjectUid();
        // Add an event listener and register the event handler.
        // If the IE browser version is earlier than 9, use the attachEvent method.
        if (window.addEventListener) {
            window.addEventListener("message", onMessage, false);
        }
        else {
            if (window.attachEvent) {
                window.attachEvent("onmessage", onMessage);
            }
        }
        // Get the project ID from the message.
        function onMessage(event) {
            // Verify the message origin.
            if (hostUrl.indexOf(event.origin) != 0) return;
            // The expected message format is "<PDPProjectUid>00000000-0000-0000-0000-000000000000</PDPProjectUid>,"
            // so validate by using the length and the start and end tags.
            var length = event.data.length;
            if (length = 67) {
                var expectedStart = "<PDPProjectUid>";
                var expectedEnd = "</PDPProjectUid>";
                var endTagPosition = length - expectedEnd.length;
                var start = event.data.substr(0, expectedStart.length);
                var end = event.data.substr(endTagPosition, expectedEnd.length);
                // Parse out the project ID.
                if (start == expectedStart && end == expectedEnd) {
                    projectUid = event.data.substr(expectedStart.length, 36);
                    $get('projectUid').innerText = projectUid;
                }
            }
        }
   ```

3. <span data-ttu-id="ec483-140">ページの**body**要素に次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="ec483-140">Add the following code in the **body** element of the page.</span></span> <span data-ttu-id="ec483-141">このコードでは、プロジェクト ID を表示する span コントロールを定義します。</span><span class="sxs-lookup"><span data-stu-id="ec483-141">The code defines a span control that displays the project ID.</span></span> 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. <span data-ttu-id="ec483-142">Elements .xml ファイルで、必要に応じてアドインパーツの名前、タイトル、説明、および既定のサイズを変更します。</span><span class="sxs-lookup"><span data-stu-id="ec483-142">In the Elements.xml file, optionally change the name, title, description, and default size of the add-in part.</span></span> <span data-ttu-id="ec483-143">この例では、既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ec483-143">This example uses the default values.</span></span>
    
5. <span data-ttu-id="ec483-144">アドインパーツをテストするには、メニューバーで [**デバッグ**] を選択し、**デバッグを開始**します。</span><span class="sxs-lookup"><span data-stu-id="ec483-144">To test the add-in part, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="ec483-145">web.config ファイルを変更するように求められた場合は、[ **OK**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ec483-145">If you're prompted to modify the web.config file, choose the **OK** button.</span></span> 
    
   <span data-ttu-id="ec483-146">アドインパーツをデバッグするには、追加したスクリプトに適切なブレークポイントを設定します。</span><span class="sxs-lookup"><span data-stu-id="ec483-146">To debug the add-in part, set appropriate breakpoints in the script that you added.</span></span>
    
6. <span data-ttu-id="ec483-147">PDP ページに移動し、[ツール] メニュー (歯車アイコン) から [**ページの編集**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec483-147">Browse to a PDP page and choose **Edit page** from the Tools menu (gear icon).</span></span> 
    
7. <span data-ttu-id="ec483-148">**GetProjectId Title**パーツをページ上の web パーツに追加します。</span><span class="sxs-lookup"><span data-stu-id="ec483-148">Add the **GetProjectId Title** part to a web part on the page.</span></span> <span data-ttu-id="ec483-149">プロジェクト ID が web パーツページの**span**コントロールに表示されます。</span><span class="sxs-lookup"><span data-stu-id="ec483-149">The project ID displays in the **span** control on the web part page.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="ec483-150">次の手順</span><span class="sxs-lookup"><span data-stu-id="ec483-150">Next steps</span></span>
<span data-ttu-id="ec483-151"><a name="NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="ec483-151"></span></span>

<span data-ttu-id="ec483-152">この例のアドインパーツは、Project Server データまたは SharePoint データにアクセスしません。</span><span class="sxs-lookup"><span data-stu-id="ec483-152">The add-in part in this example doesn't access Project Server data or SharePoint data.</span></span> <span data-ttu-id="ec483-153">プロダクト ID を使用して、JavaScript オブジェクトモデル、REST サービスなど、クライアント API を使用して現在のプロジェクトに関する情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="ec483-153">You can use the product ID to get information about the current project by using a client API, such as the JavaScript object model or the REST service.</span></span>
  
<span data-ttu-id="ec483-154">appmanifest.xml ファイルで、アドインが Project Server データまたは SharePoint データにアクセスするために必要なアクセス許可を指定します。</span><span class="sxs-lookup"><span data-stu-id="ec483-154">In the AppManifest.xml file, specify the permissions that your add-in needs to access Project Server data or SharePoint data.</span></span> 
  
<span data-ttu-id="ec483-155">アドインパーツにカスタムプロパティを設定する方法については[、「アドインパーツを作成して SharePoint アドインと共にインストールする](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ec483-155">See [Create add-in parts to install with your SharePoint Add-in](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) to learn how to set custom properties for an add-in part.</span></span> 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a><span data-ttu-id="ec483-156">例: PDP ページでアドインパーツのプロジェクト ID を取得する</span><span class="sxs-lookup"><span data-stu-id="ec483-156">Example: Getting the project ID in an add-in part on a PDP page</span></span>
<span data-ttu-id="ec483-157"><a name="CodeExample"> </a></span><span class="sxs-lookup"><span data-stu-id="ec483-157"></span></span>

<span data-ttu-id="ec483-158">次の例は、クライアント web パーツの GetProjectID ページの完全なコードです。</span><span class="sxs-lookup"><span data-stu-id="ec483-158">The following example is the complete code in the client web part's GetProjectID.aspx page.</span></span> <span data-ttu-id="ec483-159">このコードでは、プロジェクト ID を含むメッセージを受け取って解析するイベントリスナーとイベントハンドラーを登録します。</span><span class="sxs-lookup"><span data-stu-id="ec483-159">The code registers an event listener and an event handler that receives and parses a message that contains the project ID.</span></span>
  
```HTML
<%@ Page language="C#" Inherits="Microsoft.SharePoint.WebPartPages.WebPartPage, Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="WebPartPages" Namespace="Microsoft.SharePoint.WebPartPages" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<WebPartPages:AllowFraming ID="AllowFraming" runat="server" />
<html>
<head>
    <title></title>
    <script type="text/javascript" src="../Scripts/jquery-1.7.1.min.js"></script>
    <script type="text/javascript" src="/_layouts/15/MicrosoftAjax.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.runtime.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.js"></script>
    <script type="text/javascript">
        'use strict';
        // Define global variables.
        var hostUrl = '';
        var projectUid;
        // Set the style of the client web part page to be consistent with the host web.
        (function () {
            var hostUrl = '';
            var link = document.createElement('link');
            link.setAttribute('rel', 'stylesheet');
            if (document.URL.indexOf('?') != -1) {
                var params = document.URL.split('?')[1].split('&');
                for (var i = 0; i < params.length; i++) {
                    var p = decodeURIComponent(params[i]);
                    if (/^SPHostUrl=/i.test(p)) {
                        hostUrl = p.split('=')[1];
                        link.setAttribute('href', hostUrl + '/_layouts/15/defaultcss.ashx');
                        break;
                    }
                }
            }
            if (hostUrl == '') {
                link.setAttribute('href', '/_layouts/15/1033/styles/themable/corev15.css');
            }
            document.head.appendChild(link);
        })();
        // Get the message.
        function getProjectUid() {
            window.parent.postMessage('getprojectuid', hostUrl);
        }
        getProjectUid();
        // Add an event listener and register the event handler.
        // If the IE browser version is earlier than 9, use the attachEvent method.
        if (window.addEventListener) {
            window.addEventListener("message", onMessage, false);
        }
        else {
            if (window.attachEvent) {
                window.attachEvent("onmessage", onMessage);
            }
        }
        // Get the project ID from the message.
        function onMessage(event) {
            // Verify the message origin.
            if (hostUrl.indexOf(event.origin) != 0) return;
            // The expected message format is "<PDPProjectUid>00000000-0000-0000-0000-000000000000</PDPProjectUid>,"
            // so validate by using the length and the start and end tags.
            var length = event.data.length;
            if (length = 67) {
                var expectedStart = "<PDPProjectUid>";
                var expectedEnd = "</PDPProjectUid>";
                var endTagPosition = length - expectedEnd.length;
                var start = event.data.substr(0, expectedStart.length);
                var end = event.data.substr(endTagPosition, expectedEnd.length);
                // Parse out the project ID.
                if (start == expectedStart && end == expectedEnd) {
                    projectUid = event.data.substr(expectedStart.length, 36);
                    $get('projectUid').innerText = projectUid;
                }
            }
        }
    </script>
</head>
<body>
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
</body>
</html>

```

## <a name="see-also"></a><span data-ttu-id="ec483-160">関連項目</span><span class="sxs-lookup"><span data-stu-id="ec483-160">See also</span></span>

- [<span data-ttu-id="ec483-161">Project のプログラミング タスク</span><span class="sxs-lookup"><span data-stu-id="ec483-161">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="ec483-162">SharePoint をホストとする Project Server アドインを作成する</span><span class="sxs-lookup"><span data-stu-id="ec483-162">Create a SharePoint-hosted Project Server add-in</span></span>](create-a-sharepoint-hosted-project-server-add-in.md)
- [<span data-ttu-id="ec483-163">アドイン パーツを作成して SharePoint アドインと共にインストールする</span><span class="sxs-lookup"><span data-stu-id="ec483-163">Create add-in parts to install with your SharePoint Add-in</span></span>](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

