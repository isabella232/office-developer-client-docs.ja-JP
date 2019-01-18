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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722691"
---
# <a name="setvalue-macro-action"></a><span data-ttu-id="fc560-102">SetValue マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="fc560-102">SetValue macro action</span></span>

<span data-ttu-id="fc560-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="fc560-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fc560-104">" **SetValue/値の代入** " アクションを使用すると、フォーム、フォーム データシート、またはレポートの Microsoft Access フィールド、コントロール、あるいはプロパティの値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="fc560-104">You can use the **SetValue** action to set the value of a Microsoft Access field, control, or property on a form, a form datasheet, or a report.</span></span>

> [!NOTE]
> - <span data-ttu-id="fc560-105">[!メモ] " **SetValue/値の代入** " アクションを使用して、オブジェクトを返す Access プロパティの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="fc560-105">You cannot use the **SetValue** action to set the value of an Access property that returns an object.</span></span>
> - <span data-ttu-id="fc560-106">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。</span><span class="sxs-lookup"><span data-stu-id="fc560-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="fc560-107">設定</span><span class="sxs-lookup"><span data-stu-id="fc560-107">Setting</span></span>

<span data-ttu-id="fc560-108">" **SetValue/値の代入** " アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fc560-108">The **SetValue** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc560-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="fc560-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="fc560-110">説明</span><span class="sxs-lookup"><span data-stu-id="fc560-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc560-111"><strong>アイテム</strong></span><span class="sxs-lookup"><span data-stu-id="fc560-111"><strong>Item</strong></span></span></p></td>
<td><p><span data-ttu-id="fc560-p101">値を設定するフィールド、コントロール、またはプロパティの名前を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>アイテム</strong>] ボックスに、フィールド、コントロール、またはプロパティの名前を入力します。このアイテムを参照するには、<em>controlname</em> (マクロが呼び出されたフォームまたはレポートのコントロールの場合)、<strong>Forms</strong>!<em>formname</em>!<em>controlname</em> など、完全な構文を使用する必要があります。この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="fc560-p101">The name of the field, control, or property whose value you want to set. Enter the field, control, or property name in the <strong>Item</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You must use the full syntax to refer to this item, such as <em>controlname</em> (for a control on the form or report from which the macro was called) or <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc560-116"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="fc560-116"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="fc560-p102">このアイテムの値を設定するときに Access が使用する式を指定します。式のオブジェクトを参照するには、完全な構文を使用する必要があります。たとえば、Employees フォームの Salary コントロールの値を 10% 増やすには、Forms!Employees!Salary\*1.1. を使用します。この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="fc560-p102">The expression Access uses to set the value for this item. You must always use the full syntax to refer to any objects in the expression. For example, to increase the value in a Salary control on an Employees form by 10 percent, use Forms!Employees!Salary\*1.1. This is a required argument.</span></span></p><p><span data-ttu-id="fc560-121"><strong>注</strong>: この引数の式の前に等号 (=) を使用するべきではありません。</span><span class="sxs-lookup"><span data-stu-id="fc560-121"><strong>NOTE</strong>: You shouldn't use an equal sign (=) before the expression in this argument.</span></span> <span data-ttu-id="fc560-122">場合は、アクセスが式を評価し、この引数の式としてこの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="fc560-122">If you do, Access evaluates the expression and then uses this value as the expression in this argument.</span></span> <span data-ttu-id="fc560-123">式が文字列の場合、予期しない結果が生じる。</span><span class="sxs-lookup"><span data-stu-id="fc560-123">This can produce unexpected results if the expression is a string.</span></span></p>
<p><span data-ttu-id="fc560-124">入力する場合など<strong>=&quot;文字列 1&quot; </strong> 、この引数を最初に評価され文字列 1 として表現します。</span><span class="sxs-lookup"><span data-stu-id="fc560-124">For example, if you type <strong>=&quot;String1&quot;</strong> for this argument, Access first evaluates the expression as String1.</span></span> <span data-ttu-id="fc560-125">[String1 コントロールまたはフォームやレポート、マクロと呼ばれることで、文字列 1 をという名前のプロパティを検索するため、この引数の式として使用します。</span><span class="sxs-lookup"><span data-stu-id="fc560-125">Then it uses String1 as the expression in this argument, expecting to find a control or property named String1 on the form or report that called the macro.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="fc560-126">[!メモ] Access データベース (.mdb または .accdb) では、[ **ビルド**] をクリックし、式ビルダーを使用して、この引数のどちらかに対して式を作成します。</span><span class="sxs-lookup"><span data-stu-id="fc560-126">In an Access database (.mdb or .accdb), click the **Build** button to use the Expression Builder to create an expression for either of these arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc560-127">注釈</span><span class="sxs-lookup"><span data-stu-id="fc560-127">Remarks</span></span>

<span data-ttu-id="fc560-p105">このアクションを使用すると、フォーム、フォーム データシート、またはレポートのフィールドあるいはコントロールに対して値を設定できます。また、任意のビューのほぼすべてのコントロール、フォーム、およびレポートのプロパティに値を設定することもできます。マクロを使用して特定のプロパティを設定できるかどうか、およびどのビューでプロパティを設定できるかを確認するには、Visual Basic エディターのそのプロパティに関するヘルプ トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc560-p105">You can use this action to set a value for a field or control on a form, a form datasheet, or a report. You can also set the value for almost all control, form, and report properties in any view. To find out whether a particular property can be set by using a macro and which views it can be set in, see the Help topic for that property in the Visual Basic Editor.</span></span>

<span data-ttu-id="fc560-131">フィールドに連結されたコントロールがフォームに含まれていない場合でも、フォームの基になるテーブル フィールドの値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="fc560-131">You can also set the value for a field in a form's underlying table even if the form doesn't contain a control bound to the field.</span></span> <span data-ttu-id="fc560-132">**フォーム**の構文を使用して、\!*フォーム*\!このようなフィールドの値を設定する**項目**] ボックスで*フィールド名*です。</span><span class="sxs-lookup"><span data-stu-id="fc560-132">Use the syntax **Forms**\!*formname*\!*fieldname* in the **Item** box to set the value for such a field.</span></span> <span data-ttu-id="fc560-133">**レポート**の構文を使用して、レポートの基になるテーブル内のフィールドを参照することもできます\!*レポート名*\!*フィールド名*をこのフィールドにバインドされているレポート上のコントロールが存在する必要がありますかで、フィールドを参照する必要がありますが、レポートの演算コントロールです。</span><span class="sxs-lookup"><span data-stu-id="fc560-133">You can also refer to a field in a report's underlying table by using the syntax **Reports**\!*reportname*\!*fieldname*, but there must be a control on the report bound to this field, or the field must be referred to in a calculated control on the report.</span></span>

