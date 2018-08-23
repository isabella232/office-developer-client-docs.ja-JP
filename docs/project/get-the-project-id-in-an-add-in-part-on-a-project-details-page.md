---
title: プロジェクト詳細ページのアドインの部分でプロジェクト ID を取得する
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: パーツの追加では、ホスト ページから完全に隔離されている iframe 要素内でホストされています。 プロジェクト詳細ページ (PDP) に追加のパーツから現在のプロジェクトに関する情報を取得するには、window.postMessage メソッド、イベント ・ リスナー、およびメッセージからのプロジェクト ID を解析するイベント ハンドラーを使用できます。
ms.openlocfilehash: 6704dae7ded385f86d2da47a1334ae4c81622a74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804542"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a><span data-ttu-id="33e4c-104">プロジェクト詳細ページのアドインの部分でプロジェクト ID を取得する</span><span class="sxs-lookup"><span data-stu-id="33e4c-104">Get the project ID in an add-in part on a Project Details Page</span></span>

<span data-ttu-id="33e4c-105">パーツの追加では、ホスト ページから完全に隔離されている**iframe**要素内でホストされています。</span><span class="sxs-lookup"><span data-stu-id="33e4c-105">Add-in parts are hosted in **iframe** elements that are fully isolated from the hosting page.</span></span> <span data-ttu-id="33e4c-106">プロジェクト詳細ページ (PDP) に追加のパーツから現在のプロジェクトに関する情報を取得するには、 **window.postMessage**メソッド、イベント ・ リスナー、およびメッセージからのプロジェクト ID を解析するイベント ハンドラーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="33e4c-106">To get information about the current project from an add-in part on Project Details Page (PDP), you can use the **window.postMessage** method, an event listener, and an event handler that parses out the project ID from the message.</span></span> 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a><span data-ttu-id="33e4c-107">パーツを作成する SharePoint でホストされているアドインのプロジェクト ID を取得するための前提条件</span><span class="sxs-lookup"><span data-stu-id="33e4c-107">Prerequisites for creating a SharePoint-hosted add-in part that gets the project ID</span></span>
<span data-ttu-id="33e4c-108"><a name="Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="33e4c-108"></span></span>

<span data-ttu-id="33e4c-109">この資料のコード例を使用するのには次のいずれかの方法が必要です。</span><span class="sxs-lookup"><span data-stu-id="33e4c-109">To use the code example in this article, you'll need either of the following:</span></span>
  
- <span data-ttu-id="33e4c-110">SharePoint 2013 と Project Server 2013、アドインの分離用に構成します。</span><span class="sxs-lookup"><span data-stu-id="33e4c-110">SharePoint 2013 and Project Server 2013, configured for add-in isolation.</span></span> <span data-ttu-id="33e4c-111">リモートで、開発する場合、サーバーは、アドインの sideloading をサポートする必要がありますか、開発者向けサイトからアドインをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="33e4c-111">If you're developing remotely, the server must support sideloading of add-ins or you must install the add-in on a Developer Site.</span></span>
  
- <span data-ttu-id="33e4c-112">オンラインの SharePoint とオンラインのプロジェクト</span><span class="sxs-lookup"><span data-stu-id="33e4c-112">SharePoint Online and Project Online</span></span>
    
    - <span data-ttu-id="33e4c-113">Visual Studio 2013、2013 年 Visual Studio または Napa のツールの Office 開発者が Visual Studio 2012 の</span><span class="sxs-lookup"><span data-stu-id="33e4c-113">Visual Studio 2013, Visual Studio 2012 with Office Developer Tools for Visual Studio 2013, or Napa</span></span>
        
    - <span data-ttu-id="33e4c-114">ログオン ユーザーの次の十分なアクセス許可。</span><span class="sxs-lookup"><span data-stu-id="33e4c-114">Sufficient permissions for the logged-on user:</span></span>
        
        - <span data-ttu-id="33e4c-115">開発用コンピュータのローカル管理者権限。</span><span class="sxs-lookup"><span data-stu-id="33e4c-115">Local administrator permissions on the development computer.</span></span>
            
        - <span data-ttu-id="33e4c-116">少なくとも 1 つのプロジェクトへの読み取りアクセスします。</span><span class="sxs-lookup"><span data-stu-id="33e4c-116">Read access to at least one project.</span></span>
            
        - <span data-ttu-id="33e4c-117">Project Web App サイト上のページを編集するのにはアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="33e4c-117">Permission to edit pages on the Project Web App site.</span></span>
            
        - <span data-ttu-id="33e4c-118">システム アカウント以外のユーザーとしてログオンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="33e4c-118">You must be logged on as someone other than the system account.</span></span> <span data-ttu-id="33e4c-119">システム アカウントには、アドインをインストールする権限がありません。</span><span class="sxs-lookup"><span data-stu-id="33e4c-119">The system account does not have permission to install an add-in.</span></span>
    
