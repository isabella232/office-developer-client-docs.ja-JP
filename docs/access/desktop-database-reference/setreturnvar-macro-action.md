---
title: SetReturnVar マクロ アクション
TOCTitle: SetReturnVar macro action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e0c849fc507d535807bc088e667acd74410ddd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308674"
---
# <a name="setreturnvar-macro-action"></a><span data-ttu-id="2e805-102">SetReturnVar マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="2e805-102">SetReturnVar macro action</span></span>

<span data-ttu-id="2e805-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="2e805-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2e805-104">" **SetReturnVar/戻り変数の設定** " アクションは、戻り変数を作成し、それを特定の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="2e805-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span>

> [!NOTE]
> <span data-ttu-id="2e805-105">"**SetReturnVar**/戻り変数の設定" アクションは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="2e805-105">The **SetReturnVar** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="2e805-106">Setting</span><span class="sxs-lookup"><span data-stu-id="2e805-106">Setting</span></span>

<span data-ttu-id="2e805-107">"**SetReturnVar/戻り変数の設定**" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2e805-107">The **SetReturnVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2e805-108">引数</span><span class="sxs-lookup"><span data-stu-id="2e805-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="2e805-109">必須</span><span class="sxs-lookup"><span data-stu-id="2e805-109">Required</span></span></p></th>
<th><p><span data-ttu-id="2e805-110">説明</span><span class="sxs-lookup"><span data-stu-id="2e805-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e805-111">名前</span><span class="sxs-lookup"><span data-stu-id="2e805-111">Name</span></span></p></td>
<td><p><span data-ttu-id="2e805-112">はい</span><span class="sxs-lookup"><span data-stu-id="2e805-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="2e805-113">変数の名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="2e805-113">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e805-114">演算</span><span class="sxs-lookup"><span data-stu-id="2e805-114">Expression</span></span></p></td>
<td><p><span data-ttu-id="2e805-115">はい</span><span class="sxs-lookup"><span data-stu-id="2e805-115">Yes</span></span></p></td>
<td><p><span data-ttu-id="2e805-p101">An expression that will be used to set the value for this temporary variable. Do not precede the expression with the equal sign (=). You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.  </span><span class="sxs-lookup"><span data-stu-id="2e805-p101">An expression that will be used to set the value for this temporary variable. Do not precede the expression with the equal sign (=). You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2e805-119">注釈</span><span class="sxs-lookup"><span data-stu-id="2e805-119">Remarks</span></span>

<span data-ttu-id="2e805-120">"**SetReturnVar**/戻り変数の設定" アクションを使用して、変数の **ReturnVar** を作成できます。この変数を、"**RunDataMacro**/データマクロの実行" アクションを使用してデータ マクロを呼び出すマクロで使用できます。</span><span class="sxs-lookup"><span data-stu-id="2e805-120">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span>

<span data-ttu-id="2e805-p102">" **SetReturnVar/戻り変数の設定** " アクションによって **ReturnVar** が作成されたら、呼び出し元のマクロは式でその変数を使用できます。たとえば、 **UpdateSuccess** という名前の **ReturnVar** を作成した場合は、次の構文を使用して変数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="2e805-p102">Once a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression. For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>

```vb
    =[ReturnVars]![UpdateSuccess]
```

<span data-ttu-id="2e805-p103">" **SetReturnVar/戻り変数の設定** " アクションは、指定されたデータ マクロでのみ使用できます。データ マクロ イベントに接続されたデータ マクロでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="2e805-p103">The **SetReturnVar** action can be used only in named data macros. It is not available in data macros that are attached to a data macro event.</span></span>

## <a name="example"></a><span data-ttu-id="2e805-125">例</span><span class="sxs-lookup"><span data-stu-id="2e805-125">Example</span></span>

<span data-ttu-id="2e805-126">次の例は、 SetReturnVar アクションを使用して名前付きデータ マクロから値を返す方法を示します。</span><span class="sxs-lookup"><span data-stu-id="2e805-126">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="2e805-127">" CurrentServiceRequest" という名前の **ReturnVar** が、名前付きデータ マクロの呼び出し元であるマクロまたは Visual Basic for Applications (VBA) サブルーチンに返されます。</span><span class="sxs-lookup"><span data-stu-id="2e805-127">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="2e805-128">**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。</span><span class="sxs-lookup"><span data-stu-id="2e805-128">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