<span data-ttu-id="fc560-p107">フォームのコントロールの値を設定する場合、" **SetValue/値の代入** " アクションでは、コントロールのフォームレベルの入力規則はトリガーされませんが、コントロールが連結コントロールの場合は、基になるフィールドのテーブルレベルの入力規則がトリガーされます。また、" **SetValue/値の代入** " アクションでは再計算もトリガーされます。ただし、この再計算はすぐには実行されません。すぐに再描画をトリガーし、再計算が強制的に行われるようにするには、" **RepaintObject/オブジェクトの再描画** " アクションを使用します。さらに、" **SetValue/値の代入** " アクションでコントロールに設定する値には、コントロールまたは基になるフィールドの **InputMask** プロパティで設定された定型入力は適用されません。</span><span class="sxs-lookup"><span data-stu-id="fc560-p107">If you set the value of a control on a form, the **SetValue** action doesn't trigger the control's form-level validation rules, but it does trigger the underlying field's table-level validation rules if the control is a bound control. The **SetValue** action also triggers recalculation, but the recalculation may not happen immediately. To trigger immediate repainting and force the recalculation to completion, use the **RepaintObject** action. The value you set in a control by using the **SetValue** action is also not affected by an input mask set in the control's or underlying field's **InputMask** property.</span></span>

