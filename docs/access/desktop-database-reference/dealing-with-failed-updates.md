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
# <a name="dealing-with-failed-updates"></a><span data-ttu-id="2a86b-102">失敗した更新を処理します。</span><span class="sxs-lookup"><span data-stu-id="2a86b-102">Dealing with failed updates</span></span>

<span data-ttu-id="2a86b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2a86b-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="dealing-with-failed-updates"></a><span data-ttu-id="2a86b-104">失敗した更新の処理</span><span class="sxs-lookup"><span data-stu-id="2a86b-104">Dealing with Failed Updates</span></span>

<span data-ttu-id="2a86b-105">更新プログラムで、エラーで終了するときは、エラーを解決する方法の種類と、エラーの重大度レベル、およびアプリケーションのロジックによって異なります。</span><span class="sxs-lookup"><span data-stu-id="2a86b-105">When an update concludes with errors, how you resolve the errors depends on the nature and severity of the errors and the logic of your application.</span></span> <span data-ttu-id="2a86b-106">ただし、データベースの他のユーザーと共有されている場合、一般的なエラーは操作を行う前に、フィールドを変更他のユーザー。</span><span class="sxs-lookup"><span data-stu-id="2a86b-106">However, if the database is shared with other users, a typical error is that someone else modifies the field before you do.</span></span> <span data-ttu-id="2a86b-107">この種のエラーと呼ばれる、*の競合します*。</span><span class="sxs-lookup"><span data-stu-id="2a86b-107">This type of error is called a *conflict.*</span></span> <span data-ttu-id="2a86b-108">ADO はこの状況を検出し、エラーを報告します。</span><span class="sxs-lookup"><span data-stu-id="2a86b-108">ADO detects this situation and reports an error.</span></span>

<span data-ttu-id="2a86b-109">更新エラーが発生すると、そのエラーはエラー処理ルーチンにトラップされます。</span><span class="sxs-lookup"><span data-stu-id="2a86b-109">If there are update errors, they will be trapped in an error-handling routine.</span></span> <span data-ttu-id="2a86b-110">競合する行だけが表示されるよう、 **adFilterConflictingRecords** 定数を使用して **Recordset** をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="2a86b-110">Filter the **Recordset** with the **adFilterConflictingRecords** constant so that only the conflicting rows are visible.</span></span> <span data-ttu-id="2a86b-111">この例では、エラーの解決の戦略は、単なる作成者を印刷するの最初と最後の名前 (**au\_fname**と**au\_lname**)。</span><span class="sxs-lookup"><span data-stu-id="2a86b-111">In this example, the error-resolution strategy is merely to print the author's first and last names (**au\_fname** and **au\_lname**).</span></span>

<span data-ttu-id="2a86b-112">更新時に競合が発生したことをユーザーに警告するコードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="2a86b-112">The code to alert the user to the update conflict looks like this:</span></span>

```vb 
 
objRs.Filter = adFilterConflictingRecords 
objRs.MoveFirst 
Do While Not objRst.EOF 
   Debug.Print "Conflict: Name =  "; objRs!au_fname; " "; objRs!au_lname 
   objRs.MoveNext 
Loop 
```

