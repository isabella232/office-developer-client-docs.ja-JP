---
title: 失敗した更新を処理します。
TOCTitle: Dealing with failed updates
ms:assetid: f6f4914d-59b3-f3f2-b986-218e07ce5a1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250258(v=office.15)
ms:contentKeyID: 48548752
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 659b5389074371ed4de41b909ab5228ad8fca080
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947750"
---
# <a name="dealing-with-failed-updates"></a>失敗した更新を処理します。

**適用されます**Access 2013、Office 2013。

## <a name="dealing-with-failed-updates"></a>失敗した更新の処理

更新プログラムで、エラーで終了するときは、エラーを解決する方法の種類と、エラーの重大度レベル、およびアプリケーションのロジックによって異なります。 ただし、データベースの他のユーザーと共有されている場合、一般的なエラーは操作を行う前に、フィールドを変更他のユーザー。 この種のエラーと呼ばれる、*の競合します*。 ADO はこの状況を検出し、エラーを報告します。

更新エラーが発生すると、そのエラーはエラー処理ルーチンにトラップされます。 競合する行だけが表示されるよう、 **adFilterConflictingRecords** 定数を使用して **Recordset** をフィルター処理します。 この例では、エラーの解決の戦略は、単なる作成者を印刷するの最初と最後の名前 (**au\_fname**と**au\_lname**)。

更新時に競合が発生したことをユーザーに警告するコードを次に示します。

```vb 
 
objRs.Filter = adFilterConflictingRecords 
objRs.MoveFirst 
Do While Not objRst.EOF 
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname 
   objRs.MoveNext 
Loop 
```