<span data-ttu-id="fc560-p108">コントロールの **AfterUpdate** イベント プロパティによって指定されたマクロで " **SetValue/値の代入** " アクションを使用すると、そのコントロールの値を変更できます。ただし、コントロールの **BeforeUpdate** イベント プロパティで指定されたマクロで " **SetValue/値の代入** " アクションでは、そのコントロールの値を変更することはできません (ただし、" **SetValue/値の代入** " アクションを使用して、他のコントロールの値を変更することはできます)。また、フォームの **BeforeUpdate** または **AfterUpdate** プロパティで指定されたマクロで " **SetValue/値の代入** " アクションを使用して、カレント レコードのコントロールの値を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="fc560-p108">To change the value of a control, you can use the **SetValue** action in a macro specified by the control's **AfterUpdate** event property. However, you can't use the **SetValue** action in a macro specified by a control's **BeforeUpdate** event property to change the value of the control (although you can use the **SetValue** action to change the value of other controls). You can also use the **SetValue** action in a macro specified by the **BeforeUpdate** or **AfterUpdate** property of a form to change the value of any controls in the current record.</span></span>

> [!NOTE]
> <span data-ttu-id="fc560-141">"**SetValue/値の導入**" アクションを使用して、次のコントロールの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="fc560-141">You can't use the **SetValue** action to set the value of the following controls:</span></span>
> - <span data-ttu-id="fc560-142">レポートの連結コントロールおよび演算コントロール。</span><span class="sxs-lookup"><span data-stu-id="fc560-142">Bound controls and calculated controls on reports.</span></span>
> - <span data-ttu-id="fc560-143">フォームの演算コントロール。</span><span class="sxs-lookup"><span data-stu-id="fc560-143">Calculated controls on forms.</span></span>

> [!TIP]
> <span data-ttu-id="fc560-144">[!ヒント] " **SetValue/値の代入** " アクションを使用すると、フォーム ビューのフォームを表示または非表示にできます。</span><span class="sxs-lookup"><span data-stu-id="fc560-144">You can use the **SetValue** action to hide or show a form in Form view.</span></span> <span data-ttu-id="fc560-145">**フォーム**を入力してください。*formname。。表示されている*\* で、**項目**のボックスと**いいえ]** または **[はい]** [**式**] ボックスにします。</span><span class="sxs-lookup"><span data-stu-id="fc560-145">Enter **Forms**!*formname\*\*\*.Visible*\* in the **Item** box, and **No** or **Yes** in the **Expression** box.</span></span> <span data-ttu-id="fc560-146">モーダル フォームの **Visible** プロパティを **No** に設定すると、フォームは非表示およびモードレスになります。</span><span class="sxs-lookup"><span data-stu-id="fc560-146">Setting a modal form's **Visible** property to **No** hides the form and makes it modeless.</span></span> <span data-ttu-id="fc560-147">このプロパティを **Yes** に表示すると、フォームは表示され、再度モーダルになります。</span><span class="sxs-lookup"><span data-stu-id="fc560-147">Setting the property to **Yes** displays the form and makes it modal again.</span></span>

<span data-ttu-id="fc560-p110">マクロで " **SetValue/値の代入** " アクションを使用してコントロールの値を変更するか新しいデータを追加した場合、ユーザー インターフェイスのこれらのコントロールのデータを変更または入力するときに発生するイベント ( **BeforeUpdate** 、 **BeforeInsert** 、 **Change** など) はトリガーされません。これらのイベントは、Visual Basic for Applications (VBA) モジュールを使用してコントロールの値を設定しても発生しません。</span><span class="sxs-lookup"><span data-stu-id="fc560-p110">Changing the value of or adding new data in a control by using the **SetValue** action in a macro doesn't trigger events such as **BeforeUpdate**, **BeforeInsert**, or **Change** that occur when you change or enter data in these controls in the user interface. These events also don't occur if you set the value of the control by using a Visual Basic for Applications (VBA) module.</span></span>

