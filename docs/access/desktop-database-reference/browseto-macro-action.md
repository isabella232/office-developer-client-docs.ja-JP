---
title: "'BrowseTo/参照先' マクロ アクション"
TOCTitle: BrowseTo Macro Action
ms:assetid: b25e1cc6-c4ed-abd6-0285-94fc7dae0bdf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822020(v=office.15)
ms:contentKeyID: 48547167
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm35083
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 242041627a909b1c16d956dbbb94a3bf173d544a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878935"
---
# <a name="browseto-macro-action"></a><span data-ttu-id="487c2-102">"BrowseTo/参照先" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="487c2-102">BrowseTo Macro Action</span></span>

<span data-ttu-id="487c2-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="487c2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="487c2-104">**参照**アクションを使用するには保存されているオブジェクト間を移動します。</span><span class="sxs-lookup"><span data-stu-id="487c2-104">You can use the **BrowseTo** action to navigate between objects in place.</span></span> <span data-ttu-id="487c2-105">サブフォーム コントロールの引数へのパスを指定することで、サブフォーム コントロールのソース オブジェクトを変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="487c2-105">You can also change the source object of a subform control by specifying the Path to Subform Control argument.</span></span> <span data-ttu-id="487c2-106">**参照**を使用して、新しいウィンドウを開かずに、form2 を form1 から移動します。</span><span class="sxs-lookup"><span data-stu-id="487c2-106">Use **BrowseTo** to navigate from form1 to form2 without opening up a new window.</span></span>

## <a name="setting"></a><span data-ttu-id="487c2-107">設定</span><span class="sxs-lookup"><span data-stu-id="487c2-107">Setting</span></span>

<span data-ttu-id="487c2-108">**参照**操作では、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="487c2-108">The **BrowseTo** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="487c2-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="487c2-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="487c2-110">説明</span><span class="sxs-lookup"><span data-stu-id="487c2-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="487c2-111">オブジェクトの種類</span><span class="sxs-lookup"><span data-stu-id="487c2-111">Object Type</span></span></p></td>
<td><p><span data-ttu-id="487c2-112">参照先のオブジェクトの種類。</span><span class="sxs-lookup"><span data-stu-id="487c2-112">The object type to which to browse.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="487c2-113">オブジェクト名</span><span class="sxs-lookup"><span data-stu-id="487c2-113">Object Name</span></span></p></td>
<td><p><span data-ttu-id="487c2-114">"Path to Subform Control/サブフォーム コントロールへのパス" 引数で参照するサブフォーム コントロール内に読み込まれるオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="487c2-114">The object that loads inside the subform control referenced by the Path to Subform Control argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="487c2-115">Path to Subform Control/サブフォーム コントロールへのパス</span><span class="sxs-lookup"><span data-stu-id="487c2-115">Path to Subform Control</span></span></p></td>
<td><p><span data-ttu-id="487c2-116">指定されている場合に、ターゲット アプリケーションのメイン フォームからのパスは、[オブジェクト名] 引数で指定されたオブジェクトその荷重を制御します。</span><span class="sxs-lookup"><span data-stu-id="487c2-116">If specified, the path from the main form of the application to the target subform control that loads the object specified by the Object Name argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="487c2-117">Where Condition/Where 条件式</span><span class="sxs-lookup"><span data-stu-id="487c2-117">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="487c2-118">指定した場合は、オブジェクト レコード ソースの Where 条件を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="487c2-118">If specified, replaces the Where condition of the object record source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="487c2-119">Page オブジェクト</span><span class="sxs-lookup"><span data-stu-id="487c2-119">Page</span></span></p></td>
<td><p><span data-ttu-id="487c2-120">指定した場合は、現在のページになる帳票フォームのページを設定します。</span><span class="sxs-lookup"><span data-stu-id="487c2-120">If specified, sets the page of the continuous form that will be made the current page.</span></span> <span data-ttu-id="487c2-121">この引数は、web のみです。</span><span class="sxs-lookup"><span data-stu-id="487c2-121">This argument is web only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="487c2-122">Data Mode/データ モード</span><span class="sxs-lookup"><span data-stu-id="487c2-122">Data Mode</span></span></p></td>
<td><p><span data-ttu-id="487c2-123">指定した場合は、フォームのデータ入力モードを設定します。</span><span class="sxs-lookup"><span data-stu-id="487c2-123">If specified, the data entry mode of the form.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="487c2-124">備考</span><span class="sxs-lookup"><span data-stu-id="487c2-124">Remarks</span></span>

<span data-ttu-id="487c2-125">PathToSubFormControl 引数は、次のコード例に示す構文で指定します。</span><span class="sxs-lookup"><span data-stu-id="487c2-125">The PathToSubFormControl argument must be specified using the syntax in the following code example:</span></span>

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

<span data-ttu-id="487c2-p103">この例では、Main Form が Access クライアント アプリケーションでの最上位フォームになります。"Path to Subform Control/サブフォーム コントロールへのパス" 引数では、メイン フォームから、"Object Name/オブジェクト名" 引数で指定したオブジェクトのコンテナーであるサブフォーム コントロールまで、フォームとサブフォーム コントロールの名前を交互に指定する必要があります。指定する各サブフォーム コントロールは、その前のフォーム上のコントロールである必要があります。このパスは、サブフォーム コントロールで終わる必要があります。</span><span class="sxs-lookup"><span data-stu-id="487c2-p103">In this example, the Main Form is the top level form in the Access client application. The Path to Sub Form Control argument must alternately specify form and subform control names leading from the main form to the subform control that is the container of the object specified by the Object Name argument. Each subform control specified must be a control on the form that precedes it. The path must end with a subform control.</span></span>

## <a name="example"></a><span data-ttu-id="487c2-130">例</span><span class="sxs-lookup"><span data-stu-id="487c2-130">Example</span></span>

<span data-ttu-id="487c2-131">次の例では、参照操作を使用して、サブフォームのコントロールやナビゲーション コントロールは、レポートを開くにする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="487c2-131">The following example shows how to use the BrowseTo action to open a report in a subform control or within a navigation control.</span></span>

<span data-ttu-id="487c2-132">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="487c2-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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



