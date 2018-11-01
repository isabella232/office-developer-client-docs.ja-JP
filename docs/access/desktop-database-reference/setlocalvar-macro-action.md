---
title: "\"SetLocalVar/ローカル変数の設定\" マクロ アクション"
TOCTitle: SetLocalVar Macro Action
ms:assetid: 8a6af395-0f76-72e2-37f3-2cff22a38b3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197097(v=office.15)
ms:contentKeyID: 48546190
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm176660
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 299227553481c4f149827c31078111db7b427f7f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886642"
---
# <a name="setlocalvar-macro-action"></a><span data-ttu-id="5ed5b-102">"SetLocalVar/ローカル変数の設定" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="5ed5b-102">SetLocalVar Macro Action</span></span>


<span data-ttu-id="5ed5b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5ed5b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5ed5b-104">" **SetLocalVar/ローカル変数の設定** " アクションは、一時変数を作成し、それを特定の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="5ed5b-104">The **SetLocalVar** action creates a temporary variable and set it to a specific value.</span></span>

## <a name="setting"></a><span data-ttu-id="5ed5b-105">設定</span><span class="sxs-lookup"><span data-stu-id="5ed5b-105">Setting</span></span>

<span data-ttu-id="5ed5b-106">" **SetLocalVar/ローカル変数の設定** " アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5ed5b-106">The **SetLocalVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ed5b-107">引数</span><span class="sxs-lookup"><span data-stu-id="5ed5b-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="5ed5b-108">必須</span><span class="sxs-lookup"><span data-stu-id="5ed5b-108">Required</span></span></p></th>
<th><p><span data-ttu-id="5ed5b-109">説明</span><span class="sxs-lookup"><span data-stu-id="5ed5b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ed5b-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="5ed5b-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed5b-111">はい</span><span class="sxs-lookup"><span data-stu-id="5ed5b-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="5ed5b-112">変数の名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="5ed5b-112">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ed5b-113"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="5ed5b-113"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="5ed5b-114">はい</span><span class="sxs-lookup"><span data-stu-id="5ed5b-114">Yes</span></span></p></td>
<td><p><span data-ttu-id="5ed5b-115">この一時変数の値を設定に使用する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="5ed5b-115">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="5ed5b-116">式の前に等号 (=) を付けないでください。</span><span class="sxs-lookup"><span data-stu-id="5ed5b-116">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="5ed5b-117">この引数を設定するのには、<strong>式ビルダー</strong>を使用するのには [<strong>ビルド</strong>] ボタンをクリックすることができます。</span><span class="sxs-lookup"><span data-stu-id="5ed5b-117">You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5ed5b-118">備考</span><span class="sxs-lookup"><span data-stu-id="5ed5b-118">Remarks</span></span>

<span data-ttu-id="5ed5b-119">**予約**によって作成された変数は、定義されているマクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="5ed5b-119">Variables created by the **SetLocalVar** action can be used only in the macro in which they are defined.</span></span> <span data-ttu-id="5ed5b-120">**[SetTempVar](settempvar-macro-action.md)** アクションを使用して、別のマクロ、イベント プロシージャ、またはフォームまたはレポートで使用できる変数を定義します。</span><span class="sxs-lookup"><span data-stu-id="5ed5b-120">Use the **[SetTempVar](settempvar-macro-action.md)** action to define a variable that can be used in another macro, in an event procedure, or on a form or report.</span></span>

<span data-ttu-id="5ed5b-p103">一時変数を作成すると、それを式で参照できます。たとえば、TotalAmount という一時変数を作成した場合、次の構文でこの変数をテキスト ボックスのコントロール ソースとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="5ed5b-p103">Once a temporary variable has been created, you can refer to it in an expression. For example, if you created a temporary variable named TotalAmount, you could use the variable as the control source for a text box by using the following syntax.</span></span>

`=[LocalVars]![TotalAmount]`


> [!NOTE]
> <P><span data-ttu-id="5ed5b-p104">[!メモ] データ マクロでは、変数を参照するために LocalVals コレクションを使用する必要はありません。たとえば、データ マクロで TotalAmount という一時変数を作成した場合、次の構文でこの変数をテキスト ボックスのコントロールとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="5ed5b-p104">In a Data Macro, you do not have to use the LocalVars collection to refer to a variable. For example, if you created a temporary variable in a Data Macro named TotalAmount, you could use the variable as the control source for a text box by using the following syntax</span></span><BR><span data-ttu-id="5ed5b-125">= [TotalAmount]</span><span class="sxs-lookup"><span data-stu-id="5ed5b-125">=[TotalAmount]</span></span></P>


