---
title: SetValue マクロ アクション
TOCTitle: SetValue macro action
ms:assetid: a08be0c1-a053-45f9-b4ae-709fedc58e8b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820771(v=office.15)
ms:contentKeyID: 48546712
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6f407c5da2ca669025d5aec47685e6eb9732c72c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927103"
---
# <a name="setvalue-macro-action"></a><span data-ttu-id="2c735-102">SetValue マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="2c735-102">SetValue macro action</span></span>


<span data-ttu-id="2c735-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2c735-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="2c735-104">" **SetValue/値の代入** " アクションを使用すると、フォーム、フォーム データシート、またはレポートの Microsoft Access フィールド、コントロール、あるいはプロパティの値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="2c735-104">You can use the **SetValue** action to set the value of a Microsoft Access field, control, or property on a form, a form datasheet, or a report.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2c735-105">[!メモ] " <STRONG>SetValue/値の代入</STRONG> " アクションを使用して、オブジェクトを返す Access プロパティの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="2c735-105">You cannot use the <STRONG>SetValue</STRONG> action to set the value of an Access property that returns an object.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="2c735-p101">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2c735-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="2c735-108">設定</span><span class="sxs-lookup"><span data-stu-id="2c735-108">Setting</span></span>

<span data-ttu-id="2c735-109">" **SetValue/値の代入** " アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2c735-109">The **SetValue** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2c735-110">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="2c735-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="2c735-111">説明</span><span class="sxs-lookup"><span data-stu-id="2c735-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2c735-112"><strong>Item</strong></span><span class="sxs-lookup"><span data-stu-id="2c735-112"><strong>Item</strong></span></span></p></td>
<td><p><span data-ttu-id="2c735-p102">値を設定するフィールド、コントロール、またはプロパティの名前を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>アイテム</strong>] ボックスに、フィールド、コントロール、またはプロパティの名前を入力します。このアイテムを参照するには、<em>controlname</em> (マクロが呼び出されたフォームまたはレポートのコントロールの場合)、<strong>Forms</strong>!<em>formname</em>!<em>controlname</em> など、完全な構文を使用する必要があります。この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="2c735-p102">The name of the field, control, or property whose value you want to set. Enter the field, control, or property name in the <strong>Item</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You must use the full syntax to refer to this item, such as <em>controlname</em> (for a control on the form or report from which the macro was called) or <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c735-117"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="2c735-117"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="2c735-p103">このアイテムの値を設定するときに Access が使用する式を指定します。式のオブジェクトを参照するには、完全な構文を使用する必要があります。たとえば、Employees フォームの Salary コントロールの値を 10% 増やすには、Forms!Employees!Salary\*1.1. を使用します。この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="2c735-p103">The expression Access uses to set the value for this item. You must always use the full syntax to refer to any objects in the expression. For example, to increase the value in a Salary control on an Employees form by 10 percent, use Forms!Employees!Salary\*1.1. This is a required argument.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="2c735-122">等号 (=) を使用するべきではありません (<STRONG>=</STRONG>) この引数の式の前にします。</span><span class="sxs-lookup"><span data-stu-id="2c735-122">You shouldn't use an equal sign (<STRONG>=</STRONG>) before the expression in this argument.</span></span> <span data-ttu-id="2c735-123">場合は、アクセスが式を評価し、この引数の式としてこの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="2c735-123">If you do, Access evaluates the expression and then uses this value as the expression in this argument.</span></span> <span data-ttu-id="2c735-124">式が文字列の場合、予期しない結果が生じる。</span><span class="sxs-lookup"><span data-stu-id="2c735-124">This can produce unexpected results if the expression is a string.</span></span></P>


