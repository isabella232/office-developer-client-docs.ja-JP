---
title: SetReturnVar マクロ アクション
TOCTitle: SetReturnVar Macro Action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fa4380904888194bf1d954ebf5619cab7d155047
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477375"
---
# <a name="setreturnvar-macro-action"></a><span data-ttu-id="68c68-102">SetReturnVar マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="68c68-102">SetReturnVar Macro Action</span></span>

<span data-ttu-id="68c68-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="68c68-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="68c68-104">" **SetReturnVar/戻り変数の設定** " アクションは、戻り変数を作成し、それを特定の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="68c68-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span>

> [!NOTE]
> <span data-ttu-id="68c68-105">[!メモ] " **SetReturnVar/戻り変数の設定** " アクションは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="68c68-105">The **SetReturnVar** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="68c68-106">設定</span><span class="sxs-lookup"><span data-stu-id="68c68-106">Setting</span></span>

<span data-ttu-id="68c68-107">" **SetReturnVar/戻り変数の設定** " アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="68c68-107">The **SetReturnVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="68c68-108">引数</span><span class="sxs-lookup"><span data-stu-id="68c68-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="68c68-109">必須</span><span class="sxs-lookup"><span data-stu-id="68c68-109">Required</span></span></p></th>
<th><p><span data-ttu-id="68c68-110">説明</span><span class="sxs-lookup"><span data-stu-id="68c68-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="68c68-111">名前</span><span class="sxs-lookup"><span data-stu-id="68c68-111">Name</span></span></p></td>
<td><p><span data-ttu-id="68c68-112">はい</span><span class="sxs-lookup"><span data-stu-id="68c68-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="68c68-113">変数の名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="68c68-113">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68c68-114">演算</span><span class="sxs-lookup"><span data-stu-id="68c68-114">Expression</span></span></p></td>
<td><p><span data-ttu-id="68c68-115">はい</span><span class="sxs-lookup"><span data-stu-id="68c68-115">Yes</span></span></p></td>
<td><p><span data-ttu-id="68c68-116">この一時変数の値を設定に使用する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="68c68-116">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="68c68-117">式の前に等号 (=) を付けないでください。</span><span class="sxs-lookup"><span data-stu-id="68c68-117">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="68c68-118">この引数を設定するのには、<strong>式ビルダー</strong>を使用するのには [<strong>ビルド</strong>] ボタンをクリックすることができます。</span><span class="sxs-lookup"><span data-stu-id="68c68-118">You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="68c68-119">備考</span><span class="sxs-lookup"><span data-stu-id="68c68-119">Remarks</span></span>

<span data-ttu-id="68c68-120">" **SetReturnVar/戻り変数の設定** " アクションを使用して、 **ReturnVar** を作成します。この変数は、" **RunDataMacro/データマクロの実行** " アクションを使用してデータ マクロを呼び出すマクロが使用できます。</span><span class="sxs-lookup"><span data-stu-id="68c68-120">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span>

<span data-ttu-id="68c68-p102">" **SetReturnVar/戻り変数の設定** " アクションによって **ReturnVar** が作成されたら、呼び出し元のマクロは式でその変数を使用できます。たとえば、 **UpdateSuccess** という名前の **ReturnVar** を作成した場合は、次の構文を使用して変数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="68c68-p102">Once a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression. For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>

```vb
    =[ReturnVars]![UpdateSuccess]
```

<span data-ttu-id="68c68-p103">" **SetReturnVar/戻り変数の設定** " アクションは、指定されたデータ マクロでのみ使用できます。データ マクロ イベントに接続されたデータ マクロでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="68c68-p103">The **SetReturnVar** action can be used only in named data macros. It is not available in data macros that are attached to a data macro event.</span></span>

## <a name="example"></a><span data-ttu-id="68c68-125">例</span><span class="sxs-lookup"><span data-stu-id="68c68-125">Example</span></span>

<span data-ttu-id="68c68-p104">次の例は、 SetReturnVar アクションを使用して名前付きデータ マクロから値を返す方法を示します。" CurrentServiceRequest" という名前の **ReturnVar** が、名前付きデータ マクロの呼び出し元であるマクロまたは Visual Basic for Applications (VBA) サブルーチンに返されます。</span><span class="sxs-lookup"><span data-stu-id="68c68-p104">The following example shows how to use the SetReturnVar action to return a value from a named data macro. A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="68c68-128">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="68c68-128">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
