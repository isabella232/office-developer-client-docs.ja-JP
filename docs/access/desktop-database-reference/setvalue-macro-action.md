---
title: SetValue マクロ アクション
TOCTitle: SetValue macro action
ms:assetid: a08be0c1-a053-45f9-b4ae-709fedc58e8b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820771(v=office.15)
ms:contentKeyID: 48546712
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 6b6f16c22e9265159c73279cfa1b2644adbc0277
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306819"
---
# <a name="setvalue-macro-action"></a><span data-ttu-id="8bebf-102">SetValue マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="8bebf-102">SetValue macro action</span></span>

<span data-ttu-id="8bebf-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="8bebf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8bebf-104">" **SetValue/値の代入** " アクションを使用すると、フォーム、フォーム データシート、またはレポートの Microsoft Access フィールド、コントロール、あるいはプロパティの値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="8bebf-104">You can use the **SetValue** action to set the value of a Microsoft Access field, control, or property on a form, a form datasheet, or a report.</span></span>

> [!NOTE]
> - <span data-ttu-id="8bebf-105">[!メモ] " **SetValue/値の代入** " アクションを使用して、オブジェクトを返す Access プロパティの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="8bebf-105">You cannot use the **SetValue** action to set the value of an Access property that returns an object.</span></span>
> - <span data-ttu-id="8bebf-106">このアクションは、データベースが信頼されていない場合には許可されません。</span><span class="sxs-lookup"><span data-stu-id="8bebf-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="8bebf-107">Setting</span><span class="sxs-lookup"><span data-stu-id="8bebf-107">Setting</span></span>

<span data-ttu-id="8bebf-108">"**SetValue/値の代入**" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8bebf-108">The **SetValue** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8bebf-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="8bebf-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="8bebf-110">説明</span><span class="sxs-lookup"><span data-stu-id="8bebf-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8bebf-111"><strong>Item</strong></span><span class="sxs-lookup"><span data-stu-id="8bebf-111"><strong>Item</strong></span></span></p></td>
<td><p><span data-ttu-id="8bebf-p101">値を設定するフィールド、コントロール、またはプロパティの名前を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>アイテム</strong>] ボックスに、フィールド、コントロール、またはプロパティの名前を入力します。このアイテムを参照するには、<em>controlname</em> (マクロが呼び出されたフォームまたはレポートのコントロールの場合)、<strong>Forms</strong>!<em>formname</em>!<em>controlname</em> など、完全な構文を使用する必要があります。この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="8bebf-p101">The name of the field, control, or property whose value you want to set. Enter the field, control, or property name in the <strong>Item</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You must use the full syntax to refer to this item, such as <em>controlname</em> (for a control on the form or report from which the macro was called) or <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bebf-116"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="8bebf-116"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="8bebf-117">Access がこのアイテムの値を設定するために使う式。</span><span class="sxs-lookup"><span data-stu-id="8bebf-117">The expression Access uses to set the value for this item.</span></span> <span data-ttu-id="8bebf-118">式の中のオブジェクトを参照するには、常に完全な構文を使う必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bebf-118">You must always use the full syntax to refer to any objects in the expression.</span></span> <span data-ttu-id="8bebf-119">たとえば、Employees フォームの Salary コントロールの値を 10% 増やすには、Forms!Employees!Salary\*1.1 を使用します。</span><span class="sxs-lookup"><span data-stu-id="8bebf-119">For example, to increase the value in a Salary control on an Employees form by 10 percent, use Forms!Employees!Salary\*1.1.</span></span> <span data-ttu-id="8bebf-120">これは必須の引数です。</span><span class="sxs-lookup"><span data-stu-id="8bebf-120">This is a required argument.</span></span></p><p><span data-ttu-id="8bebf-121"><strong>注</strong>: この引数の式の前に等号 (=) を付けてはなりません。</span><span class="sxs-lookup"><span data-stu-id="8bebf-121"><strong>NOTE</strong>: You shouldn't use an equal sign (=) before the expression in this argument.</span></span> <span data-ttu-id="8bebf-122">等号を付けると、Access は式を評価し、その値をこの引数の式として使用します。</span><span class="sxs-lookup"><span data-stu-id="8bebf-122">You shouldn't use an equal sign (=) before the expression in this argument. If you do, Access evaluates the expression and then uses this value as the expression in this argument. This can produce unexpected results if the expression is a string.</span></span> <span data-ttu-id="8bebf-123">その式が文字列の場合、予期しない結果になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8bebf-123">This can produce unexpected results if the expression is a string.</span></span></p>
<p><span data-ttu-id="8bebf-124">たとえば、この引数に「<strong>=&quot;String1&quot;</strong>」と入力すると、Access は最初にこの式を "String1" と評価します。</span><span class="sxs-lookup"><span data-stu-id="8bebf-124">For example, if you type <strong>=&quot;String1&quot;</strong> for this argument, Access first evaluates the expression as String1.</span></span> <span data-ttu-id="8bebf-125">その後、"String1" をこの引数の式として使うので、マクロを呼び出したフォームまたはレポート上の String1 という名前のコントロールまたはプロパティを検索することが予想されます。</span><span class="sxs-lookup"><span data-stu-id="8bebf-125">
For example, if you type ="String1" for this argument, Access first evaluates the expression as String1. Then it uses String1 as the expression in this argument, expecting to find a control or property named String1 on the form or report that called the macro. 
</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="8bebf-126">Access データベース (.mdb または .accdb) では、これらの引数の式を作成するには、[**ビルド**] ボタンをクリックして式ビルダーを使います。</span><span class="sxs-lookup"><span data-stu-id="8bebf-126">In an Access database (.mdb or .accdb), click the **Build** button to use the Expression Builder to create an expression for either of these arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bebf-127">解説</span><span class="sxs-lookup"><span data-stu-id="8bebf-127">Remarks</span></span>

