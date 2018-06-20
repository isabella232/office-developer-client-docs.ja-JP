---
title: プロジェクト詳細ページに追加する一部のプロジェクト ID を取得します。
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
# <a name="get-the-project-id-in-an-add-in-part-on-a-project-details-page"></a>プロジェクト詳細ページに追加する一部のプロジェクト ID を取得します。

パーツの追加では、ホスト ページから完全に隔離されている**iframe**要素内でホストされています。 プロジェクト詳細ページ (PDP) に追加のパーツから現在のプロジェクトに関する情報を取得するには、 **window.postMessage**メソッド、イベント ・ リスナー、およびメッセージからのプロジェクト ID を解析するイベント ハンドラーを使用できます。 
  
## <a name="prerequisites-for-creating-a-sharepoint-hosted-add-in-part-that-gets-the-project-id"></a>パーツを作成する SharePoint でホストされているアドインのプロジェクト ID を取得するための前提条件
<a name="Prereqs"> </a>

この資料のコード例を使用するのには次のいずれかの方法が必要です。
  
- SharePoint 2013 と Project Server 2013、アドインの分離用に構成します。 リモートで、開発する場合、サーバーは、アドインの sideloading をサポートする必要がありますか、開発者向けサイトからアドインをインストールする必要があります。
  
- オンラインの SharePoint とオンラインのプロジェクト
    
    - Visual Studio 2013、2013 年 Visual Studio または Napa のツールの Office 開発者が Visual Studio 2012 の
        
    - ログオン ユーザーの次の十分なアクセス許可。
        
        - 開発用コンピュータのローカル管理者権限。
            
        - 少なくとも 1 つのプロジェクトへの読み取りアクセスします。
            
        - Project Web App サイト上のページを編集するのにはアクセスを許可します。
            
        - システム アカウント以外のユーザーとしてログオンする必要があります。 システム アカウントには、アドインをインストールする権限がありません。
    
詳細については、アドイン プロジェクトを[Project Server 2013 のアドインを作成するための前提条件](create-a-sharepoint-hosted-project-server-add-in.md#pj15_StatusingApp_Prerequisites)を参照してください。 設置型のセットアップ (必要な場合は、ループバック チェックを無効にする方法を含む) に関するガイダンスについては[、設置型の開発環境の SharePoint のアドインの設定](http://msdn.microsoft.com/library/b0878c12-27c9-4eea-ae3b-7e79e5a8838d%28Office.15%29.aspx)を参照してください。 リモートで、開発する場合は、[リモート システム上の SharePoint の開発のアプリケーション](http://msdn.microsoft.com/library/bf35d59c-9b84-42e5-877e-fa6881a7b6fc%28Office.15%29.aspx)を参照してください。
  
## <a name="create-the-sharepoint-hosted-add-in-and-client-web-part"></a>SharePoint でホストされているアドインの追加とクライアントの web パーツを作成します。
<a name="CreateApp"> </a>

1. Visual Studio を開き、**ファイル**を選択して > **新規** > **プロジェクト**。
    
2. [ **新しいプロジェクト**] ダイアログ ボックスで、上部のドロップダウン リストから [ **.NET Framework 4.5**] を選択します。 
    
3. **テンプレート**] の一覧で次のように選択**Visual C#** > **Office**SharePoint/ > **アドイン** > **SharePoint 2013 用のアドイン**です。
    
4. 追加で GetProjectIdAddinPart では、名前を指定し、 **[OK** ] ボタンをクリックします。 
    
5. **新しいアドイン SharePoint の**保存ダイアログ ボックスで、デバッグに使用する、PWA サイトの URL を入力します (例: _https://contoso.com/sites/pwasite/_)。
    
6. アドインをホストする**SharePoint でホストされている**オプションを選択し、し、 **[完了**] ボタンを選択します。 
    
7. **ソリューション エクスプ ローラー**で、GetProjectIdAddinPart プロジェクトのショートカット メニューを表示し、[**追加** > **[新しい項目**のします。
    
8. **新しい項目の追加**] ダイアログ ボックスで、**クライアント web パーツ (Web のホスト)** を選択、GetProjectId、web パーツの名前で **[追加**] ボタンを選択し。 
    
9. **Web パーツの [クライアント作成**] ダイアログ ボックスで、**新しいクライアント web パーツ ページの作成**] オプションを選択し、 **[完了**] ボタンを選択し。 
    
## <a name="get-the-project-id-in-the-add-in-part"></a>アドインの一部で、プロジェクト ID を取得します。
<a name="GetProjectId"> </a>

GetProjectId アドインの一部では、クライアントの web パーツの [GetProjectId.aspx] ページで、カスタム コードを定義します。 受信し、メッセージを処理するロジックがページの**head**要素で定義されているし、ページのコントロールがページの**body**要素で定義されています。 
  
1. (フォルダー内の**ページ**) には、GetProjectId.aspx web パーツ ページを開きます。 
    
2. ページの**head**要素を次のコードを含む**スクリプト**タグの間のコードを置き換えます。 
    
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

3. ページの**body**要素内には、次のコードを追加します。 コードは、プロジェクト ID を表示する span コントロールを定義します。 
    
   ```HTML
    <p>The ID for this project is:</p>
    <span id="projectUid"></span>
   ```

4. Elements.xml ファイルに、名前、タイトル、説明、およびアドインの一部の既定のサイズを必要に応じて変更します。 この例では、既定値を使用します。
    
5. アドインの一部をメニュー バーの [をテストするのには、**デバッグ**、**デバッグの開始**を選択します。 Web.config ファイルを変更するメッセージが表示されたら、 **[OK** ] を選択します。 
    
   アドインの一部をデバッグするには、追加したスクリプトで適切なブレークポイントを設定します。
    
6. PDP のページを参照し、(歯車アイコン) の [ツール] メニューから [**ページの編集**」を選択します。 
    
7. **GetProjectId タイトル**の一部をページ上の web パーツに追加します。 プロジェクト ID は、web パーツ ページの**span**コントロールに表示します。 
    
## <a name="next-steps"></a>次の手順
<a name="NextSteps"> </a>

この例ではアドインの一部は Project Server のデータ、または SharePoint データにアクセスします。 プロダクト ID を使用すると、JavaScript オブジェクト モデルまたは REST サービスなどのクライアント API を使用して、現在のプロジェクトに関する情報を取得します。
  
AppManifest.xml ファイルで、アドインを Project Server のデータ、または SharePoint データにアクセスする必要があるアクセス許可を指定します。 
  
追加のパーツのカスタム プロパティを設定する方法については[、SharePoint アドインを使用してインストールするのには追加でパーツを作成](http://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)を参照してください。 
  
## <a name="example-getting-the-project-id-in-an-add-in-part-on-a-pdp-page"></a>例: [PDP] ページで、アドインの一部で、プロジェクト ID を取得します。
<a name="CodeExample"> </a>

次の使用例は、クライアントの web パーツの GetProjectID.aspx のページの完全なコードです。 イベント ・ リスナーとを受信し、プロジェクトの ID を含むメッセージを解析し、イベント ハンドラーを登録するコードを
  
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

- [プロジェクトのプログラミング タスク](project-programming-tasks.md)
- [Project Server の SharePoint でホストされているアドインの作成します。](create-a-sharepoint-hosted-project-server-add-in.md)
- [アドイン パーツを作成して SharePoint アドインと共にインストールする](http://msdn.microsoft.com/library/a2664289-6c56-4cb1-987a-22367fad55eb%28Office.15%29.aspx)
    

