---
title: SetFilter マクロ アクション
TOCTitle: SetFilter macro action
ms:assetid: dee699e2-0840-1612-23ce-199ef8d30566
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835438(v=office.15)
ms:contentKeyID: 48548203
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm122943
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ac1a2c8a603fb74b56d71f73605455ecdbc87035
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308695"
---
# <a name="setfilter-macro-action"></a><span data-ttu-id="8bb30-102">SetFilter マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="8bb30-102">SetFilter macro action</span></span>

<span data-ttu-id="8bb30-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="8bb30-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8bb30-104">"SetFilter/フィルターの実行" アクションを使用すると、アクティブ データシート、アクティブ フォーム、アクティブ レポート、またはアクティブ テーブルのレコードに対してフィルターを適用できます。</span><span class="sxs-lookup"><span data-stu-id="8bb30-104">You can use the **SetFilter** action to apply a filter to the records in the active datasheet, form, report, or table.</span></span>

## <a name="setting"></a><span data-ttu-id="8bb30-105">Setting</span><span class="sxs-lookup"><span data-stu-id="8bb30-105">Setting</span></span>

<span data-ttu-id="8bb30-106">"SetFilter/フィルターの実行" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8bb30-106">The **SetFilter** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8bb30-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="8bb30-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="8bb30-108">説明</span><span class="sxs-lookup"><span data-stu-id="8bb30-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8bb30-109">Filter Name/フィルター名</span><span class="sxs-lookup"><span data-stu-id="8bb30-109">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="8bb30-110">指定した場合は、クエリの名前、またはクエリとして保存されているフィルターの名前。</span><span class="sxs-lookup"><span data-stu-id="8bb30-110">If provided, the name of a query or of a filter saved as a query.</span></span> <span data-ttu-id="8bb30-111">クライアントデータベースでは、この引数または WhereCondition 引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="8bb30-111">This argument or the WhereCondition argument is required in a client database.</span></span> <span data-ttu-id="8bb30-112">web データベースでは、この引数は使用できません。</span><span class="sxs-lookup"><span data-stu-id="8bb30-112">In a web database, this argument is not available.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bb30-113">Where Condition/Where 条件式</span><span class="sxs-lookup"><span data-stu-id="8bb30-113">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="8bb30-114">指定した場合は、データシート、フォーム、レポート、またはテーブルのレコードを制限する SQL WHERE 句。</span><span class="sxs-lookup"><span data-stu-id="8bb30-114">If provided, a SQL WHERE clause that restricts the records in the datasheet, form, report, or table.</span></span> <span data-ttu-id="8bb30-115">web データベースでは、この引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="8bb30-115">In a web database, this argument is required.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bb30-116">コントロール名</span><span class="sxs-lookup"><span data-stu-id="8bb30-116">Control Name</span></span></p></td>
<td><p><span data-ttu-id="8bb30-p103">指定した場合は、フィルター処理するサブフォームまたはサブレポートに対応するコントロールの名前を示します。指定しない場合は、現在のオブジェクトがフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="8bb30-p103">If provided, the name of the control that corresponds to the subform or subreport to be filtered. If empty, the current object is filtered.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8bb30-119">注釈</span><span class="sxs-lookup"><span data-stu-id="8bb30-119">Remarks</span></span>

<span data-ttu-id="8bb30-120">Web データベースでは、Where Condition 引数の先頭に (=) を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="8bb30-120">In a web database, the Where Condition argument cannot begin with an equal sign (=).</span></span>

<span data-ttu-id="8bb30-121">このアクションを実行すると、アクティブであり、かつフォーカスがあるテーブル、フォーム、レポート、またはデータシート (クエリ結果など) に対してフィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="8bb30-121">When you run this action, the filter is applied to the table, form, report or datasheet (for example, query result) that is active and has the focus.</span></span>

<span data-ttu-id="8bb30-p104">アクティブなオブジェクトの **Filter** プロパティを使用すると、"WhereCondition/Where 条件式" 引数を保存して、後で適用できます。フィルターは、それを作成したオブジェクトに保存されます。そのオブジェクトが開くと自動的に読み込まれますが、自動的に適用されることはありません。</span><span class="sxs-lookup"><span data-stu-id="8bb30-p104">The **Filter** property of the active object is used to save the WhereCondition argument and apply it at a later time. Filters are saved with the objects in which they are created. They are automatically loaded when the object is opened, but they are not automatically applied.</span></span>

<span data-ttu-id="8bb30-125">クライアントデータベースで、オブジェクトを開いたときにフィルターを自動的に適用するには、 **FilterOnLoad**プロパティを True に設定します。</span><span class="sxs-lookup"><span data-stu-id="8bb30-125">In a client database, to automatically apply a filter when the object is opened, set the **FilterOnLoad** property to True.</span></span>

<span data-ttu-id="8bb30-126">Web データベースで、オブジェクトを開いたときにフィルターを自動的に適用するには、マクロに "SetFilter/フィルターの実行" アクションを追加し、このマクロをオブジェクトの OnLoad イベントに追加します。</span><span class="sxs-lookup"><span data-stu-id="8bb30-126">In a web database, to automatically apply a filter when the object is opened, add the **SetFilter** action to a macro, and add the macro to the object's **OnLoad** event.</span></span>

## <a name="example"></a><span data-ttu-id="8bb30-127">例</span><span class="sxs-lookup"><span data-stu-id="8bb30-127">Example</span></span>

<span data-ttu-id="8bb30-128">次の例では、SetFilter アクションを使用して、マクロが定義されているフォームにフィルターを適用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="8bb30-128">The following example shows how to use the SetFilter action to filter the form in which the macro is defined.</span></span>

<span data-ttu-id="8bb30-129">**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。</span><span class="sxs-lookup"><span data-stu-id="8bb30-129">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    SetFilter
        Filter Name
        Where Condtion =[display_name] Like "*cheese*"
        Control Name
```
