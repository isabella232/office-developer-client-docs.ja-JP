---
title: RunDataMacro マクロ アクション
TOCTitle: RunDataMacro macro action
ms:assetid: fe4ac2f4-7851-7797-ce91-5f2dd3ba4d22
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837269(v=office.15)
ms:contentKeyID: 48548933
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168493
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 32945f0822682a9432d75ed1ac59117dde3cc0e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306812"
---
# <a name="rundatamacro-macro-action"></a><span data-ttu-id="30881-102">RunDataMacro マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="30881-102">RunDataMacro macro action</span></span>

<span data-ttu-id="30881-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="30881-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="30881-104">"RunDataMacro/データマクロの実行" アクションを使用して、名前付きデータ マクロを実行できます。</span><span class="sxs-lookup"><span data-stu-id="30881-104">You can use the **RunDataMacro** action to run a named data macro.</span></span>

## <a name="setting"></a><span data-ttu-id="30881-105">Setting</span><span class="sxs-lookup"><span data-stu-id="30881-105">Setting</span></span>

<span data-ttu-id="30881-106">"RunDataMacro/データマクロの実行" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="30881-106">The **RunDataMacro** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30881-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="30881-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="30881-108">説明</span><span class="sxs-lookup"><span data-stu-id="30881-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30881-109">名前</span><span class="sxs-lookup"><span data-stu-id="30881-109">Name</span></span></p></td>
<td><p><span data-ttu-id="30881-110">実行するデータ マクロの名前</span><span class="sxs-lookup"><span data-stu-id="30881-110">The name of the data macro to run.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="30881-111">注釈</span><span class="sxs-lookup"><span data-stu-id="30881-111">Remarks</span></span>

<span data-ttu-id="30881-112">**RunDataMacro**アクションは、マクロ、マクロの名前付きデータマクロ、およびマクロイベントの終了後**[](after-delete-macro-event.md)**、マクロイベントの**[挿入](after-insert-macro-event.md)** 後、および更新後**[マクロイベント](after-update-macro-event.md)** の後に使用できます。</span><span class="sxs-lookup"><span data-stu-id="30881-112">You can use the **RunDataMacro** action in macros, named data macros, and the following macro events: **[After Delete macro event](after-delete-macro-event.md)**, **[After Insert macro event](after-insert-macro-event.md)** and **[After Update macro event](after-update-macro-event.md)**.</span></span>

<span data-ttu-id="30881-113">データマクロの名前には、追加先のテーブルを含める必要があります (たとえば、addcomment だけではなく\*\*\*\*、**コメント**など)。</span><span class="sxs-lookup"><span data-stu-id="30881-113">The name of the data macro must include the table to which it is attached (for example, **Comments.AddComment**, not just **AddComment**).</span></span>

<span data-ttu-id="30881-p101">マクロ デザイナーで実行するデータ マクロを選択すると、そのデータ マクロにパラメーターが必要であるかどうかが自動的に判断されます。パラメーターが必要な場合は、引数を入力するテキストボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="30881-p101">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters. If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>

<span data-ttu-id="30881-p102">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.</span><span class="sxs-lookup"><span data-stu-id="30881-p102">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span>

## <a name="example"></a><span data-ttu-id="30881-118">例</span><span class="sxs-lookup"><span data-stu-id="30881-118">Example</span></span>

<span data-ttu-id="30881-119">次の例は、名前付きデータマクロにパラメーターを渡す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="30881-119">The following example shows how to pass a parameter to a named data macro.</span></span> <span data-ttu-id="30881-120">tblServiceRequests テーブルの dmGetCurrentServiceRequest data マクロは、RunDataMacro アクションを使用して呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="30881-120">The dmGetCurrentServiceRequest data macro of the tblServiceRequests table is called by using the RunDataMacro action.</span></span> <span data-ttu-id="30881-121">dmGetCurrentServiceRequest が完了すると、CurrentServiceRequest 変数が返された形式で、データマクロが txtcurrentsr テキストボックスに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="30881-121">When the dmGetCurrentServiceRequest is finished, the CurrentServiceRequest variable returned form the data macro is written to the txtCurrentSR text box.</span></span>

<span data-ttu-id="30881-122">**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。</span><span class="sxs-lookup"><span data-stu-id="30881-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    RunDataMacro
        Macro Name tblServiceRequests.dmGetCurrentServiceRequest
    
    Parameters
        prmAssignedTo =[ID]
    
    SetProperty
        Control Name txtCurrentSR
        Property Value
        Value =[ReturnVars]![CurrentServiceRequest]
```
