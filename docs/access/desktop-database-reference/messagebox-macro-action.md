---
title: MessageBox マクロ アクション
TOCTitle: MessageBox Macro Action
ms:assetid: 326a0e68-38fb-4f81-b319-5a70caa5aec4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192304(v=office.15)
ms:contentKeyID: 48544077
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd2600164941555c584bb91b827debfd4074ea18
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478333"
---
# <a name="messagebox-macro-action"></a><span data-ttu-id="feffb-102">MessageBox マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="feffb-102">MessageBox Macro Action</span></span>


<span data-ttu-id="feffb-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="feffb-103">**Applies to**: Access 2013 | Office 2013</span></span>




<span data-ttu-id="feffb-p101">" **MessageBox/メッセージボックス** " アクションを使用すると、警告または情報メッセージが含まれるメッセージ ボックスを表示できます。たとえば、" **MessageBox/メッセージボックス** " アクションは入力検査マクロで使用できます。コントロールまたはレコードがマクロの入力検査の条件に適合しない場合は、メッセージ ボックスが表示され、エラー メッセージと入力できるデータの種類に関する説明が示されます。</span><span class="sxs-lookup"><span data-stu-id="feffb-p101">You can use the **MessageBox** action to display a message box containing a warning or an informational message. For example, you can use the **MessageBox** action with validation macros. When a control or record fails a validation condition in the macro, a message box can display an error message and provide instructions about the kind of data that should be entered.</span></span>

## <a name="setting"></a><span data-ttu-id="feffb-107">設定</span><span class="sxs-lookup"><span data-stu-id="feffb-107">Setting</span></span>

