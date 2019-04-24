---
title: BrowseTo マクロ アクション
TOCTitle: BrowseTo macro action
ms:assetid: b25e1cc6-c4ed-abd6-0285-94fc7dae0bdf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822020(v=office.15)
ms:contentKeyID: 48547167
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm35083
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0bcf0a37f8c1596856f5d7b921430371d620f7a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296774"
---
# <a name="browseto-macro-action"></a><span data-ttu-id="67858-102">BrowseTo マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="67858-102">BrowseTo macro action</span></span>

<span data-ttu-id="67858-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="67858-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="67858-p101">You can use the **BrowseTo** action to navigate between objects in place. You can also change the source object of a subform control by specifying the Path to Subform Control argument. Use **BrowseTo** to navigate from form1 to form2 without opening up a new window.</span><span class="sxs-lookup"><span data-stu-id="67858-p101">You can use the **BrowseTo** action to navigate between objects in place. You can also change the source object of a subform control by specifying the Path to Subform Control argument. Use **BrowseTo** to navigate from form1 to form2 without opening up a new window.</span></span>

## <a name="setting"></a><span data-ttu-id="67858-107">Setting</span><span class="sxs-lookup"><span data-stu-id="67858-107">Setting</span></span>

<span data-ttu-id="67858-108">"BrowseTo/参照先" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="67858-108">The **BrowseTo** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67858-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="67858-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="67858-110">説明</span><span class="sxs-lookup"><span data-stu-id="67858-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67858-111">Object Type/オブジェクトの種類</span><span class="sxs-lookup"><span data-stu-id="67858-111">Object Type</span></span></p></td>
<td><p><span data-ttu-id="67858-112">参照先のオブジェクトの種類。</span><span class="sxs-lookup"><span data-stu-id="67858-112">The object type to which to browse.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67858-113">オブジェクト名</span><span class="sxs-lookup"><span data-stu-id="67858-113">Object Name</span></span></p></td>
<td><p><span data-ttu-id="67858-114">"Path to Subform Control/サブフォーム コントロールへのパス" 引数で参照するサブフォーム コントロール内に読み込まれるオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="67858-114">The object that loads inside the subform control referenced by the Path to Subform Control argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67858-115">Path to Subform Control/サブフォーム コントロールへのパス</span><span class="sxs-lookup"><span data-stu-id="67858-115">Path to Subform Control</span></span></p></td>
<td><p><span data-ttu-id="67858-116">指定した場合、アプリケーションのメインフォームから、オブジェクト名の引数で指定されたオブジェクトを読み込むターゲットサブフォームコントロールへのパス。</span><span class="sxs-lookup"><span data-stu-id="67858-116">If specified, the path from the main form of the application to the target subform control that loads the object specified by the Object Name argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67858-117">Where Condition/Where 条件式</span><span class="sxs-lookup"><span data-stu-id="67858-117">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="67858-118">指定した場合は、オブジェクト レコード ソースの Where 条件を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="67858-118">If specified, replaces the Where condition of the object record source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67858-119">ページ</span><span class="sxs-lookup"><span data-stu-id="67858-119">Page</span></span></p></td>
<td><p><span data-ttu-id="67858-120">指定した場合は、現在のページになる帳票フォームのページを設定します。</span><span class="sxs-lookup"><span data-stu-id="67858-120">If specified, sets the page of the continuous form that will be made the current page.</span></span> <span data-ttu-id="67858-121">この引数は web のみです。</span><span class="sxs-lookup"><span data-stu-id="67858-121">This argument is web only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67858-122">Data Mode/データ モード</span><span class="sxs-lookup"><span data-stu-id="67858-122">Data Mode</span></span></p></td>
<td><p><span data-ttu-id="67858-123">指定した場合は、フォームのデータ入力モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="67858-123">If specified, the data entry mode of the form.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="67858-124">注釈</span><span class="sxs-lookup"><span data-stu-id="67858-124">Remarks</span></span>

<span data-ttu-id="67858-125">PathToSubFormControl 引数は、次のコード例に示す構文で指定します。</span><span class="sxs-lookup"><span data-stu-id="67858-125">The PathToSubFormControl argument must be specified using the syntax in the following code example:</span></span>

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

<span data-ttu-id="67858-p103">この例では、Main Form が Access クライアント アプリケーションでの最上位フォームになります。"Path to Subform Control/サブフォーム コントロールへのパス" 引数では、メイン フォームから、"Object Name/オブジェクト名" 引数で指定したオブジェクトのコンテナーであるサブフォーム コントロールまで、フォームとサブフォーム コントロールの名前を交互に指定する必要があります。指定する各サブフォーム コントロールは、その前のフォーム上のコントロールである必要があります。このパスは、サブフォーム コントロールで終わる必要があります。</span><span class="sxs-lookup"><span data-stu-id="67858-p103">In this example, the Main Form is the top level form in the Access client application. The Path to Sub Form Control argument must alternately specify form and subform control names leading from the main form to the subform control that is the container of the object specified by the Object Name argument. Each subform control specified must be a control on the form that precedes it. The path must end with a subform control.</span></span>

## <a name="example"></a><span data-ttu-id="67858-130">例</span><span class="sxs-lookup"><span data-stu-id="67858-130">Example</span></span>

<span data-ttu-id="67858-131">次の例は、BrowseTo アクションを使用して、サブフォームコントロールまたはナビゲーションコントロール内のレポートを開く方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="67858-131">The following example shows how to use the BrowseTo action to open a report in a subform control or within a navigation control.</span></span>

<span data-ttu-id="67858-132">**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。</span><span class="sxs-lookup"><span data-stu-id="67858-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OnError
        Go to Next
        Macro Name
    
    /* Try to load the report in the host form (frmAuthorsParameter)    */
    BrowseTo
        Object Type Report
        Object Name rptChapters
        Path to Subform Control frmAuthorsParameter.sfrmChild
        Where Condition
        Page
        Data Mode Edit
    
    Parameters
        SelectedAuthor =[cboAuthor]
    
    /* if this fails, try to load it in the navigation subform     */
    BrowseTo
        Object Type Report
        Object Name rptChapters
        Path to Subform Control frmMain.NavigationSubform>frmAuthorsParameter.sfrmChild
        Where Condition
        Page
        Data Mode Edit
    
    Parameters
        SelectedAuthor =[cboAuthor]
```