<p><span data-ttu-id="2c735-125">入力する場合など<strong>=&quot;文字列 1&quot; </strong> 、この引数を最初に評価され文字列 1 として表現します。</span><span class="sxs-lookup"><span data-stu-id="2c735-125">For example, if you type <strong>=&quot;String1&quot;</strong> for this argument, Access first evaluates the expression as String1.</span></span> <span data-ttu-id="2c735-126">[String1 コントロールまたはフォームやレポート、マクロと呼ばれることで、文字列 1 をという名前のプロパティを検索するため、この引数の式として使用します。</span><span class="sxs-lookup"><span data-stu-id="2c735-126">Then it uses String1 as the expression in this argument, expecting to find a control or property named String1 on the form or report that called the macro.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="2c735-127">[!メモ] Access データベース (.mdb または .accdb) では、[ <STRONG>ビルド</STRONG>] をクリックし、式ビルダーを使用して、この引数のどちらかに対して式を作成します。</span><span class="sxs-lookup"><span data-stu-id="2c735-127">In an Access database (.mdb or .accdb), click the <STRONG>Build</STRONG> button to use the Expression Builder to create an expression for either of these arguments.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="2c735-128">注釈</span><span class="sxs-lookup"><span data-stu-id="2c735-128">Remarks</span></span>

<span data-ttu-id="2c735-p106">このアクションを使用すると、フォーム、フォーム データシート、またはレポートのフィールドあるいはコントロールに対して値を設定できます。また、任意のビューのほぼすべてのコントロール、フォーム、およびレポートのプロパティに値を設定することもできます。マクロを使用して特定のプロパティを設定できるかどうか、およびどのビューでプロパティを設定できるかを確認するには、Visual Basic エディターのそのプロパティに関するヘルプ トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2c735-p106">You can use this action to set a value for a field or control on a form, a form datasheet, or a report. You can also set the value for almost all control, form, and report properties in any view. To find out whether a particular property can be set by using a macro and which views it can be set in, see the Help topic for that property in the Visual Basic Editor.</span></span>

<span data-ttu-id="2c735-132">フィールドに連結されたコントロールがフォームに含まれていない場合でも、フォームの基になるテーブル フィールドの値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="2c735-132">You can also set the value for a field in a form's underlying table even if the form doesn't contain a control bound to the field.</span></span> <span data-ttu-id="2c735-133">**フォーム**の構文を使用して、\!*フォーム*\!このようなフィールドの値を設定する**項目**] ボックスで*フィールド名*です。</span><span class="sxs-lookup"><span data-stu-id="2c735-133">Use the syntax **Forms**\!*formname*\!*fieldname* in the **Item** box to set the value for such a field.</span></span> <span data-ttu-id="2c735-134">**レポート**の構文を使用して、レポートの基になるテーブル内のフィールドを参照することもできます\!*レポート名*\!*フィールド名*をこのフィールドにバインドされているレポート上のコントロールが存在する必要がありますかで、フィールドを参照する必要がありますが、レポートの演算コントロールです。</span><span class="sxs-lookup"><span data-stu-id="2c735-134">You can also refer to a field in a report's underlying table by using the syntax **Reports**\!*reportname*\!*fieldname*, but there must be a control on the report bound to this field, or the field must be referred to in a calculated control on the report.</span></span>

<span data-ttu-id="2c735-p108">フォームのコントロールの値を設定する場合、" **SetValue/値の代入** " アクションでは、コントロールのフォームレベルの入力規則はトリガーされませんが、コントロールが連結コントロールの場合は、基になるフィールドのテーブルレベルの入力規則がトリガーされます。また、" **SetValue/値の代入** " アクションでは再計算もトリガーされます。ただし、この再計算はすぐには実行されません。すぐに再描画をトリガーし、再計算が強制的に行われるようにするには、" **RepaintObject/オブジェクトの再描画** " アクションを使用します。さらに、" **SetValue/値の代入** " アクションでコントロールに設定する値には、コントロールまたは基になるフィールドの **InputMask** プロパティで設定された定型入力は適用されません。</span><span class="sxs-lookup"><span data-stu-id="2c735-p108">If you set the value of a control on a form, the **SetValue** action doesn't trigger the control's form-level validation rules, but it does trigger the underlying field's table-level validation rules if the control is a bound control. The **SetValue** action also triggers recalculation, but the recalculation may not happen immediately. To trigger immediate repainting and force the recalculation to completion, use the **RepaintObject** action. The value you set in a control by using the **SetValue** action is also not affected by an input mask set in the control's or underlying field's **InputMask** property.</span></span>