<span data-ttu-id="feffb-108">**MessageBox/メッセージボックス** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="feffb-108">The **MessageBox** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="feffb-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="feffb-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="feffb-110">説明</span><span class="sxs-lookup"><span data-stu-id="feffb-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="feffb-111"><strong>Message</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-111"><strong>Message</strong></span></span></p></td>
<td><p><span data-ttu-id="feffb-p102">メッセージ ボックス内のテキストです。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>メッセージ</strong>] ボックスに、メッセージ テキストを入力します。255 文字までの文字列または式を入力できます (式の前には等号 (=) を付けます)。</span><span class="sxs-lookup"><span data-stu-id="feffb-p102">The text in the message box. Enter the message text in the <strong>Message</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You can type up to 255 characters or enter an expression (preceded by an equal sign).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feffb-115"><strong>Beep</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-115"><strong>Beep</strong></span></span></p></td>
<td><p><span data-ttu-id="feffb-p103">メッセージが表示されるときにコンピューターのスピーカーから警告音を鳴らすかどうかを指定します。[<strong>はい</strong>] (警告音を鳴らす) または [<strong>いいえ</strong>] (警告音を鳴らさない) をクリックします。既定値は [<strong>はい</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="feffb-p103">Specifies whether your computer's speaker sounds a beep tone when the message displays. Click <strong>Yes</strong> (sound the beep tone) or <strong>No</strong> (don't sound the beep tone). The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feffb-119"><strong>型</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-119"><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="feffb-p104">メッセージ ボックスの種類を指定します。種類ごとにアイコンが異なります。[<strong>なし</strong>]、[<strong>警告</strong>]、[<strong>注意?</strong>]、[<strong>注意!</strong>]、または [<strong>情報</strong>] をクリックします。既定値は [<strong>なし</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="feffb-p104">The type of message box. Each type has a different icon. Click <strong>None</strong>, <strong>Critical</strong>, <strong>Warning?</strong>, <strong>Warning!</strong>, or <strong>Information</strong>. The default is <strong>None</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feffb-124"><strong>タイトル</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-124"><strong>Title</strong></span></span></p></td>
<td><p><span data-ttu-id="feffb-125">メッセージ ボックスのタイトル バーに表示されるテキストです。</span><span class="sxs-lookup"><span data-stu-id="feffb-125">The text displayed in the message box title bar.</span></span> <span data-ttu-id="feffb-126">タイトル バーの表示を持つことができますたとえば、&quot;顧客 ID の検証&quot;。</span><span class="sxs-lookup"><span data-stu-id="feffb-126">For example, you can have the title bar display &quot;Customer ID Validation&quot;.</span></span> <span data-ttu-id="feffb-127">この引数を空白のままにする場合は、 &quot;Access&quot;が表示されます。</span><span class="sxs-lookup"><span data-stu-id="feffb-127">If you leave this argument blank, &quot;Microsoft Access&quot; is displayed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="feffb-128">注釈</span><span class="sxs-lookup"><span data-stu-id="feffb-128">Remarks</span></span>

<span data-ttu-id="feffb-p106">" **MessageBox/メッセージボックス** " アクションを使用すると、Microsoft Access によって表示される組み込みエラー メッセージに似た書式のエラー メッセージを作成できます。" **MessageBox/メッセージボックス** " アクションにより、"Message/メッセージ" 引数の 3 つのセクションにメッセージを入力できます。各セクションは "@" 記号で区切ります。</span><span class="sxs-lookup"><span data-stu-id="feffb-p106">You can use the **MessageBox** action to create a formatted error message similar to built-in error messages displayed by Microsoft Access. The **MessageBox** action permits you to supply a message in three sections for the Message argument. You separate the sections with the "@" character.</span></span>

<span data-ttu-id="feffb-p107">次の例では、書式設定されたメッセージ ボックスを表示します。このメッセージ ボックスのメッセージはセクションに分けられています。メッセージのテキストの最初のセクションは、太字の見出しとして表示されます。2 番目のセクションは、見出しの下にプレーン テキストとして表示されます。3 番目のセクションは、2 番目のセクションの下にプレーン テキストとして表示されます。2 番目のセクションと 3 番目のセクションの間には空白行が挿入されます。</span><span class="sxs-lookup"><span data-stu-id="feffb-p107">The following example displays a formatted message box with a sectioned message. The first section of text in the message is displayed as a bold heading. The second section is displayed as plain text beneath that heading. The third section is displayed as plain text beneath the second section, with a blank line between them.</span></span>

<span data-ttu-id="feffb-136">" **Message/メッセージ** " 引数に次の文字列を入力します。</span><span class="sxs-lookup"><span data-stu-id="feffb-136">Type the following string in the **Message** argument:</span></span>

<span data-ttu-id="feffb-137">**間違ったボタン\!@This ボタンは、work.@Try は別です。**</span><span class="sxs-lookup"><span data-stu-id="feffb-137">**Wrong button\!@This button doesn't work.@Try another.**</span></span>

<span data-ttu-id="feffb-p108">Visual Basic for Applications (VBA) モジュールでは " **MessageBox/メッセージボックス** " アクションを実行することはできません。代わりに **MsgBox** 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="feffb-p108">You can't run the **MessageBox** action in a Visual Basic for Applications (VBA) module. Use the **MsgBox** function instead.</span></span>

## <a name="examples"></a><span data-ttu-id="feffb-140">例</span><span class="sxs-lookup"><span data-stu-id="feffb-140">Examples</span></span>

<span data-ttu-id="feffb-141">**マクロによるフォームの同期**</span><span class="sxs-lookup"><span data-stu-id="feffb-141">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="feffb-p109">次のマクロは、[仕入先] フォームの右下に [製品リスト] フォームを開き、現在の仕入先の商品を表示します。このマクロは、" **Echo/エコー** "、" **MessageBox/メッセージボックス** "、" **GoToControl/コントロールの移動** "、" **StopMacro/マクロの中止** "、" **OpenForm/フォームを開く** "、および " **MoveAndSizeWindow/ウィンドウの移動とサイズ変更** " の各アクションの使い方を示します。また、" **MessageBox/メッセージボックス** "、" **"GoToControl/コントロールの移動** "、" **StopMacro/マクロの中止** " の各アクションで条件式を使用する方法も示しています。このマクロを [仕入先] フォームの [商品の参照] ボタンに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="feffb-p109">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products. It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions. It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions. This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="feffb-146">条件</span><span class="sxs-lookup"><span data-stu-id="feffb-146">Condition</span></span></p></th>
<th><p><span data-ttu-id="feffb-147">アクション</span><span class="sxs-lookup"><span data-stu-id="feffb-147">Action</span></span></p></th>
<th><p><span data-ttu-id="feffb-148">引数: 設定値</span><span class="sxs-lookup"><span data-stu-id="feffb-148">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="feffb-149">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="feffb-149">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="feffb-150"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-150"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="feffb-151"><strong>Echo On/エコーの設定</strong>: <strong>No/いいえ</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-151"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="feffb-152">画面の更新は停止しますが、マクロは実行されています。</span><span class="sxs-lookup"><span data-stu-id="feffb-152">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feffb-153">IsNull([SupplierID])</span><span class="sxs-lookup"><span data-stu-id="feffb-153">IsNull([SupplierID])</span></span></p></td>
<td><p><span data-ttu-id="feffb-154"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-154"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="feffb-155"><strong>Message/メッセージ</strong>: 表示する商品を扱う仕入先のレコードに移動し、[商品の参照] ボタンを再度クリックします。</span><span class="sxs-lookup"><span data-stu-id="feffb-155"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="feffb-156"><strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: 仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="feffb-156"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="feffb-157">[仕入先] フォームに現在の仕入先が存在しない場合、メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="feffb-157">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feffb-158">...</span><span class="sxs-lookup"><span data-stu-id="feffb-158"></span></span></p></td>
<td><p><span data-ttu-id="feffb-159"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-159"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="feffb-160"><strong>Control Name/コントロール名</strong>: 会社名</span><span class="sxs-lookup"><span data-stu-id="feffb-160"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="feffb-161">フォーカスを [仕入先名] コントロールに移動します。</span><span class="sxs-lookup"><span data-stu-id="feffb-161">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feffb-162">...</span><span class="sxs-lookup"><span data-stu-id="feffb-162"></span></span></p></td>
<td><p><span data-ttu-id="feffb-163"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-163"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="feffb-164">マクロを停止します。</span><span class="sxs-lookup"><span data-stu-id="feffb-164">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="feffb-165"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-165"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="feffb-166"><strong>フォーム名</strong>: 製品リストの<strong>表示</strong>: <strong>DatasheetFilter の名前</strong>: <strong>Where 条件式</strong>: [仕入先コード] = [Forms]![仕入先]![仕入先コード]<strong>データ モード</strong>:<strong>読み取り OnlyWindow モード</strong>:<strong>標準</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-166"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="feffb-167">[製品リスト] フォームを開き、現在の仕入先の製品を表示します。</span><span class="sxs-lookup"><span data-stu-id="feffb-167">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="feffb-168"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-168"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="feffb-169"><strong>右</strong>: 0.7799&quot; <strong>ダウン</strong>: 1.8&quot;</span><span class="sxs-lookup"><span data-stu-id="feffb-169"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="feffb-170">[製品リスト] を [仕入先] フォームの右下に配置します。</span><span class="sxs-lookup"><span data-stu-id="feffb-170">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="feffb-171">**マクロによるデータの入力検査**</span><span class="sxs-lookup"><span data-stu-id="feffb-171">**Validate data by using a macro**</span></span>

<span data-ttu-id="feffb-p111">次の入力検査マクロでは、"仕入先" フォームで入力された郵便番号を確認します。このマクロでは、" **StopMacro/マクロの中止** "、" **MessageBox/メッセージボックス** "、" **CancelEvent/イベントのキャンセル** "、および " **GoToControl/コントロールの移動** " の各アクションの使い方を示します。条件式では、フォームのレコードに入力された都道府県と郵便番号を確認します。都道府県に対して郵便番号が正しく入力されていない場合、マクロはメッセージ ボックスを表示して、レコードの保存を取り消します。その後、PostalCode コントロールに戻り、エラーを修正することができます。このマクロは "仕入先" フォームの " **BeforeUpdate/更新前処理** " プロパティに設定します。</span><span class="sxs-lookup"><span data-stu-id="feffb-p111">The following validation macro checks the postal codes entered in a Suppliers form. It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions. A conditional expression checks the country/region and postal code entered in a record on the form. If the postal code isn't in the right format for the country/region, the macro displays a message box and cancels saving the record. It then returns you to the PostalCode control, where you can correct the error. This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="feffb-178">条件</span><span class="sxs-lookup"><span data-stu-id="feffb-178">Condition</span></span></p></th>
<th><p><span data-ttu-id="feffb-179">アクション</span><span class="sxs-lookup"><span data-stu-id="feffb-179">Action</span></span></p></th>
<th><p><span data-ttu-id="feffb-180">引数: 設定値</span><span class="sxs-lookup"><span data-stu-id="feffb-180">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="feffb-181">コメント</span><span class="sxs-lookup"><span data-stu-id="feffb-181">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="feffb-182">IsNull([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="feffb-182">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="feffb-183"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-183"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="feffb-184">[都道府県] の値が <strong>Null</strong> の場合は、郵便番号を検証できません。</span><span class="sxs-lookup"><span data-stu-id="feffb-184">If CountryRegion is <strong>Null</strong>, the postal code can't be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feffb-185">[都道府県](&quot;フランス&quot;、&quot;イタリア&quot;、&quot;スペイン&quot;) と Len([PostalCode]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="feffb-185">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([PostalCode]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="feffb-186"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-186"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="feffb-187"><strong>メッセージ</strong>: 郵便番号のコードは 5 文字である必要があります。</span><span class="sxs-lookup"><span data-stu-id="feffb-187"><strong>Message</strong>: The postal code must be 5 characters.</span></span> <span data-ttu-id="feffb-188"><strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: 郵便番号エラー</span><span class="sxs-lookup"><span data-stu-id="feffb-188"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="feffb-189">郵便番号が 7 文字でない場合にメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="feffb-189">If the postal code isn't 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feffb-190">...</span><span class="sxs-lookup"><span data-stu-id="feffb-190"></span></span></p></td>
<td><p><span data-ttu-id="feffb-191"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-191"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="feffb-192">イベントを取り消します。</span><span class="sxs-lookup"><span data-stu-id="feffb-192">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="feffb-193"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-193"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="feffb-194"><strong>コントロール名</strong>: [郵便番号]</span><span class="sxs-lookup"><span data-stu-id="feffb-194"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feffb-195">[都道府県](&quot;オーストラリア&quot;、&quot;シンガポール&quot;) と Len([PostalCode]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="feffb-195">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([PostalCode]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="feffb-196"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-196"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="feffb-197"><strong>メッセージ</strong>: 郵便番号のコードは 4 文字である必要があります。</span><span class="sxs-lookup"><span data-stu-id="feffb-197"><strong>Message</strong>: The postal code must be 4 characters.</span></span> <span data-ttu-id="feffb-198"><strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: 郵便番号エラー</span><span class="sxs-lookup"><span data-stu-id="feffb-198"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="feffb-199">郵便番号が 7 文字でない場合にメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="feffb-199">If the postal code isn't 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feffb-200">...</span><span class="sxs-lookup"><span data-stu-id="feffb-200"></span></span></p></td>
<td><p><span data-ttu-id="feffb-201"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-201"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="feffb-202">イベントを取り消します。</span><span class="sxs-lookup"><span data-stu-id="feffb-202">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="feffb-203"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-203"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="feffb-204"><strong>コントロール名</strong>: [郵便番号]</span><span class="sxs-lookup"><span data-stu-id="feffb-204"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="feffb-205">([都道府県] =&quot;カナダ&quot;)([郵便番号] が気に入らない&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</span><span class="sxs-lookup"><span data-stu-id="feffb-205">([CountryRegion] = &quot;Canada&quot;) And ([PostalCode] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="feffb-206"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-206"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="feffb-207"><strong>メッセージ</strong>: 郵便番号のコードが有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="feffb-207"><strong>Message</strong>: The postal code is not valid.</span></span> <span data-ttu-id="feffb-208">カナダのコードの例: H1J 1C 3<strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: 郵便番号コードのエラー</span><span class="sxs-lookup"><span data-stu-id="feffb-208">Example of Canadian code: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="feffb-p115">[都道府県] が広島県で、郵便番号の上 3 桁が 720 ～ 739 でない場合にメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="feffb-p115">If the postal code isn't correct for Canada, display a message. (Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="feffb-211">...</span><span class="sxs-lookup"><span data-stu-id="feffb-211"></span></span></p></td>
<td><p><span data-ttu-id="feffb-212"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="feffb-212"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="feffb-213">イベントを取り消します。</span><span class="sxs-lookup"><span data-stu-id="feffb-213">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>
