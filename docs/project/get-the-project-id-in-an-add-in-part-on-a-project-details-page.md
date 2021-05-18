---
title: プロジェクト詳細ページのアドインの部分でプロジェクト ID を取得する
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: アドイン パーツは、ホスティング ページから完全に分離された iframe 要素でホストされます。 Project 詳細ページ (PDP) のアドイン パーツから現在のプロジェクトに関する情報を取得するには、window.postMessage メソッド、イベント リスナー、およびメッセージからプロジェクト ID を解析するイベント ハンドラーを使用できます。
ms.openlocfilehash: ffaf9cb7dac783a754b2d56b5ece4d5a7a0319be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322597"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a><span data-ttu-id="93c8f-104">プロジェクト詳細ページのアドインの部分でプロジェクト ID を取得する</span><span class="sxs-lookup"><span data-stu-id="93c8f-104">Get the project ID in an add-in part on a Project Details Page</span></span>

<span data-ttu-id="93c8f-105">アドイン パーツは、ホスティング ページから完全に分離された **iframe** 要素でホストされます。</span><span class="sxs-lookup"><span data-stu-id="93c8f-105">Add-in parts are hosted in **iframe** elements that are fully isolated from the hosting page.</span></span> <span data-ttu-id="93c8f-106">Project 詳細ページ (PDP) のアドイン パーツから現在のプロジェクトに関する情報を取得するには **、window.postMessage** メソッド、イベント リスナー、およびメッセージからプロジェクト ID を解析するイベント ハンドラーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93c8f-106">To get information about the current project from an add-in part on Project Details Page (PDP), you can use the **window.postMessage** method, an event listener, and an event handler that parses out the project ID from the message.</span></span> 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a><span data-ttu-id="93c8f-107">プロジェクト ID を取得するSharePointホスト型アドイン パーツを作成するための前提条件</span><span class="sxs-lookup"><span data-stu-id="93c8f-107">Prerequisites for creating a SharePoint-hosted add-in part that gets the project ID</span></span>
<span data-ttu-id="93c8f-108"><a name="Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="93c8f-108"><a name="Prereqs"> </a></span></span>

<span data-ttu-id="93c8f-109">この記事のコード例を使用するには、次のどちらかが必要です。</span><span class="sxs-lookup"><span data-stu-id="93c8f-109">To use the code example in this article, you'll need either of the following:</span></span>
  
- <span data-ttu-id="93c8f-110">SharePoint分離用にProject 2013 およびサーバー 2013 を使用します。</span><span class="sxs-lookup"><span data-stu-id="93c8f-110">SharePoint 2013 and Project Server 2013, configured for add-in isolation.</span></span> <span data-ttu-id="93c8f-111">リモートで開発する場合、サーバーはアドインのサイドローディングをサポートするか、開発者サイトにアドインをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="93c8f-111">If you're developing remotely, the server must support sideloading of add-ins or you must install the add-in on a Developer Site.</span></span>
  
- <span data-ttu-id="93c8f-112">SharePointオンラインとProject Online</span><span class="sxs-lookup"><span data-stu-id="93c8f-112">SharePoint Online and Project Online</span></span>
    
    - <span data-ttu-id="93c8f-113">Visual Studio 2013 2012 Visual Studio 2012 Office開発者向けツール、Visual Studio 2013 Napa</span><span class="sxs-lookup"><span data-stu-id="93c8f-113">Visual Studio 2013, Visual Studio 2012 with Office Developer Tools for Visual Studio 2013, or Napa</span></span>
        
    - <span data-ttu-id="93c8f-114">ログオン ユーザーの次の十分なアクセス許可。</span><span class="sxs-lookup"><span data-stu-id="93c8f-114">Sufficient permissions for the logged-on user:</span></span>
        
        - <span data-ttu-id="93c8f-115">開発用コンピュータのローカル管理者権限。</span><span class="sxs-lookup"><span data-stu-id="93c8f-115">Local administrator permissions on the development computer.</span></span>
            
        - <span data-ttu-id="93c8f-116">少なくとも 1 つのプロジェクトへの読み取りアクセス。</span><span class="sxs-lookup"><span data-stu-id="93c8f-116">Read access to at least one project.</span></span>
            
        - <span data-ttu-id="93c8f-117">サイト上のページを編集Project Web Appアクセス許可。</span><span class="sxs-lookup"><span data-stu-id="93c8f-117">Permission to edit pages on the Project Web App site.</span></span>
            
        - <span data-ttu-id="93c8f-118">システム アカウント以外の誰かとしてログオンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="93c8f-118">You must be logged on as someone other than the system account.</span></span> <span data-ttu-id="93c8f-119">システム アカウントには、アドインをインストールするアクセス許可が付与されません。</span><span class="sxs-lookup"><span data-stu-id="93c8f-119">The system account does not have permission to install an add-in.</span></span>
    
