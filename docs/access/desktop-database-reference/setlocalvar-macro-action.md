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
ms.openlocfilehash: fb2b3aabb4736c0deee57dafb36e32730fb95f4f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479705"
---
# <a name="setlocalvar-macro-action"></a><span data-ttu-id="f1ec0-102">"SetLocalVar/ローカル変数の設定" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="f1ec0-102">SetLocalVar Macro Action</span></span>


<span data-ttu-id="f1ec0-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="f1ec0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f1ec0-104">" **SetLocalVar/ローカル変数の設定** " アクションは、一時変数を作成し、それを特定の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="f1ec0-104">The **SetLocalVar** action creates a temporary variable and set it to a specific value.</span></span>

## <a name="setting"></a><span data-ttu-id="f1ec0-105">設定</span><span class="sxs-lookup"><span data-stu-id="f1ec0-105">Setting</span></span>

<span data-ttu-id="f1ec0-106">" **SetLocalVar/ローカル変数の設定** " アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f1ec0-106">The **SetLocalVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f1ec0-107">引数</span><span class="sxs-lookup"><span data-stu-id="f1ec0-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="f1ec0-108">必須</span><span class="sxs-lookup"><span data-stu-id="f1ec0-108">Required</span></span></p></th>
<th><p><span data-ttu-id="f1ec0-109">説明</span><span class="sxs-lookup"><span data-stu-id="f1ec0-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1ec0-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="f1ec0-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="f1ec0-111">はい</span><span class="sxs-lookup"><span data-stu-id="f1ec0-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="f1ec0-112">変数の名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="f1ec0-112">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1ec0-113"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="f1ec0-113"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="f1ec0-114">はい</span><span class="sxs-lookup"><span data-stu-id="f1ec0-114">Yes</span></span></p></td>
<td><p><span data-ttu-id="f1ec0-115">この一時変数の値を設定に使用する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="f1ec0-115">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="f1ec0-116">式の前に等号 (=) を付けないでください。</span><span class="sxs-lookup"><span data-stu-id="f1ec0-116">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="f1ec0-117">この引数を設定するのには、<strong>式ビルダー</strong>を使用するのには [<strong>ビルド</strong>] ボタンをクリックすることができます。</span><span class="sxs-lookup"><span data-stu-id="f1ec0-117">You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f1ec0-118">備考</span><span class="sxs-lookup"><span data-stu-id="f1ec0-118">Remarks</span></span>

<span data-ttu-id="f1ec0-119">**予約**によって作成された変数は、定義されているマクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="f1ec0-119">Variables created by the **SetLocalVar** action can be used only in the macro in which they are defined.</span></span> <span data-ttu-id="f1ec0-120">**[SetTempVar](settempvar-macro-action.md)** アクションを使用して、別のマクロ、イベント プロシージャ、またはフォームまたはレポートで使用できる変数を定義します。</span><span class="sxs-lookup"><span data-stu-id="f1ec0-120">Use the **[SetTempVar](settempvar-macro-action.md)** action to define a variable that can be used in another macro, in an event procedure, or on a form or report.</span></span>

<span data-ttu-id="f1ec0-p103">一時変数を作成すると、それを式で参照できます。たとえば、TotalAmount という一時変数を作成した場合、次の構文でこの変数をテキスト ボックスのコントロール ソースとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="f1ec0-p103">Once a temporary variable has been created, you can refer to it in an expression. For example, if you created a temporary variable named TotalAmount, you could use the variable as the control source for a text box by using the following syntax.</span></span>

`=[LocalVars]![TotalAmount]`


> [!NOTE]
> <P><span data-ttu-id="f1ec0-p104">[!メモ] データ マクロでは、変数を参照するために LocalVals コレクションを使用する必要はありません。たとえば、データ マクロで TotalAmount という一時変数を作成した場合、次の構文でこの変数をテキスト ボックスのコントロールとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="f1ec0-p104">In a Data Macro, you do not have to use the LocalVars collection to refer to a variable. For example, if you created a temporary variable in a Data Macro named TotalAmount, you could use the variable as the control source for a text box by using the following syntax</span></span><BR><span data-ttu-id="f1ec0-125">= [TotalAmount]</span><span class="sxs-lookup"><span data-stu-id="f1ec0-125">=[TotalAmount]</span></span></P>