<span data-ttu-id="8bebf-p105">このアクションを使って、フォーム、フォーム データシート、レポート上のフィールドまたはコントロールの値を設定できます。また、ビューのほぼすべてのコントロール、フォーム、レポートのプロパティの値を設定することもできます。マクロを使って特定のプロパティを設定できるかどうか、および設定できるビューについては、Visual Basic エディターでそのプロパティのヘルプ トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bebf-p105">You can use this action to set a value for a field or control on a form, a form datasheet, or a report. You can also set the value for almost all control, form, and report properties in any view. To find out whether a particular property can be set by using a macro and which views it can be set in, see the Help topic for that property in the Visual Basic Editor.</span></span>

<span data-ttu-id="8bebf-131">また、フィールドにバインドされたコントロールがフォームに含まれない場合でも、フォームの基になっているテーブルのフィールドの値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="8bebf-131">You can also set the value for a field in a form's underlying table even if the form doesn't contain a control bound to the field.</span></span> <span data-ttu-id="8bebf-132">そのようなフィールドの値を設定するには、**[アイテム]** ボックスで **Forms**\!*formname*\!*fieldname* という構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="8bebf-132">Use the syntax **Forms**\!*formname*\!*fieldname* in the **Item** box to set the value for such a field.</span></span> <span data-ttu-id="8bebf-133">また、**Reports**\!*reportname*\!*fieldname* という構文を使うことでレポートの基になっているテーブルのフィールドを参照することもできますが、このフィールドにバインドされたコントロールがレポート上に存在するか、またはレポートの演算コントロールでフィールドが参照されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bebf-133">You can also set the value for a field in a form's underlying table even if the form doesn't contain a control bound to the field. Use the syntax Forms!formname!fieldname in the Item box to set the value for such a field. You can also refer to a field in a report's underlying table by using the syntax Reports!reportname!fieldname, but there must be a control on the report bound to this field, or the field must be referred to in a calculated control on the report.</span></span>

<span data-ttu-id="8bebf-p107">フォームのコントロールの値を設定する場合、" **SetValue/値の代入** " アクションでは、コントロールのフォームレベルの入力規則はトリガーされませんが、コントロールが連結コントロールの場合は、基になるフィールドのテーブルレベルの入力規則がトリガーされます。また、" **SetValue/値の代入** " アクションでは再計算もトリガーされます。ただし、この再計算はすぐには実行されません。すぐに再描画をトリガーし、再計算が強制的に行われるようにするには、" **RepaintObject/オブジェクトの再描画** " アクションを使用します。さらに、" **SetValue/値の代入** " アクションでコントロールに設定する値には、コントロールまたは基になるフィールドの **InputMask** プロパティで設定された定型入力は適用されません。</span><span class="sxs-lookup"><span data-stu-id="8bebf-p107">If you set the value of a control on a form, the **SetValue** action doesn't trigger the control's form-level validation rules, but it does trigger the underlying field's table-level validation rules if the control is a bound control. The **SetValue** action also triggers recalculation, but the recalculation may not happen immediately. To trigger immediate repainting and force the recalculation to completion, use the **RepaintObject** action. The value you set in a control by using the **SetValue** action is also not affected by an input mask set in the control's or underlying field's **InputMask** property.</span></span>

