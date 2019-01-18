---
title: アドレス帳のコマンド ボタン
TOCTitle: Address Book command buttons
ms:assetid: bcea6f53-3e36-b067-03c2-b157ed02d41d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249908(v=office.15)
ms:contentKeyID: 48547422
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 09f2513a3c541c76352e773f7f2a8f0c24f78850
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700305"
---
# <a name="address-book-command-buttons"></a>アドレス帳のコマンド ボタン


**適用されます**Access 2013、Office 2013。


アドレス帳アプリケーションには次のコマンド ボタンがあります。

- クエリをデータベースに送信するための **[検索]** ボタン。

- 新しい検索を開始する前にテキスト ボックスをクリアするための **[クリア]** ボタン。

- 従業員レコードに対する変更を保存するための  **[プロファイルの更新]** ボタン。

- 変更を破棄するための **[変更の取り消し]** ボタン。

## <a name="find-button"></a>[検索] ボタン

VBScript の検索をアクティブに、[**検索**] ボタンをクリックすると\_OnClick の Sub プロシージャは、ビルドし、SQL クエリを送信します。 このボタンをクリックすると、データ グリッドが設定されます。

## <a name="building-the-sql-query"></a>SQL クエリの作成

検索する文字列の最初の部分\_OnClick Sub プロシージャはテキスト文字列をグローバル SQL SELECT ステートメントに追加することによって、一度に 1 つの語句であり、SQL クエリを構築します。 この Sub プロシージャは、データ ソース テーブルからすべてのデータ行を要求する SQL SELECT ステートメントに変数を設定することから始まります。 次に、ページ上の 4 つの入力ボックスをそれぞれスキャンします。

プログラムでは、SQL ステートメントの作成時にワードを使用するため、クエリは完全一致ではなく、サブ文字列検索になります。

たとえば、[ **姓** ] ボックスに "Berge" が入力され、[ **タイトル** ] ボックスに "Program Manager" が入力された場合、SQL ステートメント (値) は次のようになります。

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

クエリが成功すると、"Berge" という文字を含む姓 (Berge や Berger など) と、"Program Manager" という単語を含むタイトル (Program Manager, Advanced Technologies など) が HTML データ グリッドに表示されます。

## <a name="preparing-and-sending-the-query"></a>クエリの準備と送信

検索する文字列の最後の部分\_OnClick Sub プロシージャは、2 つのステートメントで構成されています。 最初のステートメントは、RDS.DataControl オブジェクトの SQL プロパティを、動的に作成される SQL クエリと等しくなるように割り当てます。 2 番目のステートメントでは、 **RDS.DataControl** オブジェクト ( ) でデータベースにクエリを実行した後、クエリの新しい結果をグリッドに表示します。

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a>[プロファイルの更新] ボタン

VBScript の更新プログラムをアクティブに、[**プロファイルの更新**] ボタンをクリックすると\_OnClick Sub プロシージャは、実行 rds.DataControl オブジェクトの () SubmitChanges メソッドと更新メソッド。

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

DC1 です。SubmitChanges を実行、リモート データ サービスは、すべての更新プログラムに関する情報をパッケージ化し、HTTP 経由でサーバーに送信します。 更新プログラムは、まったく。更新プログラムの一部が失敗した場合のすべての更新を行い、ステータス メッセージが返されます。 これを実行すると、リモート データ サービスは、すべての更新プログラムに関する情報をパッケージ化し、HTTP 経由でサーバーに送信します。 更新プログラムは、まったく。更新プログラムの一部が失敗した場合のすべての更新を行い、ステータス メッセージが返されます。 DC1 です。リモート データ サービスでは、 **SubmitChanges**の後更新する必要はありませんが、最新のデータになります。

## <a name="cancel-changes-button"></a>[変更の取り消し] ボタン

VBScript の [キャンセル] をアクティブに**変更をキャンセル**をクリックすると\_OnClick Sub プロシージャは、実行 rds.DataControl オブジェクトの (CancelUpdate メソッドです。

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

実行すると、前回のクエリまたは更新後にユーザーがデータ グリッドの従業員レコードに対して行ったすべての編集が破棄されます。