<span data-ttu-id="33e4c-120">詳細については、アドイン プロジェクトを[Project Server 2013 のアドインを作成するための前提条件](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33e4c-120">See [Prerequisites for creating an add-in for Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites) for more information about add-ins for Project.</span></span> <span data-ttu-id="33e4c-121">設置型のセットアップ (必要な場合は、ループバック チェックを無効にする方法を含む) に関するガイダンスについては[、設置型の開発環境の SharePoint のアドインの設定](http://msdn.microsoft.com/library/b0878c12-27c9-4eea-ae3b-7e79e5a8838d%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33e4c-121">See [Set up an on-premises development environment for SharePoint Add-ins](http://msdn.microsoft.com/library/b0878c12-27c9-4eea-ae3b-7e79e5a8838d%28Office.15%29.aspx) for guidance about on-premises setup (including how to disable the loopback check, if necessary).</span></span> <span data-ttu-id="33e4c-122">リモートで、開発する場合は、[リモート システム上の SharePoint の開発のアプリケーション](http://msdn.microsoft.com/library/bf35d59c-9b84-42e5-877e-fa6881a7b6fc%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33e4c-122">If you're developing remotely, see [Developing apps for SharePoint on a remote system](http://msdn.microsoft.com/library/bf35d59c-9b84-42e5-877e-fa6881a7b6fc%28Office.15%29.aspx).</span></span>
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a><span data-ttu-id="33e4c-123">SharePoint でホストされているアドインの追加とクライアントの web パーツを作成します。</span><span class="sxs-lookup"><span data-stu-id="33e4c-123">Create the SharePoint-hosted add-in and client web part</span></span>
<span data-ttu-id="33e4c-124"><a name="CreateApp"> </a></span><span class="sxs-lookup"><span data-stu-id="33e4c-124"></span></span>

1. <span data-ttu-id="33e4c-125">Visual Studio を開き、**ファイル**を選択して > **新規** > **プロジェクト**。</span><span class="sxs-lookup"><span data-stu-id="33e4c-125">Open Visual Studio and choose **File** > **New** > **Project**.</span></span>
    
2. <span data-ttu-id="33e4c-126">[ **新しいプロジェクト**] ダイアログ ボックスで、上部のドロップダウン リストから [ **.NET Framework 4.5**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="33e4c-126">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
3. <span data-ttu-id="33e4c-127">**テンプレート**] の一覧で次のように選択**Visual C#** > **Office**SharePoint/ > **アドイン** > **SharePoint 2013 用のアドイン**です。</span><span class="sxs-lookup"><span data-stu-id="33e4c-127">In the **Templates** list, choose **Visual C#** > **Office/SharePoint** > **Add-ins** > **Add-in for SharePoint 2013**.</span></span>
    
4. <span data-ttu-id="33e4c-128">追加で GetProjectIdAddinPart では、名前を指定し、 **[OK** ] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="33e4c-128">Name the add-in GetProjectIdAddinPart, and then choose the **OK** button.</span></span> 
    
5. <span data-ttu-id="33e4c-129">**新しいアドイン SharePoint の**保存ダイアログ ボックスで、デバッグに使用する、PWA サイトの URL を入力します (例: _https://contoso.com/sites/pwasite/_)。</span><span class="sxs-lookup"><span data-stu-id="33e4c-129">In the **New add-in for SharePoint** dialog box, enter the URL of the PWA site that you want to use for debugging (for example:  _https://contoso.com/sites/pwasite/_).</span></span>
    
6. <span data-ttu-id="33e4c-130">アドインをホストする**SharePoint でホストされている**オプションを選択し、し、 **[完了**] ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="33e4c-130">Choose the **SharePoint-hosted** option to host your add-in, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="33e4c-131">**ソリューション エクスプ ローラー**で、GetProjectIdAddinPart プロジェクトのショートカット メニューを表示し、[**追加** > **[新しい項目**のします。</span><span class="sxs-lookup"><span data-stu-id="33e4c-131">In **Solution Explorer**, open the shortcut menu for the GetProjectIdAddinPart project, and then choose **Add** > **New Item**.</span></span>
    
8. <span data-ttu-id="33e4c-132">**新しい項目の追加**] ダイアログ ボックスで、**クライアント web パーツ (Web のホスト)** を選択、GetProjectId、web パーツの名前で **[追加**] ボタンを選択し。</span><span class="sxs-lookup"><span data-stu-id="33e4c-132">In the **Add New Item** dialog box, choose **Client web part (Host Web)**, name the web part GetProjectId, and then choose the **Add** button.</span></span> 
    
9. <span data-ttu-id="33e4c-133">**Web パーツの [クライアント作成**] ダイアログ ボックスで、**新しいクライアント web パーツ ページの作成**] オプションを選択し、 **[完了**] ボタンを選択し。</span><span class="sxs-lookup"><span data-stu-id="33e4c-133">In the **Create Client web part** dialog box, choose the **Create a new client web part page** option, and then choose the **Finish** button.</span></span> 
    
## <a name="get-the-project-id-in-the-add-in-part"></a><span data-ttu-id="33e4c-134">アドインの一部で、プロジェクト ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="33e4c-134">Get the project ID in the add-in part</span></span>
<span data-ttu-id="33e4c-135"><a name="GetProjectId"> </a></span><span class="sxs-lookup"><span data-stu-id="33e4c-135"></span></span>

<span data-ttu-id="33e4c-136">GetProjectId アドインの一部では、クライアントの web パーツの [GetProjectId.aspx] ページで、カスタム コードを定義します。</span><span class="sxs-lookup"><span data-stu-id="33e4c-136">The GetProjectId add-in part defines its custom code in the GetProjectId.aspx page of the client web part.</span></span> <span data-ttu-id="33e4c-137">受信し、メッセージを処理するロジックがページの**head**要素で定義されているし、ページのコントロールがページの**body**要素で定義されています。</span><span class="sxs-lookup"><span data-stu-id="33e4c-137">The logic that receives and handles the message is defined in the **head** element of the page and the page controls are defined in the **body** element of the page.</span></span> 
  
1. <span data-ttu-id="33e4c-138">(フォルダー内の**ページ**) には、GetProjectId.aspx web パーツ ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="33e4c-138">Open the GetProjectId.aspx web part page (in the **Pages** folder).</span></span> 
    
2. <span data-ttu-id="33e4c-139">ページの**head**要素を次のコードを含む**スクリプト**タグの間のコードを置き換えます。</span><span class="sxs-lookup"><span data-stu-id="33e4c-139">In the **head** element of the page, replace the code between the **script** tags with the following code.</span></span> 
    
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

3. <span data-ttu-id="33e4c-140">ページの**body**要素内には、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="33e4c-140">Add the following code in the **body** element of the page.</span></span> <span data-ttu-id="33e4c-141">コードは、プロジェクト ID を表示する span コントロールを定義します。</span><span class="sxs-lookup"><span data-stu-id="33e4c-141">The code defines a span control that displays the project ID.</span></span> 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. <span data-ttu-id="33e4c-142">Elements.xml ファイルに、名前、タイトル、説明、およびアドインの一部の既定のサイズを必要に応じて変更します。</span><span class="sxs-lookup"><span data-stu-id="33e4c-142">In the Elements.xml file, optionally change the name, title, description, and default size of the add-in part.</span></span> <span data-ttu-id="33e4c-143">この例では、既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="33e4c-143">This example uses the default values.</span></span>
    
5. <span data-ttu-id="33e4c-144">アドインの一部をメニュー バーの [をテストするのには、**デバッグ**、**デバッグの開始**を選択します。</span><span class="sxs-lookup"><span data-stu-id="33e4c-144">To test the add-in part, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="33e4c-145">Web.config ファイルを変更するメッセージが表示されたら、 **[OK** ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="33e4c-145">If you're prompted to modify the web.config file, choose the **OK** button.</span></span> 
    
   <span data-ttu-id="33e4c-146">アドインの一部をデバッグするには、追加したスクリプトで適切なブレークポイントを設定します。</span><span class="sxs-lookup"><span data-stu-id="33e4c-146">To debug the add-in part, set appropriate breakpoints in the script that you added.</span></span>
    
6. <span data-ttu-id="33e4c-147">PDP のページを参照し、(歯車アイコン) の [ツール] メニューから [**ページの編集**」を選択します。</span><span class="sxs-lookup"><span data-stu-id="33e4c-147">Browse to a PDP page and choose **Edit page** from the Tools menu (gear icon).</span></span> 
    
7. <span data-ttu-id="33e4c-148">**GetProjectId タイトル**の一部をページ上の web パーツに追加します。</span><span class="sxs-lookup"><span data-stu-id="33e4c-148">Add the **GetProjectId Title** part to a web part on the page.</span></span> <span data-ttu-id="33e4c-149">プロジェクト ID は、web パーツ ページの**span**コントロールに表示します。</span><span class="sxs-lookup"><span data-stu-id="33e4c-149">The project ID displays in the **span** control on the web part page.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="33e4c-150">次の手順</span><span class="sxs-lookup"><span data-stu-id="33e4c-150">Next steps</span></span>
<span data-ttu-id="33e4c-151"><a name="NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="33e4c-151"></span></span>

<span data-ttu-id="33e4c-152">この例ではアドインの一部は Project Server のデータ、または SharePoint データにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="33e4c-152">The add-in part in this example doesn't access Project Server data or SharePoint data.</span></span> <span data-ttu-id="33e4c-153">プロダクト ID を使用すると、JavaScript オブジェクト モデルまたは REST サービスなどのクライアント API を使用して、現在のプロジェクトに関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="33e4c-153">You can use the product ID to get information about the current project by using a client API, such as the JavaScript object model or the REST service.</span></span>
  
<span data-ttu-id="33e4c-154">AppManifest.xml ファイルで、アドインを Project Server のデータ、または SharePoint データにアクセスする必要があるアクセス許可を指定します。</span><span class="sxs-lookup"><span data-stu-id="33e4c-154">In the AppManifest.xml file, specify the permissions that your add-in needs to access Project Server data or SharePoint data.</span></span> 
  
<span data-ttu-id="33e4c-155">追加のパーツのカスタム プロパティを設定する方法については[、SharePoint アドインを使用してインストールするのには追加でパーツを作成](http://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33e4c-155">See [Create add-in parts to install with your SharePoint Add-in](http://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) to learn how to set custom properties for an add-in part.</span></span> 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a><span data-ttu-id="33e4c-156">例: [PDP] ページで、アドインの一部で、プロジェクト ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="33e4c-156">Example: Getting the project ID in an add-in part on a PDP page</span></span>
<span data-ttu-id="33e4c-157"><a name="CodeExample"> </a></span><span class="sxs-lookup"><span data-stu-id="33e4c-157"></span></span>

<span data-ttu-id="33e4c-158">次の使用例は、クライアントの web パーツの GetProjectID.aspx のページの完全なコードです。</span><span class="sxs-lookup"><span data-stu-id="33e4c-158">The following example is the complete code in the client web part's GetProjectID.aspx page.</span></span> <span data-ttu-id="33e4c-159">イベント ・ リスナーとを受信し、プロジェクトの ID を含むメッセージを解析し、イベント ハンドラーを登録するコードを</span><span class="sxs-lookup"><span data-stu-id="33e4c-159">The code registers an event listener and an event handler that receives and parses a message that contains the project ID.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="33e4c-160">関連項目</span><span class="sxs-lookup"><span data-stu-id="33e4c-160">See also</span></span>

- [<span data-ttu-id="33e4c-161">Project のプログラミング タスク</span><span class="sxs-lookup"><span data-stu-id="33e4c-161">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="33e4c-162">SharePoint をホストとする Project Server アドインを作成する</span><span class="sxs-lookup"><span data-stu-id="33e4c-162">Create a SharePoint-hosted Project Server add-in</span></span>](create-a-sharepoint-hosted-project-server-add-in.md)
- [<span data-ttu-id="33e4c-163">アドイン パーツを作成して SharePoint アドインと共にインストールする</span><span class="sxs-lookup"><span data-stu-id="33e4c-163">Create add-in parts to install with your SharePoint Add-in</span></span>](http://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