<span data-ttu-id="2c735-p109">コントロールの **AfterUpdate** イベント プロパティによって指定されたマクロで " **SetValue/値の代入** " アクションを使用すると、そのコントロールの値を変更できます。ただし、コントロールの **BeforeUpdate** イベント プロパティで指定されたマクロで " **SetValue/値の代入** " アクションでは、そのコントロールの値を変更することはできません (ただし、" **SetValue/値の代入** " アクションを使用して、他のコントロールの値を変更することはできます)。また、フォームの **BeforeUpdate** または **AfterUpdate** プロパティで指定されたマクロで " **SetValue/値の代入** " アクションを使用して、カレント レコードのコントロールの値を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="2c735-p109">To change the value of a control, you can use the **SetValue** action in a macro specified by the control's **AfterUpdate** event property. However, you can't use the **SetValue** action in a macro specified by a control's **BeforeUpdate** event property to change the value of the control (although you can use the **SetValue** action to change the value of other controls). You can also use the **SetValue** action in a macro specified by the **BeforeUpdate** or **AfterUpdate** property of a form to change the value of any controls in the current record.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2c735-142">"<STRONG>SetValue/値の導入</STRONG>" アクションを使用して、次のコントロールの値を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="2c735-142">You can't use the <STRONG>SetValue</STRONG> action to set the value of the following controls:</span></span></P>
> <UL>
> <LI>
> <P><span data-ttu-id="2c735-143">レポートの連結コントロールおよび演算コントロール。</span><span class="sxs-lookup"><span data-stu-id="2c735-143">Bound controls and calculated controls on reports.</span></span></P>
> <LI>
> <P><span data-ttu-id="2c735-144">フォームの演算コントロール。</span><span class="sxs-lookup"><span data-stu-id="2c735-144">Calculated controls on forms.</span></span></P></LI></UL>




> [!TIP]
> <P><span data-ttu-id="2c735-p110">"<STRONG>SetValue/値の代入</STRONG>" アクションを使用すると、フォーム ビューのフォームを表示または非表示にできます。[<STRONG>アイテム</STRONG>] ボックスで <STRONG>Forms</STRONG>!<EM>formname</EM><STRONG>.Visible</STRONG> を、[<STRONG>式</STRONG>] ボックスで <STRONG>No</STRONG> または <STRONG>Yes</STRONG> を指定します。モーダル フォームの <STRONG>Visible</STRONG> プロパティを <STRONG>No</STRONG> に設定すると、フォームは非表示およびモードレスになります。このプロパティを <STRONG>Yes</STRONG> に表示すると、フォームは表示され、再度モーダルになります。</span><span class="sxs-lookup"><span data-stu-id="2c735-p110">You can use the <STRONG>SetValue</STRONG> action to hide or show a form in Form view. Enter <STRONG>Forms</STRONG>!<EM>formname</EM><STRONG>.Visible</STRONG> in the <STRONG>Item</STRONG> box and <STRONG>No</STRONG> or <STRONG>Yes</STRONG> in the <STRONG>Expression</STRONG> box. Setting a modal form's <STRONG>Visible</STRONG> property to <STRONG>No</STRONG> hides the form and makes it modeless. Setting the property to <STRONG>Yes</STRONG> displays the form and makes it modal again.</span></span></P>



<span data-ttu-id="2c735-p111">マクロで " **SetValue/値の代入** " アクションを使用してコントロールの値を変更するか新しいデータを追加した場合、ユーザー インターフェイスのこれらのコントロールのデータを変更または入力するときに発生するイベント ( **BeforeUpdate** 、 **BeforeInsert** 、 **Change** など) はトリガーされません。これらのイベントは、Visual Basic for Applications (VBA) モジュールを使用してコントロールの値を設定しても発生しません。</span><span class="sxs-lookup"><span data-stu-id="2c735-p111">Changing the value of or adding new data in a control by using the **SetValue** action in a macro doesn't trigger events such as **BeforeUpdate**, **BeforeInsert**, or **Change** that occur when you change or enter data in these controls in the user interface. These events also don't occur if you set the value of the control by using a Visual Basic for Applications (VBA) module.</span></span>

