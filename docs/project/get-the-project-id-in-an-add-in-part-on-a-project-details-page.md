---
title: プロジェクト詳細ページのアドインの部分でプロジェクト ID を取得する
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 009cd997-c7e5-4078-b495-c40caa29a5fb
description: アドイン パーツは、ホスティング ページから完全に分離された iframe 要素でホストされます。 Project 詳細ページ (PDP) のアドイン パーツから現在のプロジェクトに関する情報を取得するには、window.postMessage メソッド、イベント リスナー、およびメッセージからプロジェクト ID を解析するイベント ハンドラーを使用できます。
ms.openlocfilehash: 78851a6008157741ed489ce8b3868497823d48d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623559"
---
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a>プロジェクト詳細ページのアドインの部分でプロジェクト ID を取得する

アドイン パーツは、ホスティング ページから完全に分離された **iframe** 要素でホストされます。 Project 詳細ページ (PDP) のアドイン パーツから現在のプロジェクトに関する情報を取得するには **、window.postMessage** メソッド、イベント リスナー、およびメッセージからプロジェクト ID を解析するイベント ハンドラーを使用できます。 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a>プロジェクト ID を取得するSharePointホスト型アドイン パーツを作成するための前提条件
<a name="Prereqs"> </a>

この記事のコード例を使用するには、次のどちらかが必要です。
  
- SharePoint分離用にProject 2013 およびサーバー 2013 を使用します。 リモートで開発する場合、サーバーはアドインのサイドローディングをサポートするか、開発者サイトにアドインをインストールする必要があります。
  
- SharePointオンラインとProject Online
    
    - Visual Studio 2013 2012 Visual Studio 2012 Office開発者向けツール、Visual Studio 2013 Napa
        
    - ログオン ユーザーの次の十分なアクセス許可。
        
        - 開発用コンピュータのローカル管理者権限。
            
        - 少なくとも 1 つのプロジェクトへの読み取りアクセス。
            
        - サイト上のページを編集Project Web Appアクセス許可。
            
        - システム アカウント以外の誰かとしてログオンする必要があります。 システム アカウントには、アドインをインストールするアクセス許可が付与されません。
    
詳細[については、「Project Server 2013](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites)のアドインを作成するための前提条件」を参照Project。 オンプレミス[のセットアップに関するガイダンスについては、「SharePoint](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins)アドインのオンプレミスの開発環境をセットアップする(必要に応じてループバック チェックを無効にする方法を含む)」を参照してください。 リモートで開発する場合は、「リモート システムでのアプリの開発[SharePointを参照してください](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins)。
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a>ホストされるSharePointクライアント Web パーツを作成する
<a name="CreateApp"> </a>

1. [ファイルVisual Studio開き、[**ファイル** の新  >  **しいファイル] を**  >  **Project。**
    
2. [ **新しいプロジェクト**] ダイアログ ボックスで、上部のドロップダウン リストから [ **.NET Framework 4.5**] を選択します。 
    
3. [テンプレート **] リスト** で  >  、[2013 **Visual C#Office/SharePoint** アドイン アドイン] を選択SharePoint  >    >  **します**。
    
4. アドインに GetProjectIdAddinPart という名前を付け **、[OK] ボタンを選択** します。 
    
5. [新 **しい** アドインを作成SharePoint] ダイアログ ボックスに、デバッグに使用する PWA サイトの URL を入力します (例: _https://contoso.com/sites/pwasite/_ )。
    
6. [ホスト **SharePoint] オプション** を選択してアドインをホストし、[完了] ボタン **を選択** します。 
    
7. ソリューション **エクスプローラーで、GetProjectIdAddinPart** プロジェクトのショートカット メニューを開き、[新しいアイテムの追加]  >  **を選択します**。
    
8. [新しい **アイテムの追加** ] ダイアログ ボックスで、[クライアント Web パーツ **(Host Web)]** を選択し、Web パーツに GetProjectId という名前を付け、[追加] ボタン **を選択** します。 
    
9. [クライアント **Web パーツの作成** ] ダイアログ ボックスで、[新しいクライアント Web パーツ ページの作成] オプションを **選択** し、[完了] ボタン **を選択** します。 
    
## <a name="get-the-project-id-in-the-add-in-part"></a>アドイン パーツでプロジェクト ID を取得する
<a name="GetProjectId"> </a>

GetProjectId アドイン パーツは、クライアント Web パーツの GetProjectId.aspx ページでカスタム コードを定義します。 メッセージを受信して処理するロジックは、ページの **head** 要素で定義され、ページ コントロールはページの **body** 要素で定義されます。 
  
1. GetProjectId.aspx Web パーツ ページ (Pages フォルダー内) **を開** きます。 
    
2. ページの **head** 要素で、スクリプト タグ間のコードを次のコードに置き換えます。 
    
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

3. ページの body 要素に次 **の** コードを追加します。 このコードは、プロジェクト ID を表示するスパン コントロールを定義します。 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. このファイルElements.xml必要に応じて、アドイン パーツの名前、タイトル、説明、および既定のサイズを変更します。 この例では、既定値を使用します。
    
5. アドイン パーツをテストするには、メニュー バーで [デバッグ] 、[ **デバッグ** の開始] **を選択します**。 web.config ファイルを変更するように求められた場合は、[ **OK**] ボタンをクリックします。 
    
   アドイン パーツをデバッグするには、追加したスクリプトに適切なブレークポイントを設定します。
    
6. PDP ページを参照し、[ **ツール]** メニュー (歯車アイコン) から [ページの編集] を選択します。 
    
7. ページ上 **の Web パーツに GetProjectId Title** パーツを追加します。 プロジェクト ID は、Web パーツ **ページの span** コントロールに表示されます。 
    
## <a name="next-steps"></a>次の手順
<a name="NextSteps"> </a>

この例のアドイン パーツは、サーバー データまたはサーバー データProjectアクセスSharePointしません。 製品 ID を使用して、JavaScript オブジェクト モデルや REST サービスなどのクライアント API を使用して、現在のプロジェクトに関する情報を取得できます。
  
このファイルAppManifest.xml、アドインがサーバー データまたはサーバー データにアクセスするために必要Projectアクセス許可SharePointします。 
  
アドイン[パーツのカスタム プロパティを設定する方法については、「create add-in](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx) parts to install with your SharePoint アドイン」を参照してください。 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a>例: PDP ページのアドイン パーツでプロジェクト ID を取得する
<a name="CodeExample"> </a>

次の例は、クライアント Web パーツの GetProjectID.aspx ページの完全なコードです。 このコードは、プロジェクト ID を含むメッセージを受信して解析するイベント リスナーとイベント ハンドラーを登録します。
  
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

## <a name="see-also"></a>関連項目

- [Project のプログラミング タスク](project-programming-tasks.md)
- [SharePoint をホストとする Project Server アドインを作成する](create-a-sharepoint-hosted-project-server-add-in.md)
- [アドイン パーツを作成して SharePoint アドインと共にインストールする](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

