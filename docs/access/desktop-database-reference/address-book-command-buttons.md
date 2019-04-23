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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282479"
---
# <a name="address-book-command-buttons"></a>アドレス帳のコマンド ボタン


**適用先:** Access 2013、Office 2013


アドレス帳アプリケーションには次のコマンド ボタンがあります。

- クエリをデータベースに送信するための **[検索]** ボタン。

- 新しい検索を開始する前にテキスト ボックスをクリアするための **[クリア]** ボタン。

- 従業員レコードに対する変更を保存するための  **[プロファイルの更新]** ボタン。

- 変更を破棄するための **[変更の取り消し]** ボタン。

## <a name="find-button"></a>[検索] ボタン

[**検索**] ボタンをクリックすると\_、VBScript 検索の OnClick Sub プロシージャがアクティブになり、SQL クエリが作成されて送信されます。 このボタンをクリックすると、データ グリッドが設定されます。

## <a name="building-the-sql-query"></a>SQL クエリの作成

OnClick Sub の検索\_プロシージャの最初の部分では、sql クエリを作成します。これは、1つの文字列をグローバル sql SELECT ステートメントに追加することによって行います。 この Sub プロシージャは、データ ソース テーブルからすべてのデータ行を要求する SQL SELECT ステートメントに変数を設定することから始まります。 次に、ページ上の 4 つの入力ボックスをそれぞれスキャンします。

プログラムでは、SQL ステートメントの作成時にワードを使用するため、クエリは完全一致ではなく、サブ文字列検索になります。

たとえば、[ **姓** ] ボックスに "Berge" が入力され、[ **タイトル** ] ボックスに "Program Manager" が入力された場合、SQL ステートメント (値) は次のようになります。

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

クエリが成功すると、"Berge" という文字を含む姓  (Berge や Berger など) と、"Program Manager" という単語を含むタイトル (Program Manager, Advanced Technologies など) が HTML データ グリッドに表示されます。

## <a name="preparing-and-sending-the-query"></a>クエリの準備と送信

OnClick Sub の検索\_プロシージャの最後の部分は、2つのステートメントで構成されます。 最初のステートメントは、RDS.DataControl オブジェクトの SQL プロパティを、動的に作成される SQL クエリと等しくなるように割り当てます。 2 番目のステートメントでは、**RDS.DataControl** オブジェクト ( ) でデータベースにクエリを実行した後、クエリの新しい結果をグリッドに表示します。

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a>[プロファイルの更新] ボタン

[**プロファイルの更新**] ボタンをクリックする\_と、VBScript update OnClick Sub プロシージャがアクティブになります。これにより、RDS が実行されます。DataControl オブジェクトの () SubmitChanges メソッドおよび Refresh メソッド

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

DC1。SubmitChanges が実行されると、リモートデータサービスはすべての更新情報をパッケージ化し、HTTP を介してサーバーに送信します。 update は all または nothing です。更新の一部が失敗した場合、変更は一切行われず、ステータスメッセージが返されます。 が実行されると、リモートデータサービスはすべての更新情報をパッケージ化し、HTTP を介してサーバーに送信します。 update は all または nothing です。更新の一部が失敗した場合、変更は一切行われず、ステータスメッセージが返されます。 DC1.リモートデータサービスを使用して**SubmitChanges**を実行した後に更新する必要はありませんが、最新のデータが保証されます。

## <a name="cancel-changes-button"></a>[変更の取り消し] ボタン

**[変更のキャンセル]** をクリック\_すると、VBScript のキャンセル OnClick Sub プロシージャがアクティブになります。これにより、RDS が実行されます。DataControl オブジェクト (CancelUpdate メソッド)。

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

実行すると、前回のクエリまたは更新後にユーザーがデータ グリッドの従業員レコードに対して行ったすべての編集が破棄されます。