<span data-ttu-id="2c735-p112">このアクションは VBA モジュールでは使用できません。値は Visual Basic で直接設定します。</span><span class="sxs-lookup"><span data-stu-id="2c735-p112">This action isn't available in a VBA module. Set the value directly in VBA.</span></span>

## <a name="example"></a><span data-ttu-id="2c735-153">例</span><span class="sxs-lookup"><span data-stu-id="2c735-153">Example</span></span>

<span data-ttu-id="2c735-154">**マクロによるコントロールの値の設定**</span><span class="sxs-lookup"><span data-stu-id="2c735-154">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="2c735-p113">次のマクロは、[仕入先] フォーム上のボタンから [商品の追加] フォームを開きます。このマクロは、" **Echo/エコー** "、" **CloseWindow/ウィンドウを閉じる** "、" **OpenForm/フォームを開く** "、" **SetValue/値の代入** "、および " **GoToControl/コントロールの移動** " の各アクションの使い方を示します。" **SetValue/値の代入** " アクションは、[商品] フォームの [仕入先コード] コントロールを [仕入先] フォームの現在の仕入先に設定します。次に、" **GoToControl/コントロールの移動** " アクションがフォーカスを [カテゴリ ID] フィールドに移動します。ユーザーは、ここで、新しい製品のデータの入力を開始できます。このマクロを [仕入先] フォームの [商品の追加] ボタンに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c735-p113">The following macro opens the Add Products form from a button on the Suppliers form. It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions. The **SetValue** action sets the SupplierID control on the Products form to the current supplier on the Suppliers form. The **GoToControl** action then moves the focus to the CategoryID field, where you can begin to enter data for the new product. This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2c735-160">アクション</span><span class="sxs-lookup"><span data-stu-id="2c735-160">Action</span></span></p></th>
<th><p><span data-ttu-id="2c735-161">引数: 設定値</span><span class="sxs-lookup"><span data-stu-id="2c735-161">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="2c735-162">コメント</span><span class="sxs-lookup"><span data-stu-id="2c735-162">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2c735-163"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="2c735-163"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="2c735-164"><strong>Echo On/エコーの設定</strong>: <strong>No/いいえ</strong></span><span class="sxs-lookup"><span data-stu-id="2c735-164"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="2c735-165">画面の更新は停止しますが、マクロは実行されています。</span><span class="sxs-lookup"><span data-stu-id="2c735-165">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c735-166"><strong>CloseWindow</strong></span><span class="sxs-lookup"><span data-stu-id="2c735-166"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="2c735-167"><strong>オブジェクトの種類</strong>: <strong>FormObject 名</strong>: 製品の一覧<strong>を保存</strong>:<strong>なし</strong></span><span class="sxs-lookup"><span data-stu-id="2c735-167"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="2c735-168">[製品リスト] フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2c735-168">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c735-169"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="2c735-169"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="2c735-170"><strong>フォーム名</strong>: 製品の<strong>表示</strong>: <strong>FormData モード</strong>: <strong>AddWindow モード</strong>:<strong>標準</strong></span><span class="sxs-lookup"><span data-stu-id="2c735-170"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="2c735-171">[製品] フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="2c735-171">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2c735-172"><strong>値の代入</strong></span><span class="sxs-lookup"><span data-stu-id="2c735-172"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="2c735-173"><strong>Item/アイテム</strong>: [フォーム]![製品]![SupplierID] <strong>Expression/式</strong>: SupplierID</span><span class="sxs-lookup"><span data-stu-id="2c735-173"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="2c735-174">[仕入先コード] コントロールを [仕入先] フォームの現在の仕入先に設定します。</span><span class="sxs-lookup"><span data-stu-id="2c735-174">Set the SupplierID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2c735-175"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="2c735-175"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="2c735-176"><strong>Control Name/コントロール名</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="2c735-176"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="2c735-177">[カテゴリ ID] コントロールに移動します。</span><span class="sxs-lookup"><span data-stu-id="2c735-177">Go to the CategoryID control.</span></span></p></td>
</tr>
</tbody>
</table>

