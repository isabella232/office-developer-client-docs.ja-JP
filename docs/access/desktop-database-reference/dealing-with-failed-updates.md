---
title: 失敗した更新の処理
TOCTitle: Dealing with failed updates
ms:assetid: f6f4914d-59b3-f3f2-b986-218e07ce5a1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250258(v=office.15)
ms:contentKeyID: 48548752
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9e7d34ad96a44ba654f06f6b94d67a6dd3cf4cef
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585768"
---
# <a name="dealing-with-failed-updates"></a>失敗した更新の処理

**適用先**: Access 2013、Office 2013

## <a name="dealing-with-failed-updates"></a>失敗した更新操作に対処する

更新操作でエラーが発生した場合、エラーの解決方法は、エラーの性質と深刻度、およびアプリケーションのロジックによって異なります。しかし、データベースを他のユーザーと共有している場合に発生する一般的なエラーは、自分がフィールドを変更する前に他のユーザーがそのフィールドを変更したことによるものです。このようなエラーは "競合" と呼ばれます。ADO はこの状況を検知し、エラーを報告します。

更新エラーが発生すると、そのエラーはエラー処理ルーチンにトラップされます。 競合する行だけが表示されるよう、 **adFilterConflictingRecords** 定数を使用して **Recordset** をフィルター処理します。 この例では、エラー解決の戦略は、著者の姓 **(au \_ fname** と **au \_ lname)** を印刷することだけです。

更新時に競合が発生したことをユーザーに警告するコードを次に示します。

```vb 
 
objRs.Filter = adFilterConflictingRecords 
objRs.MoveFirst 
Do While Not objRst.EOF 
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname 
   objRs.MoveNext 
Loop 
```