<span data-ttu-id="8bebf-p108">コントロールの値を変更するには、コントロールの **AfterUpdate** イベント プロパティによって指定されているマクロで **"SetValue/値の代入"** アクションを使います。ただし、コントロールの **BeforeUpdate** イベント プロパティで指定されているマクロで **"SetValue/値の代入"** アクションを使って、コントロールの値を変更することはできません (ただし、**"SetValue/値の代入"** アクションを使って、他のコントロールの値を変更することはできます)。また、フォームの **BeforeUpdate** または **AfterUpdate** プロパティによって指定されたマクロで **"SetValue/値の代入"** アクションを使って、現在のレコードのコントロールの値を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="8bebf-p108">To change the value of a control, you can use the **SetValue** action in a macro specified by the control's **AfterUpdate** event property. However, you can't use the **SetValue** action in a macro specified by a control's **BeforeUpdate** event property to change the value of the control (although you can use the **SetValue** action to change the value of other controls). You can also use the **SetValue** action in a macro specified by the **BeforeUpdate** or **AfterUpdate** property of a form to change the value of any controls in the current record.</span></span>

> [!NOTE]
> <span data-ttu-id="8bebf-141">"**SetValue/値の導入**" アクションを使用して、次のコントロールの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="8bebf-141">You can't use the **SetValue** action to set the value of the following controls:</span></span>
> - <span data-ttu-id="8bebf-142">レポート上のバインドされたコントロールおよび演算コントロール</span><span class="sxs-lookup"><span data-stu-id="8bebf-142">Bound controls and calculated controls on reports.</span></span>
> - <span data-ttu-id="8bebf-143">フォーム上の演算コントロール</span><span class="sxs-lookup"><span data-stu-id="8bebf-143">Calculated controls on forms.</span></span>

> [!TIP]
> <span data-ttu-id="8bebf-144">**SetValue** アクションを使用して、フォーム ビューのフォームの表示または非表示を設定できます。</span><span class="sxs-lookup"><span data-stu-id="8bebf-144">You can use the **SetValue** action to hide or show a form in Form view.</span></span> <span data-ttu-id="8bebf-145">**[アイテム]** ボックスで **Forms**!*formname\*\*\*.Visible*\* を、**[式]** ボックスで **No** または **Yes** を指定します。</span><span class="sxs-lookup"><span data-stu-id="8bebf-145">Enter **Forms**!*formname*.Visible in the **Item** box and **No** or **Yes** in the **Expression** box.</span></span> <span data-ttu-id="8bebf-146">モーダル フォームの **Visible** プロパティを **No** に設定すると、フォームは非表示およびモードレスになります。</span><span class="sxs-lookup"><span data-stu-id="8bebf-146">Setting a modal form's **Visible** property to **No** hides the form and makes it modeless.</span></span> <span data-ttu-id="8bebf-147">このプロパティを **Yes** に表示すると、フォームは表示され、再度モーダルになります。</span><span class="sxs-lookup"><span data-stu-id="8bebf-147">Setting the property to **Yes** displays the form and makes it modal again.</span></span>

<span data-ttu-id="8bebf-p110">マクロで **"SetValue/値の代入"** アクションを使って、コントロールの値を変更したり、コントロールに新しいデータを追加しても、**BeforeUpdate**、**BeforeInsert**、**Change** などのイベントはトリガーされません。これらのイベントは、ユーザー インターフェイスでこれらのコントロールのデータを変更または入力すると発生します。また、これらのイベントは、Visual Basic for Applications (VBA) モジュールを使ってコントロールの値を設定した場合も発生しません。</span><span class="sxs-lookup"><span data-stu-id="8bebf-p110">Changing the value of or adding new data in a control by using the **SetValue** action in a macro doesn't trigger events such as **BeforeUpdate**, **BeforeInsert**, or **Change** that occur when you change or enter data in these controls in the user interface. These events also don't occur if you set the value of the control by using a Visual Basic for Applications (VBA) module.</span></span>

