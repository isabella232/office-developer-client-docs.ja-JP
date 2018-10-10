---
title: "'RunDataMacro/データマクロの実行' マクロ アクション"
TOCTitle: RunDataMacro Macro Action
ms:assetid: fe4ac2f4-7851-7797-ce91-5f2dd3ba4d22
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837269(v=office.15)
ms:contentKeyID: 48548933
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168493
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9790faf03ba0f6ea02520abb525c4301ac2181e2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476679"
---
# <a name="rundatamacro-macro-action"></a><span data-ttu-id="b2433-102">"RunDataMacro/データマクロの実行" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="b2433-102">RunDataMacro Macro Action</span></span>

<span data-ttu-id="b2433-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2433-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b2433-104">**RunDataMacro**アクションを使用すると、名前付きデータ マクロを実行します。</span><span class="sxs-lookup"><span data-stu-id="b2433-104">You can use the **RunDataMacro** action to run a named data macro.</span></span>

## <a name="setting"></a><span data-ttu-id="b2433-105">設定</span><span class="sxs-lookup"><span data-stu-id="b2433-105">Setting</span></span>

<span data-ttu-id="b2433-106">" **RunDataMacro/データマクロの実行** " アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b2433-106">The **RunDataMacro** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b2433-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="b2433-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b2433-108">説明</span><span class="sxs-lookup"><span data-stu-id="b2433-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2433-109">名前</span><span class="sxs-lookup"><span data-stu-id="b2433-109">Name</span></span></p></td>
<td><p><span data-ttu-id="b2433-110">実行するデータ マクロの名前</span><span class="sxs-lookup"><span data-stu-id="b2433-110">The name of the data macro to run.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b2433-111">備考</span><span class="sxs-lookup"><span data-stu-id="b2433-111">Remarks</span></span>

<span data-ttu-id="b2433-112">**RunDataMacro**アクションを使用すると、マクロ、名前付きデータ マクロでは、およびマクロの次のイベントの中で:**[マクロ イベントの削除後](after-delete-macro-event.md)**、**[マクロ イベントの挿入後](after-insert-macro-event.md)**、**[更新後のマクロ イベント](after-update-macro-event.md)** です。</span><span class="sxs-lookup"><span data-stu-id="b2433-112">You can use the **RunDataMacro** action in macros, named data macros, and the following macro events: **[After Delete Macro Event](after-delete-macro-event.md)**, **[After Insert Macro Event](after-insert-macro-event.md)** and **[After Update Macro Event](after-update-macro-event.md)**.</span></span>

<span data-ttu-id="b2433-113">データ マクロの名前は、それが関連付けられている (たとえば、 **Comments.AddComment**、 **AddComment**だけではなく) テーブルを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2433-113">The name of the data macro must include the table to which it is attached (for example, **Comments.AddComment**, not just **AddComment**).</span></span>

<span data-ttu-id="b2433-p101">マクロ デザイナーで実行するデータ マクロを選択すると、そのデータ マクロにパラメーターが必要であるかどうかが自動的に判断されます。パラメーターが必要な場合は、引数を入力するテキストボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b2433-p101">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters. If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>

<span data-ttu-id="b2433-116">**RunDataMacro**アクションを含むマクロを実行するし、 **RunDataMacro**アクションに到達して、data という名前のマクロが実行されます。</span><span class="sxs-lookup"><span data-stu-id="b2433-116">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro.</span></span> <span data-ttu-id="b2433-117">Data という名前のマクロが完了したら、アクセスが元に戻りし、次のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="b2433-117">When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span>

## <a name="example"></a><span data-ttu-id="b2433-118">例</span><span class="sxs-lookup"><span data-stu-id="b2433-118">Example</span></span>

<span data-ttu-id="b2433-119">次の例では、名前付きデータ マクロにパラメーターを渡す方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b2433-119">The following example shows how to pass a parameter to a named data macro.</span></span> <span data-ttu-id="b2433-120">RunDataMacro アクションを使用して、tblServiceRequests テーブルの dmGetCurrentServiceRequest のデータ マクロが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b2433-120">The dmGetCurrentServiceRequest data macro of the tblServiceRequests table is called by using the RunDataMacro action.</span></span> <span data-ttu-id="b2433-121">DmGetCurrentServiceRequest が完了したら、CurrentServiceRequest 変数には、フォームのデータ マクロは、txtCurrentSR テキスト ボックスに書き込まれますが返されます。</span><span class="sxs-lookup"><span data-stu-id="b2433-121">When the dmGetCurrentServiceRequest is finished, the CurrentServiceRequest variable returned form the data macro is written to the txtCurrentSR text box.</span></span>

<span data-ttu-id="b2433-122">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="b2433-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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