<span data-ttu-id="93c8f-120">詳細[については、「Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites)のアドインを作成するための前提条件」を参照Project。</span><span class="sxs-lookup"><span data-stu-id="93c8f-120">See [Prerequisites for creating an add-in for Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) for more information about add-ins for Project.</span></span> <span data-ttu-id="93c8f-121">オンプレミス[のセットアップに関するガイダンスについては、「SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins)アドインのオンプレミスの開発環境をセットアップする(必要に応じてループバック チェックを無効にする方法を含む)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93c8f-121">See [Set up an on-premises development environment for SharePoint Add-ins](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins) for guidance about on-premises setup (including how to disable the loopback check, if necessary).</span></span> <span data-ttu-id="93c8f-122">リモートで開発する場合は、「リモート システムでのアプリの開発[SharePointを参照してください](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins)。</span><span class="sxs-lookup"><span data-stu-id="93c8f-122">If you're developing remotely, see [Developing apps for SharePoint on a remote system](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins).</span></span>
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a><span data-ttu-id="93c8f-123">ホストされるSharePointクライアント Web パーツを作成する</span><span class="sxs-lookup"><span data-stu-id="93c8f-123">Create the SharePoint-hosted add-in and client web part</span></span>
<span data-ttu-id="93c8f-124"><a name="CreateApp"> </a></span><span class="sxs-lookup"><span data-stu-id="93c8f-124"><a name="CreateApp"> </a></span></span>