<span data-ttu-id="8bebf-p111">このアクションは、VBA モジュールでは使用できません。VBA で直接値を設定してください。</span><span class="sxs-lookup"><span data-stu-id="8bebf-p111">This action isn't available in a VBA module. Set the value directly in VBA.</span></span>

## <a name="example"></a><span data-ttu-id="8bebf-152">例</span><span class="sxs-lookup"><span data-stu-id="8bebf-152">Example</span></span>

<span data-ttu-id="8bebf-153">**マクロによるコントロールの値の設定**</span><span class="sxs-lookup"><span data-stu-id="8bebf-153">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="8bebf-p112">次のマクロは、[仕入先] フォーム上のボタンから [商品の追加] フォームを開きます。このマクロは、" **Echo/エコー** "、" **CloseWindow/ウィンドウを閉じる** "、" **OpenForm/フォームを開く** "、" **SetValue/値の代入** "、および " **GoToControl/コントロールの移動** " の各アクションの使い方を示します。" **SetValue/値の代入** " アクションは、[商品] フォームの [仕入先コード] コントロールを [仕入先] フォームの現在の仕入先に設定します。次に、" **GoToControl/コントロールの移動** " アクションがフォーカスを [カテゴリ ID] フィールドに移動します。ユーザーは、ここで、新しい製品のデータの入力を開始できます。このマクロを [仕入先] フォームの [商品の追加] ボタンに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bebf-p112">The following macro opens the Add Products form from a button on the Suppliers form. It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions. The **SetValue** action sets the SupplierID control on the Products form to the current supplier on the Suppliers form. The **GoToControl** action then moves the focus to the CategoryID field, where you can begin to enter data for the new product. This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8bebf-159">アクション</span><span class="sxs-lookup"><span data-stu-id="8bebf-159">Action</span></span></p></th>
<th><p><span data-ttu-id="8bebf-160">引数: 設定値</span><span class="sxs-lookup"><span data-stu-id="8bebf-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="8bebf-161">コメント</span><span class="sxs-lookup"><span data-stu-id="8bebf-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8bebf-162"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="8bebf-162"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="8bebf-163"><strong>Echo On/エコーの設定</strong>: <strong>いいえ</strong></span><span class="sxs-lookup"><span data-stu-id="8bebf-163"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="8bebf-164">マクロの実行中に画面の更新を停止します。</span><span class="sxs-lookup"><span data-stu-id="8bebf-164">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bebf-165"><strong>CloseWindow</strong></span><span class="sxs-lookup"><span data-stu-id="8bebf-165"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="8bebf-166"><strong>オブジェクトの種類</strong>: <strong>フォームオブジェクト名</strong>: 製品リスト<strong>保存</strong>: <strong>いいえ</strong></span><span class="sxs-lookup"><span data-stu-id="8bebf-166"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List  
<strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="8bebf-167">製品/サービス項目の一覧フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8bebf-167">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bebf-168"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="8bebf-168"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="8bebf-169"><strong>フォーム名</strong>: 製品<strong>ビュー</strong>: <strong>フォームデータ モード</strong>: <strong>追加ウィンドウ モード</strong>: <strong>標準</strong></span><span class="sxs-lookup"><span data-stu-id="8bebf-169"><strong>Form Name</strong>: Products  
 
<strong>View</strong>: <strong>Form</strong><strong>Data Mode</strong>: <strong>AddWindow Mode: Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="8bebf-170">[商品] フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="8bebf-170">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bebf-171"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="8bebf-171"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="8bebf-172"><strong>Item/アイテム</strong>: [フォーム]![製品]![SupplierID] <strong>Expression/式</strong>: SupplierID</span><span class="sxs-lookup"><span data-stu-id="8bebf-172"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="8bebf-173">[仕入先コード] コントロールに [仕入先] フォームの現在の仕入先を設定します。</span><span class="sxs-lookup"><span data-stu-id="8bebf-173">Set the SupplierID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bebf-174"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="8bebf-174"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="8bebf-175">"<strong>Control Name/コントロール名</strong>":商品コード</span><span class="sxs-lookup"><span data-stu-id="8bebf-175"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="8bebf-176">[商品コード] コントロールに移動します。</span><span class="sxs-lookup"><span data-stu-id="8bebf-176">Go to the CategoryID control.</span></span></p></td>
</tr>
</tbody>
</table>

