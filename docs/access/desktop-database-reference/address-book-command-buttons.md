---
title: アドレス帳のコマンド ボタン
TOCTitle: Address Book command buttons
ms:assetid: bcea6f53-3e36-b067-03c2-b157ed02d41d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249908(v=office.15)
ms:contentKeyID: 48547422
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f981ef687f916a6d82cddf974ed1b6dac26c4252
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603082"
---
# <a name="address-book-command-buttons"></a>アドレス帳のコマンド ボタン


**適用先**: Access 2013、Office 2013


アドレス帳アプリケーションには次のコマンド ボタンがあります。

- クエリをデータベースに送信するための **[検索]** ボタン。

- 新しい検索を開始する前にテキスト ボックスをクリアするための **[クリア]** ボタン。

- 従業員レコードに対する変更を保存するための  **[プロファイルの更新]** ボタン。

- 変更を破棄するための **[変更の取り消し]** ボタン。

## <a name="find-button"></a>[検索] ボタン

[検索] ボタン **を** クリックすると、VBScript Find OnClick Sub プロシージャがアクティブ化され、クエリの作成と送信SQL \_ されます。 このボタンをクリックすると、データ グリッドが設定されます。

## <a name="building-the-sql-query"></a>SQL クエリの作成

Find OnClick Sub プロシージャの最初の部分では、グローバルクエリ SELECT ステートメントにテキスト文字列を追加することで、SQL クエリ (一度に 1 つの語句) \_ をSQLします。 この Sub プロシージャは、データ ソース テーブルからすべてのデータ行を要求する SQL SELECT ステートメントに変数を設定することから始まります。 次に、ページ上の 4 つの入力ボックスをそれぞれスキャンします。

プログラムでは、SQL ステートメントの作成時にワードを使用するため、クエリは完全一致ではなく、サブ文字列検索になります。

たとえば、[ **姓** ] ボックスに "Berge" が入力され、[ **タイトル** ] ボックスに "Program Manager" が入力された場合、SQL ステートメント (値) は次のようになります。

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

クエリが成功すると、"Berge" という文字を含む姓  (Berge や Berger など) と、"Program Manager" という単語を含むタイトル (Program Manager, Advanced Technologies など) が HTML データ グリッドに表示されます。

## <a name="preparing-and-sending-the-query"></a>クエリの準備と送信

Find OnClick Sub プロシージャの最後の \_ 部分は、2 つのステートメントで構成されます。 最初のステートメントは、RDS.DataControl オブジェクトの SQL プロパティを、動的に作成される SQL クエリと等しくなるように割り当てます。 2 番目のステートメントでは、**RDS.DataControl** オブジェクト ( ) でデータベースにクエリを実行した後、クエリの新しい結果をグリッドに表示します。

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a>[プロファイルの更新] ボタン

[プロファイルの更新 **] ボタンを** クリックすると、RDS を実行する VBScript Update \_ OnClick Sub プロシージャがアクティブ化されます。DataControl オブジェクトの () SubmitChanges メソッドと Refresh メソッド。

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

DC1 の場合。SubmitChanges が実行され、リモート データ サービスは、すべての更新情報をパッケージし、HTTP 経由でサーバーに送信します。 この更新プログラムは、すべてまたは何も行いません。更新プログラムの一部が失敗した場合、変更は行われません。状態メッセージが返されます。 を実行すると、リモート データ サービスは、すべての更新情報をパッケージし、HTTP 経由でサーバーに送信します。 この更新プログラムは、すべてまたは何も行いません。更新プログラムの一部が失敗した場合、変更は行われません。状態メッセージが返されます。 DC1。リモート データ サービスを使用して **SubmitChanges** を実行した後は更新は必要ありませんが、新しいデータが保証されます。

## <a name="cancel-changes-button"></a>[変更の取り消し] ボタン

[変更の **取り消し]** をクリックすると、RDS を実行する VBScript Cancel \_ OnClick Sub プロシージャがアクティブ化されます。DataControl オブジェクトの ( CancelUpdate メソッド。

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

実行すると、前回のクエリまたは更新後にユーザーがデータ グリッドの従業員レコードに対して行ったすべての編集が破棄されます。