<span data-ttu-id="fc560-p111">このアクションは VBA モジュールでは使用できません。値は Visual Basic で直接設定します。</span><span class="sxs-lookup"><span data-stu-id="fc560-p111">This action isn't available in a VBA module. Set the value directly in VBA.</span></span>

## <a name="example"></a><span data-ttu-id="fc560-152">例</span><span class="sxs-lookup"><span data-stu-id="fc560-152">Example</span></span>

<span data-ttu-id="fc560-153">**マクロによるコントロールの値の設定**</span><span class="sxs-lookup"><span data-stu-id="fc560-153">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="fc560-p112">次のマクロは、[仕入先] フォーム上のボタンから [商品の追加] フォームを開きます。このマクロは、" **Echo/エコー** "、" **CloseWindow/ウィンドウを閉じる** "、" **OpenForm/フォームを開く** "、" **SetValue/値の代入** "、および " **GoToControl/コントロールの移動** " の各アクションの使い方を示します。" **SetValue/値の代入** " アクションは、[商品] フォームの [仕入先コード] コントロールを [仕入先] フォームの現在の仕入先に設定します。次に、" **GoToControl/コントロールの移動** " アクションがフォーカスを [カテゴリ ID] フィールドに移動します。ユーザーは、ここで、新しい製品のデータの入力を開始できます。このマクロを [仕入先] フォームの [商品の追加] ボタンに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc560-p112">The following macro opens the Add Products form from a button on the Suppliers form. It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions. The **SetValue** action sets the SupplierID control on the Products form to the current supplier on the Suppliers form. The **GoToControl** action then moves the focus to the CategoryID field, where you can begin to enter data for the new product. This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc560-159">アクション</span><span class="sxs-lookup"><span data-stu-id="fc560-159">Action</span></span></p></th>
<th><p><span data-ttu-id="fc560-160">引数: 設定値</span><span class="sxs-lookup"><span data-stu-id="fc560-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="fc560-161">コメント</span><span class="sxs-lookup"><span data-stu-id="fc560-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc560-162"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="fc560-162"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="fc560-163"><strong>Echo On/エコーの設定</strong>: <strong>No/いいえ</strong></span><span class="sxs-lookup"><span data-stu-id="fc560-163"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="fc560-164">画面の更新は停止しますが、マクロは実行されています。</span><span class="sxs-lookup"><span data-stu-id="fc560-164">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc560-165"><strong>CloseWindow</strong></span><span class="sxs-lookup"><span data-stu-id="fc560-165"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="fc560-166"><strong>オブジェクトの種類</strong>: <strong>FormObject 名</strong>: 製品の一覧<strong>を保存</strong>:<strong>なし</strong></span><span class="sxs-lookup"><span data-stu-id="fc560-166"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="fc560-167">[製品リスト] フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fc560-167">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc560-168"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="fc560-168"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="fc560-169"><strong>フォーム名</strong>: 製品の<strong>表示</strong>: <strong>FormData モード</strong>: <strong>AddWindow モード</strong>:<strong>標準</strong></span><span class="sxs-lookup"><span data-stu-id="fc560-169"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="fc560-170">[製品] フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="fc560-170">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc560-171"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="fc560-171"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="fc560-172"><strong>Item/アイテム</strong>: [フォーム]![製品]![SupplierID] <strong>Expression/式</strong>: SupplierID</span><span class="sxs-lookup"><span data-stu-id="fc560-172"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="fc560-173">[仕入先コード] コントロールを [仕入先] フォームの現在の仕入先に設定します。</span><span class="sxs-lookup"><span data-stu-id="fc560-173">Set the SupplierID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc560-174"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="fc560-174"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="fc560-175"><strong>Control Name/コントロール名</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="fc560-175"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="fc560-176">[カテゴリ ID] コントロールに移動します。</span><span class="sxs-lookup"><span data-stu-id="fc560-176">Go to the CategoryID control.</span></span></p></td>
</tr>
</tbody>
</table>

