---
title: SetOrderBy マクロ アクション
TOCTitle: SetOrderBy macro action
ms:assetid: 78f65ce9-b56f-f476-3bd6-f3307bc22a08
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196152(v=office.15)
ms:contentKeyID: 48545765
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98639
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 86834cd8b6132e8939067c0e34037ca1b0ef8bad
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704421"
---
# <a name="setorderby-macro-action"></a><span data-ttu-id="77825-102">SetOrderBy マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="77825-102">SetOrderBy macro action</span></span>


<span data-ttu-id="77825-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="77825-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="77825-104">**SetOrderBy** アクションを使用し、フォーム、レポート、テーブル、またはクエリ結果のレコードを並べ替えることができます。</span><span class="sxs-lookup"><span data-stu-id="77825-104">You can use the **SetOrderBy** action to specify how you want to sort records in a form, report, table, or query result.</span></span>

## <a name="setting"></a><span data-ttu-id="77825-105">設定</span><span class="sxs-lookup"><span data-stu-id="77825-105">Setting</span></span>

<span data-ttu-id="77825-106">**SetOrderBy** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="77825-106">The **SetOrderBy** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77825-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="77825-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="77825-108">説明</span><span class="sxs-lookup"><span data-stu-id="77825-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77825-109"><strong>Order By/並び替え</strong></span><span class="sxs-lookup"><span data-stu-id="77825-109"><strong>Order By</strong></span></span></p></td>
<td><p><span data-ttu-id="77825-110">レコードを並べ替えるフィールド (複数可) の名前を含む文字列の式です。必要に応じて ASC キーワードまたは DESC キーワードを含めることもできます</span><span class="sxs-lookup"><span data-stu-id="77825-110">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77825-111"><strong>Control Name/コントロール名</strong></span><span class="sxs-lookup"><span data-stu-id="77825-111"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="77825-p101">アクティブ オブジェクトがフォームまたはレポートである場合、並べ替えるサブフォームまたはサブレポートに対応するコントロール名を示します。この引数を指定しないと、アクティブ オブジェクトがフォームまたはレポートである場合は、親フォームまたは親レポートが並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="77825-p101">If provided and the active object is a form or report, the name of the control that corresponds to the subform or subreport that will be sorted. If empty and the active object is a form or report, the parent form or report is sorted..</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="77825-114">解説</span><span class="sxs-lookup"><span data-stu-id="77825-114">Remarks</span></span>

<span data-ttu-id="77825-115">このマクロ アクションを実行すると、アクティブであり、かつフォーカスがあるテーブル、フォーム、レポート、またはデータシート (クエリ結果) に対して並べ替えが適用されます。</span><span class="sxs-lookup"><span data-stu-id="77825-115">When you run this macro action, the sort is applied to the table, form, report or datasheet (query result) that is active and has the focus.</span></span>

<span data-ttu-id="77825-p102">"Order By/並べ替え" 引数とは、レコードを並べ替えるフィールドの名前を指します。複数のフィールド名を指定する場合はコンマ (,) で区切ります。アクティブ オブジェクトの **OrderBy** プロパティを使用すると、順序値を保存し、後で適用できます。OrderBy プロパティの値は、そのプロパティを設定したオブジェクトに保存されます。オブジェクトを開くと自動的に開きますが、自動的には適用されません。</span><span class="sxs-lookup"><span data-stu-id="77825-p102">The Order By argument is the name of the field or fields on which you want to sort records. When you use more than one field name, separate the names with a comma (,). The **OrderBy** property of the active object is used to save the ordering value and apply it at a later time. OrderBy values are saved with the objects in which they are created. They are automatically loaded when the object is opened, but they aren't automatically applied.</span></span>

<span data-ttu-id="77825-121">1 つ以上のフィールド名を入力し、"Order By/並べ替え" 引数を設定してマクロを実行すると、レコードは既定では昇順に並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="77825-121">When you set the Order By argument by entering one or more field names and then run the macro, the records are sorted by default in ascending order.</span></span>

<span data-ttu-id="77825-p103">レコードを降順に並べ替えるには、"Order By/並べ替え" 引数式の最後に「DESC」と入力します。たとえば、連絡先の降順に顧客レコードを並べ替えるには、"Order By/並べ替え" 引数を "ContactName DESC" に設定します。名前を姓の降順および名の昇順に並べ替えるには、"Order By/並べ替え" 引数を "LastName DESC, FirstName ASC" に設定します。</span><span class="sxs-lookup"><span data-stu-id="77825-p103">To sort records in descending order, type DESC at the end of the Order By argument expression. For example, to sort customer records in descending order by contact name, set the Order By argument to "ContactName DESC". To sort names by LastName descending, and FirstName ascending, set the Order By argument to "LastName DESC, FirstName ASC".</span></span>

