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
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a>プロジェクト詳細ページのアドインの部分でプロジェクト ID を取得する

アドインパーツは、ホスティングページから完全に分離された**iframe**要素にホストされます。 プロジェクト詳細ページ (PDP) のアドインパーツから現在のプロジェクトに関する情報を取得するには、 **postMessage**メソッド、イベントリスナー、およびメッセージからプロジェクト ID を解析するイベントハンドラーを使用できます。 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a>プロジェクト ID を取得する SharePoint ホスト型アドインパーツを作成するための前提条件
<a name="Prereqs"> </a>

この記事のコード例を使用するには、次のいずれかが必要になります。
  
- SharePoint 2013 および Project Server 2013。アドイン分離用に構成されています。 リモートで開発している場合、サーバーはアドインのサイドロードをサポートする必要があります。または、開発者向けサイトにアドインをインストールする必要があります。
  
- SharePoint online と Project online
    
    - visual studio 2013、visual studio 2012 (Office Developer Tools for visual studio 2013、または Napa
        
    - ログオン ユーザーの次の十分なアクセス許可。
        
        - 開発用コンピュータのローカル管理者権限。
            
        - 少なくとも1つのプロジェクトへの読み取りアクセス権。
            
        - Project Web App サイトのページを編集する権限。
            
        - システム アカウント以外の誰かとしてログオンする必要があります。 システムアカウントにアドインをインストールする権限がありません。
    
project 用アドインの詳細については、「project [Server 2013 用のアドインを作成するための前提条件](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites)」を参照してください。 オンプレミスの設定 (必要に応じてループバックチェックを無効にする方法を含む) に関するガイダンスについては[、「SharePoint アドインのオンプレミスの開発環境をセットアップ](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/set-up-an-on-premises-development-environment-for-sharepoint-add-ins)する」を参照してください。 リモートで開発している場合は、「[リモートシステムで SharePoint 用アプリを開発](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/develop-sharepoint-add-ins)する」を参照してください。
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a>SharePoint ホスト型アドインとクライアント web パーツを作成する
<a name="CreateApp"> </a>

1. Visual Studio を開き、[**ファイル** > ] [**新しい** > **プロジェクト**] の順に選択します。
    
2. [ **新しいプロジェクト**] ダイアログ ボックスで、上部のドロップダウン リストから [ **.NET Framework 4.5**] を選択します。 
    
3. [**テンプレート**] リストで、[ **Visual C#** > **Office/sharepoint** > **アドイン** > **アドイン (sharepoint 用) 2013**] を選択します。
    
4. アドインに GetProjectIdAddinPart という名前を指定し、[ **OK** ] ボタンをクリックします。 
    
5. [ **SharePoint 用アドインの新規作成**] ダイアログボックスで、デバッグに使用する PWA サイトの URL を入力します (例: _https://contoso.com/sites/pwasite/_)。
    
6. [ **SharePoint ホスト型**] オプションを選択してアドインをホストし、[**完了**] ボタンをクリックします。 
    
7. **ソリューションエクスプローラー**で、GetProjectIdAddinPart プロジェクトのショートカットメニューを開き、[**新しい項目**の**追加** > ] を選択します。
    
8. [**新しいアイテムの追加**] ダイアログボックスで、[**クライアント web パーツ (ホスト web)**] を選択し、web パーツ GetProjectId に名前を指定して、[**追加**] をクリックします。 
    
9. [**クライアント web パーツの作成**] ダイアログボックスで、[**新しいクライアント web パーツページを作成する**] オプションを選択し、[**完了**] ボタンをクリックします。 
    
## <a name="get-the-project-id-in-the-add-in-part"></a>アドインパーツのプロジェクト ID を取得する
<a name="GetProjectId"> </a>

GetProjectId アドインパーツは、クライアント web パーツの GetProjectId ページでカスタムコードを定義します。 メッセージを受け取って処理するロジックは、ページの**head**要素で定義され、ページコントロールはページの**body**要素で定義されます。 
  
1. GetProjectId web パーツページ ( **Pages**フォルダー内) を開きます。 
    
2. ページの**head**要素で、 **script**タグ間のコードを次のコードに置き換えます。 
    
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

3. ページの**body**要素に次のコードを追加します。 このコードでは、プロジェクト ID を表示する span コントロールを定義します。 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. Elements .xml ファイルで、必要に応じてアドインパーツの名前、タイトル、説明、および既定のサイズを変更します。 この例では、既定値を使用します。
    
5. アドインパーツをテストするには、メニューバーで [**デバッグ**] を選択し、**デバッグを開始**します。 web.config ファイルを変更するように求められた場合は、[ **OK**] ボタンをクリックします。 
    
   アドインパーツをデバッグするには、追加したスクリプトに適切なブレークポイントを設定します。
    
6. PDP ページに移動し、[ツール] メニュー (歯車アイコン) から [**ページの編集**] を選択します。 
    
7. **GetProjectId Title**パーツをページ上の web パーツに追加します。 プロジェクト ID が web パーツページの**span**コントロールに表示されます。 
    
## <a name="next-steps"></a>次の手順
<a name="NextSteps"> </a>

この例のアドインパーツは、Project Server データまたは SharePoint データにアクセスしません。 プロダクト ID を使用して、JavaScript オブジェクトモデル、REST サービスなど、クライアント API を使用して現在のプロジェクトに関する情報を取得できます。
  
appmanifest.xml ファイルで、アドインが Project Server データまたは SharePoint データにアクセスするために必要なアクセス許可を指定します。 
  
アドインパーツにカスタムプロパティを設定する方法については[、「アドインパーツを作成して SharePoint アドインと共にインストールする](https://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)」を参照してください。 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a>例: PDP ページでアドインパーツのプロジェクト ID を取得する
<a name="CodeExample"> </a>

次の例は、クライアント web パーツの GetProjectID ページの完全なコードです。 このコードでは、プロジェクト ID を含むメッセージを受け取って解析するイベントリスナーとイベントハンドラーを登録します。
  
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
    

