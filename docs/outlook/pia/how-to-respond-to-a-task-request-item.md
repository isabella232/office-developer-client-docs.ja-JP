---
title: タスク依頼アイテムに返信する
TOCTitle: Respond to a task request item
ms:assetid: 573c98ef-4d15-4fd1-bccd-25a22c9a63f0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184608(v=office.15)
ms:contentKeyID: 55119896
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9aa6416680bbf2443506415b5fa871d30fe5f32e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357394"
---
# <a name="respond-to-a-task-request-item"></a><span data-ttu-id="2964b-102">タスク依頼アイテムに返信する</span><span class="sxs-lookup"><span data-stu-id="2964b-102">Respond to a task request item</span></span>

<span data-ttu-id="2964b-103">以下の例では、タスク依頼アイテムの取得および返信を行う方法を示します。</span><span class="sxs-lookup"><span data-stu-id="2964b-103">This example shows how to get and respond to a task request item.</span></span>

## <a name="example"></a><span data-ttu-id="2964b-104">例</span><span class="sxs-lookup"><span data-stu-id="2964b-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="2964b-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="2964b-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="2964b-106">次のコード サンプルでは、AcceptTaskRequest は [TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\)) オブジェクトの [GetAssociatedTask(Boolean)](https://msdn.microsoft.com/library/bb645779\(v=office.15\)) メソッドを使用して [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)) オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="2964b-106">In the following code example, AcceptTaskRequest uses the [GetAssociatedTask(Boolean)](https://msdn.microsoft.com/library/bb645779\(v=office.15\)) method of the [TaskRequestItem](https://msdn.microsoft.com/library/bb610737\(v=office.15\)) object to get the [TaskItem](https://msdn.microsoft.com/library/bb624227\(v=office.15\)) object.</span></span> <span data-ttu-id="2964b-107">次に、パラメーターを [olTaskAccept](https://msdn.microsoft.com/library/bb624484\(v=office.15\)) に設定した [Respond(OlTaskResponse, Object, Object)](https://msdn.microsoft.com/library/bb644188\(v=office.15\)) メソッドを呼び出して、タスクの依頼を承諾します。</span><span class="sxs-lookup"><span data-stu-id="2964b-107">The example then calls the [Respond(OlTaskResponse, Object, Object)](https://msdn.microsoft.com/library/bb644188\(v=office.15\)) method with the parameter set to [olTaskAccept](https://msdn.microsoft.com/library/bb624484\(v=office.15\)) to accept the task request.</span></span>

<span data-ttu-id="2964b-108">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2964b-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="2964b-109">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2964b-109">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="2964b-110">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="2964b-110">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void AcceptTaskRequest()
{
    string filter = "[MessageClass] = 'IPM.TaskRequest'";
    Outlook.Items items =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderInbox).
        Items.Restrict(filter);
    if (items.Count > 0)
    {
        Outlook.TaskRequestItem taskRequest =
            (Outlook.TaskRequestItem)items[1];
        Outlook.TaskItem task =
            taskRequest.GetAssociatedTask(false);
        Outlook.TaskItem taskResponse = task.Respond(
            Outlook.OlTaskResponse.olTaskAccept, true, false);
        taskResponse.Send();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="2964b-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="2964b-111">See also</span></span>

- [<span data-ttu-id="2964b-112">タスク</span><span class="sxs-lookup"><span data-stu-id="2964b-112">Tasks</span></span>](tasks.md)

