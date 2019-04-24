---
title: Delete メソッドによるレコードの削除
TOCTitle: Deleting records using the Delete method
ms:assetid: 22917c33-4d14-ebab-d85c-2cbe7f68c560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249003(v=office.15)
ms:contentKeyID: 48543708
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a476e9bc57224b0e46afb31bf092450c26de0a17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293967"
---
# <a name="deleting-records-using-the-delete-method"></a>Delete メソッドによるレコードの削除


**適用先:** Access 2013、Office 2013

**Delete** メソッドを使用すると、 **Recordset** オブジェクト内の現在のレコード、またはレコードのグループが削除されるよう設定されます。 **Recordset** オブジェクトでレコードの削除が認められていない場合は、エラーが発生します。イミディエイト更新モードを使用している場合、削除操作はデータベース内で直ちに実行されます。データベースの整合性違反などによってレコードの削除が正常に実行できない場合、レコードは **Update** が呼び出された後も編集モードのまま変化しません。このため、 [Close](cancelupdate-method-ado.md)、[Move](close-method-ado.md)、[NextRecordset](move-method-ado.md) などを使用して現在のレコードから移動する前に、 [CancelUpdate](nextrecordset-method-ado.md) を使用して更新を取り消す必要があります。

バッチ更新モードを使用している場合、レコードはキャッシュから削除されるよう設定され、実際の削除は **UpdateBatch** メソッドを呼び出したときに実行されます (削除されたレコードを表示するには、 **Delete** を呼び出した後に **Filter** プロパティを **adFilterAffectedRecords** に設定します)。

削除されたレコードからフィールド値を取得しようとすると、エラーが生成されます。現在のレコードが削除された後も、他のレコードに移動するまで、削除されたレコードが現在のレコードとなります。削除されたレコードから移動すると、それ以降そのレコードにはアクセスできなくなります。

削除操作をトランザクション内に入れ子にしている場合は、 **RollbackTrans** メソッドを使用して削除されたレコードを元に戻すことができます。バッチ更新モードを使用している場合は、 **CancelBatch** メソッドを使用して、1 つまたは複数の保留中の削除操作を取り消すことができます。

基になるデータとの競合 (レコードが他のユーザーによって既に削除されている場合など) によって、レコードの削除操作が失敗した場合、プロバイダーは **Errors** コレクションに警告を返しますが、プログラムの実行は停止されません。実行時エラーが発生するのは、すべての要求されたレコードに競合がある場合のみです。

動的プロパティである **Unique Table** が設定されており、 **Recordset** が複数のテーブルに対して JOIN 操作を実行した結果である場合、 **Delete** メソッドを使用すると、 **Unique Table** プロパティで指定されたテーブルの行のみが削除されます。

**Delete** メソッドは、 **Delete** 操作の対象となるレコードを指定できるオプションの引数を受け取ります。この引数に指定できる値は、次の ADO **AffectEnum** 列挙定数のうちどちらかのみです。

  - **現在の範囲内の adて**いる現在のレコードにのみ影響します。

  - adています。**グループ**現在の**Filter**プロパティの設定を満たすレコードのみに影響します。 このオプションを使用するには、 **Filter** プロパティが、 **FilterGroupEnum** 値、または **Bookmarks** の配列に設定されている必要があります。

次のコードでは、 **Delete** メソッドを呼び出すときに **adAffectGroup** を指定する例を示します。この例では、いくつかのレコードをサンプルの **Recordset** に追加し、データベースを更新します。次に、フィルター列挙定数である **adFilterAffectedRecords** 使用して **Recordset** をフィルター処理し、新しく追加されたレコードのみ **Recordset** 内に表示されるようにします。最後に、 **Delete** メソッドを呼び出し、現在の **Filter** プロパティの設定を満たすすべてのレコード (新しいレコード) を削除するよう指定します。

```vb 
 
'BeginDeleteGroup 
 'add some bogus records 
 With objRs1 
 For i = 0 To 8 
 .AddNew 
 .Fields("CompanyName") = "Shipper Number " & i + 1 
 .Fields("Phone") = "(425) 555-000" & (i + 1) 
 .Update 
 Next i 
 
 're-connect & update 
 .ActiveConnection = GetNewConnection 
 .UpdateBatch 
 
 'filter on newly added records 
 .Filter = adFilterAffectedRecords 
 Debug.Print "Deleting the " & .RecordCount & _ 
 " records you just added." 
 
 'delete the newly added bogus records 
 .Delete adAffectGroup 
 .Filter = adFilterNone 
 Debug.Print .RecordCount & " records remain." 
 
 .Close 
 End With 
'EndDeleteGroup 
```