1. <span data-ttu-id="93c8f-125">[ファイルVisual Studio開き、[**ファイル** の新  >  **しいファイル] を**  >  **Project。**</span><span class="sxs-lookup"><span data-stu-id="93c8f-125">Open Visual Studio and choose **File** > **New** > **Project**.</span></span>
    
2. <span data-ttu-id="93c8f-126">**[新しいプロジェクト]** ダイアログ ボックスで、上部のドロップダウン リストから **[.NET Framework 4.5]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="93c8f-126">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
3. <span data-ttu-id="93c8f-127">[テンプレート **] リスト** で  >  、[2013 **Visual C#Office/SharePoint** アドイン アドイン] を選択SharePoint  >    >  **します**。</span><span class="sxs-lookup"><span data-stu-id="93c8f-127">In the **Templates** list, choose **Visual C#** > **Office/SharePoint** > **Add-ins** > **Add-in for SharePoint 2013**.</span></span>
    
4. <span data-ttu-id="93c8f-128">アドインに GetProjectIdAddinPart という名前を付け **、[OK] ボタンを選択** します。</span><span class="sxs-lookup"><span data-stu-id="93c8f-128">Name the add-in GetProjectIdAddinPart, and then choose the **OK** button.</span></span> 
    
5. <span data-ttu-id="93c8f-129">[新 **しい** アドインを作成SharePoint] ダイアログ ボックスに、デバッグに使用する PWA サイトの URL を入力します (例: _https://contoso.com/sites/pwasite/_ )。</span><span class="sxs-lookup"><span data-stu-id="93c8f-129">In the **New add-in for SharePoint** dialog box, enter the URL of the PWA site that you want to use for debugging (for example:  _https://contoso.com/sites/pwasite/_).</span></span>
    
6. <span data-ttu-id="93c8f-130">[ホスト **SharePoint] オプション** を選択してアドインをホストし、[完了] ボタン **を選択** します。</span><span class="sxs-lookup"><span data-stu-id="93c8f-130">Choose the **SharePoint-hosted** option to host your add-in, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="93c8f-131">ソリューション **エクスプローラーで、GetProjectIdAddinPart** プロジェクトのショートカット メニューを開き、[新しいアイテムの追加]  >  **を選択します**。</span><span class="sxs-lookup"><span data-stu-id="93c8f-131">In **Solution Explorer**, open the shortcut menu for the GetProjectIdAddinPart project, and then choose **Add** > **New Item**.</span></span>
    
8. <span data-ttu-id="93c8f-132">[新しい **アイテムの追加** ] ダイアログ ボックスで、[クライアント Web パーツ **(Host Web)]** を選択し、Web パーツに GetProjectId という名前を付け、[追加] ボタン **を選択** します。</span><span class="sxs-lookup"><span data-stu-id="93c8f-132">In the **Add New Item** dialog box, choose **Client web part (Host Web)**, name the web part GetProjectId, and then choose the **Add** button.</span></span> 
    
9. <span data-ttu-id="93c8f-133">[クライアント **Web パーツの作成** ] ダイアログ ボックスで、[新しいクライアント Web パーツ ページの作成] オプションを **選択** し、[完了] ボタン **を選択** します。</span><span class="sxs-lookup"><span data-stu-id="93c8f-133">In the **Create Client web part** dialog box, choose the **Create a new client web part page** option, and then choose the **Finish** button.</span></span> 
    
## <a name="get-the-project-id-in-the-add-in-part"></a><span data-ttu-id="93c8f-134">アドイン パーツでプロジェクト ID を取得する</span><span class="sxs-lookup"><span data-stu-id="93c8f-134">Get the project ID in the add-in part</span></span>
<span data-ttu-id="93c8f-135"><a name="GetProjectId"> </a></span><span class="sxs-lookup"><span data-stu-id="93c8f-135"><a name="GetProjectId"> </a></span></span>

<span data-ttu-id="93c8f-136">GetProjectId アドイン パーツは、クライアント Web パーツの GetProjectId.aspx ページでカスタム コードを定義します。</span><span class="sxs-lookup"><span data-stu-id="93c8f-136">The GetProjectId add-in part defines its custom code in the GetProjectId.aspx page of the client web part.</span></span> <span data-ttu-id="93c8f-137">メッセージを受信して処理するロジックは、ページの **head** 要素で定義され、ページ コントロールはページの **body** 要素で定義されます。</span><span class="sxs-lookup"><span data-stu-id="93c8f-137">The logic that receives and handles the message is defined in the **head** element of the page and the page controls are defined in the **body** element of the page.</span></span> 
  
1. <span data-ttu-id="93c8f-138">GetProjectId.aspx Web パーツ ページ (Pages フォルダー内) **を開** きます。</span><span class="sxs-lookup"><span data-stu-id="93c8f-138">Open the GetProjectId.aspx web part page (in the **Pages** folder).</span></span> 
    
2. <span data-ttu-id="93c8f-139">ページの **head** 要素で、スクリプト タグ間のコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="93c8f-139">In the **head** element of the page, replace the code between the **script** tags with the following code.</span></span> 
    
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

3. <span data-ttu-id="93c8f-140">ページの body 要素に次 **の** コードを追加します。</span><span class="sxs-lookup"><span data-stu-id="93c8f-140">Add the following code in the **body** element of the page.</span></span> <span data-ttu-id="93c8f-141">このコードは、プロジェクト ID を表示するスパン コントロールを定義します。</span><span class="sxs-lookup"><span data-stu-id="93c8f-141">The code defines a span control that displays the project ID.</span></span> 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. <span data-ttu-id="93c8f-142">このファイルElements.xml必要に応じて、アドイン パーツの名前、タイトル、説明、および既定のサイズを変更します。</span><span class="sxs-lookup"><span data-stu-id="93c8f-142">In the Elements.xml file, optionally change the name, title, description, and default size of the add-in part.</span></span> <span data-ttu-id="93c8f-143">この例では、既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="93c8f-143">This example uses the default values.</span></span>
    
5. <span data-ttu-id="93c8f-144">アドイン パーツをテストするには、メニュー バーで [デバッグ] 、[ **デバッグ** の開始] **を選択します**。</span><span class="sxs-lookup"><span data-stu-id="93c8f-144">To test the add-in part, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="93c8f-145">web.config ファイルを変更するように求められた場合は、[ **OK**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="93c8f-145">If you're prompted to modify the web.config file, choose the **OK** button.</span></span> 
    
   <span data-ttu-id="93c8f-146">アドイン パーツをデバッグするには、追加したスクリプトに適切なブレークポイントを設定します。</span><span class="sxs-lookup"><span data-stu-id="93c8f-146">To debug the add-in part, set appropriate breakpoints in the script that you added.</span></span>
    
6. <span data-ttu-id="93c8f-147">PDP ページを参照し、[ **ツール]** メニュー (歯車アイコン) から [ページの編集] を選択します。</span><span class="sxs-lookup"><span data-stu-id="93c8f-147">Browse to a PDP page and choose **Edit page** from the Tools menu (gear icon).</span></span> 
    
7. <span data-ttu-id="93c8f-148">ページ上 **の Web パーツに GetProjectId Title** パーツを追加します。</span><span class="sxs-lookup"><span data-stu-id="93c8f-148">Add the **GetProjectId Title** part to a web part on the page.</span></span> <span data-ttu-id="93c8f-149">プロジェクト ID は、Web パーツ **ページの span** コントロールに表示されます。</span><span class="sxs-lookup"><span data-stu-id="93c8f-149">The project ID displays in the **span** control on the web part page.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="93c8f-150">次の手順</span><span class="sxs-lookup"><span data-stu-id="93c8f-150">Next steps</span></span>
<span data-ttu-id="93c8f-151"><a name="NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="93c8f-151"><a name="NextSteps"> </a></span></span>

<span data-ttu-id="93c8f-152">この例のアドイン パーツは、サーバー データまたはサーバー データProjectアクセスSharePointしません。</span><span class="sxs-lookup"><span data-stu-id="93c8f-152">The add-in part in this example doesn't access Project Server data or SharePoint data.</span></span> <span data-ttu-id="93c8f-153">製品 ID を使用して、JavaScript オブジェクト モデルや REST サービスなどのクライアント API を使用して、現在のプロジェクトに関する情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="93c8f-153">You can use the product ID to get information about the current project by using a client API, such as the JavaScript object model or the REST service.</span></span>
  
<span data-ttu-id="93c8f-154">このファイルAppManifest.xml、アドインがサーバー データまたはサーバー データにアクセスするために必要Projectアクセス許可SharePointします。</span><span class="sxs-lookup"><span data-stu-id="93c8f-154">In the AppManifest.xml file, specify the permissions that your add-in needs to access Project Server data or SharePoint data.</span></span> 
  
<span data-ttu-id="93c8f-155">アドイン[パーツのカスタム プロパティを設定する方法については、「create add-in](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) parts to install with your SharePoint アドイン」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93c8f-155">See [Create add-in parts to install with your SharePoint Add-in](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) to learn how to set custom properties for an add-in part.</span></span> 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a><span data-ttu-id="93c8f-156">例: PDP ページのアドイン パーツでプロジェクト ID を取得する</span><span class="sxs-lookup"><span data-stu-id="93c8f-156">Example: Getting the project ID in an add-in part on a PDP page</span></span>
<span data-ttu-id="93c8f-157"><a name="CodeExample"> </a></span><span class="sxs-lookup"><span data-stu-id="93c8f-157"><a name="CodeExample"> </a></span></span>

<span data-ttu-id="93c8f-158">次の例は、クライアント Web パーツの GetProjectID.aspx ページの完全なコードです。</span><span class="sxs-lookup"><span data-stu-id="93c8f-158">The following example is the complete code in the client web part's GetProjectID.aspx page.</span></span> <span data-ttu-id="93c8f-159">このコードは、プロジェクト ID を含むメッセージを受信して解析するイベント リスナーとイベント ハンドラーを登録します。</span><span class="sxs-lookup"><span data-stu-id="93c8f-159">The code registers an event listener and an event handler that receives and parses a message that contains the project ID.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="93c8f-160">関連項目</span><span class="sxs-lookup"><span data-stu-id="93c8f-160">See also</span></span>

- [<span data-ttu-id="93c8f-161">Project のプログラミング タスク</span><span class="sxs-lookup"><span data-stu-id="93c8f-161">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="93c8f-162">SharePoint をホストとする Project Server アドインを作成する</span><span class="sxs-lookup"><span data-stu-id="93c8f-162">Create a SharePoint-hosted Project Server add-in</span></span>](create-a-sharepoint-hosted-project-server-add-in.md)
- [<span data-ttu-id="93c8f-163">アドイン パーツを作成して SharePoint アドインと共にインストールする</span><span class="sxs-lookup"><span data-stu-id="93c8f-163">Create add-in parts to install with your SharePoint Add-in</span></span>](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

