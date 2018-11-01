---
title: OpenForm マクロ アクション
TOCTitle: OpenForm Macro Action
ms:assetid: c519a9d7-99d4-4765-ad96-59c3fe1be9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823095(v=office.15)
ms:contentKeyID: 48547604
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 140ac927089a89fa5c77034c9e33d4cd1519e41c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870262"
---
# <a name="openform-macro-action"></a><span data-ttu-id="89e31-102">OpenForm マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="89e31-102">OpenForm Macro Action</span></span>


<span data-ttu-id="89e31-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="89e31-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="89e31-p101">" **OpenForm/フォームを開く** " アクションを使用すると、フォーム ビュー、フォーム デザイン ビュー、印刷プレビュー、またはデータシート ビューのいずれかで、フォームを開くことができます。フォームを開くときのデータ入力モードやウィンドウ モードの設定を行ったり、フォームで表示するレコードを制限したりできます。</span><span class="sxs-lookup"><span data-stu-id="89e31-p101">You can use the **OpenForm** action to open a form in Form view, Design view, Print Preview, or Datasheet view. You can select data entry and window modes for the form and restrict the records that the form displays.</span></span>

## <a name="setting"></a><span data-ttu-id="89e31-106">設定</span><span class="sxs-lookup"><span data-stu-id="89e31-106">Setting</span></span>

<span data-ttu-id="89e31-107">**OpenForm/フォームを開く** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="89e31-107">The **OpenForm** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89e31-108">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="89e31-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="89e31-109">説明</span><span class="sxs-lookup"><span data-stu-id="89e31-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89e31-110"><strong>Form Name/フォーム名</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-110"><strong>Form Name</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-111">開くフォームの名前です。</span><span class="sxs-lookup"><span data-stu-id="89e31-111">The name of the form to open.</span></span> <span data-ttu-id="89e31-112">マクロ ビルダー] ウィンドウの [<strong>フォーム名</strong>] ボックス、[<strong>アクションの引数</strong>] セクションでは、現在のデータベースのすべてのフォームを示しています。</span><span class="sxs-lookup"><span data-stu-id="89e31-112">The <strong>Form Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all forms in the current database.</span></span> <span data-ttu-id="89e31-113">この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="89e31-113">This is a required argument.</span></span> <span data-ttu-id="89e31-114"><strong>ライブラリ データベースで、このアクション</strong>を含むマクロを実行する場合は、最初の検索にライブラリ データベースで、し、[現在のデータベース内にこの名前のフォームです。</span><span class="sxs-lookup"><span data-stu-id="89e31-114">If you run a macro containing the <strong>OpenForm</strong> action in a library database, Microsoft Access first looks for the form with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89e31-115"><strong>View</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-115"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-p103">フォームを開くときのビューを指定します。[<strong>ビュー</strong>] ボックスで、[<strong>フォーム ビュー</strong>]、[<strong>デザイン ビュー</strong>]、[<strong>印刷プレビュー</strong>]、[<strong>データシート ビュー</strong>]、[<strong>ピボットテーブル ビュー</strong>]、または [<strong>ピボットグラフ ビュー</strong>] をクリックします。既定値は [<strong>フォーム ビュー</strong>] です。  
 
</span><span class="sxs-lookup"><span data-stu-id="89e31-p103">The view in which the form will open. Click <strong>Form</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>Datasheet</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Form</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="89e31-p104">"<STRONG>View/ビュー</STRONG>" 引数の設定は、フォームの "<STRONG>DefaultView/既定のビュー</STRONG>" および "<STRONG>ViewsAllowed/ビュー設定</STRONG>" プロパティの設定よりも優先されます。たとえば、フォームの "<STRONG>ViewsAllowed/ビュー設定</STRONG>" プロパティが [<STRONG>データシート</STRONG>] に設定されていても、"<STRONG>OpenForm/フォームを開く</STRONG>" アクションを使用すると、フォーム ビューでフォームを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="89e31-p104">The <STRONG>View</STRONG> argument setting overrides the settings of the form's <STRONG>DefaultView</STRONG> and <STRONG>ViewsAllowed</STRONG> properties. For example, if a form's <STRONG>ViewsAllowed</STRONG> property is set to <STRONG>Datasheet</STRONG>, you can still use the <STRONG>OpenForm</STRONG> action to open the form in Form view.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89e31-121"><strong>Filter Name</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-121"><strong>Filter Name</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-p105">フォームのレコードを制限するか並べ替えるフィルターを指定します。既存のクエリ名、またはクエリとして保存されているフィルターの名前を入力することができます。ただし、そのクエリでは、開こうとしているフォーム内のすべてのフィールドを含めるか、クエリの "<strong>OutputAllFields/全フィールド表示</strong>" プロパティを [<strong>はい</strong>] に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89e31-p105">A filter that restricts or sorts the form's records. You can enter the name of either an existing query or a filter that was saved as a query. However, the query must include all the fields in the form you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89e31-125"><strong>Where Condition</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-125"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-126">有効な SQL WHERE 句 (単語なしで) フォームからレコードを選択するときに使用する式には、テーブルまたはクエリの基になるか。</span><span class="sxs-lookup"><span data-stu-id="89e31-126">A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the form's underlying table or query.</span></span> <span data-ttu-id="89e31-127"><strong>フィルター名</strong>の引数を指定してフィルターを選択する場合は、フィルターの結果に次の WHERE 句が適用されます。</span><span class="sxs-lookup"><span data-stu-id="89e31-127">If you select a filter with the <strong>Filter Name</strong> argument, Access applies this WHERE clause to the results of the filter.</span></span> <span data-ttu-id="89e31-128">フォームを開くし、別のフォーム上のコントロールの値で指定されているレコードを制限する、次の式を使用して、:<em>フィールド名</em>の<strong>[</strong><strong>] フォームを =! [</strong><em>フォーム名</em><strong>]![</strong><em>名の他のフォームに置き換えます</em><strong>]</strong>の基になるテーブルまたはクエリ、フォームを開きたいので、フィールド名と<em>フィールド名</em>を交換しています。</span><span class="sxs-lookup"><span data-stu-id="89e31-128">To open a form and restrict its records to those specified by the value of a control on another form, use the following expression: <strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on other form</em><strong>]</strong> Replace <em>fieldname</em> with the name of a field in the underlying table or query of the form you want to open.</span></span> <span data-ttu-id="89e31-129"><em>フォーム名</em>と<em>名の他のフォームに置き換えます</em>を他のフォームと一致する最初のフォーム内のレコードが必要な値を含むその他のフォーム上のコントロールの名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="89e31-129">Replace <em>formname</em> and <em>controlname on other form</em> with the name of the other form and the control on the other form that contains the value you want records in the first form to match.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="89e31-p107">"<STRONG>Where Condition/Where 条件式</STRONG>" 引数の最大長は 255 バイトです。これより長くて複雑な SQL WHERE 句を入力する必要がある場合は、代わりに Visual Basic for Applications (VBA) モジュールで、<STRONG>DoCmd</STRONG> オブジェクトの <STRONG>OpenForm</STRONG> メソッドを使用します。VBA では、最大 32,768 バイトの SQL WHERE 句のステートメントを入力できます。</span><span class="sxs-lookup"><span data-stu-id="89e31-p107">The maximum length of the <STRONG>Where Condition</STRONG> argument is 255 characters. If you need to enter a more complex SQL WHERE clause longer than this, use the <STRONG>OpenForm</STRONG> method of the <STRONG>DoCmd</STRONG> object in a Visual Basic for Applications (VBA) module instead. You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89e31-133"><strong>Data Mode/データ モード</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-133"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-134">フォームのデータ入力モードです。</span><span class="sxs-lookup"><span data-stu-id="89e31-134">The data entry mode for the form.</span></span> <span data-ttu-id="89e31-135">この設定は、フォーム ビューまたはデータシート ビューで開いたフォームにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="89e31-135">This applies only to forms opened in Form view or Datasheet view.</span></span> <span data-ttu-id="89e31-136">新しいレコードの追加を許可して、既存のレコードの編集を禁止する場合は [ <strong>追加</strong>]、既存のレコードの編集および新しいレコードの追加を許可する場合は [ <strong>編集</strong>]、レコードの表示のみを許可する場合は [ <strong>読み取り専用</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="89e31-136">Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records).</span></span> <span data-ttu-id="89e31-137">既定値は [ <strong>編集</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="89e31-137">The default is <strong>Edit</strong>.</span></span> <span data-ttu-id="89e31-138"><strong>メモ</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-138"><strong>Notes</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="89e31-p109">"<strong>Data Mode/データ モード</strong>" 引数の設定は、フォームの "<strong>AllowEdits/更新の許可</strong>"、"<strong>AllowDeletions/削除の許可</strong>"、"<strong>AllowAdditions/追加の許可</strong>"、および "<strong>DataEntry/データ入力用</strong>" プロパティの設定よりも優先されます。たとえば、フォームの "<strong>AllowEdits/更新の許可</strong>" プロパティが [<strong>いいえ</strong>] に設定されていても、"<strong>OpenForm/フォームを開く</strong>" アクションを使用すると、編集モードでフォームを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="89e31-p109">The <strong>Data Mode</strong> argument setting overrides the settings of the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties. For example, if a form's <strong>AllowEdits</strong> property is set to <strong>No</strong>, you can still use the <strong>OpenForm</strong> action to open the form in Edit mode.</span></span></p></li>
<li><p><span data-ttu-id="89e31-141">この引数を指定しないと、フォームは、そのフォームの "<strong>AllowEdits/更新の許可</strong>"、"<strong>AllowDeletions/削除の許可</strong>"、"<strong>AllowAdditions/追加の許可</strong>"、および "<strong>DataEntry/データ入力用</strong>" プロパティによって設定されたデータ入力モードで開きます。</span><span class="sxs-lookup"><span data-stu-id="89e31-141">If you leave this argument blank, Access opens the form in the data entry mode set by the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89e31-142"><strong>Window Mode</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-142"><strong>Window Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-p110">フォームを開くときのウィンドウ モードを指定します。フォームのプロパティで設定されたモードで開く場合は [<strong>標準</strong>]、フォームを非表示にする場合は [<strong>非表示</strong>]、画面の下部に小さなタイトル バーにフォームを最小化する場合は [<strong>アイコン</strong>]、フォームの "<strong>Modal/作業ウィンドウ固定</strong>" および "<strong>PopUp/ポップアップ</strong>" プロパティを [<strong>はい</strong>] に設定する場合は [<strong>ダイアログ</strong>] をクリックします。既定値は [<strong>標準</strong>] です。</span><span class="sxs-lookup"><span data-stu-id="89e31-p110">The window mode in which the form opens. Click <strong>Normal</strong> (the form opens in the mode set by its properties), <strong>Hidden</strong> (the form is hidden), <strong>Icon</strong> (the form opens minimized as a small title bar at the bottom of the screen), or <strong>Dialog</strong> (the form's <strong>Modal</strong> and <strong>PopUp</strong> properties are set to <strong>Yes</strong>). The default is <strong>Normal</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="89e31-p111"><STRONG>Window Mode</STRONG> 引数の設定値によっては、タブ付きドキュメントを使用していると、適用されない場合があります。ウィンドウを重ねて表示するように切り替えるには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="89e31-p111">Some <STRONG>Window Mode</STRONG> argument settings do not apply when using tabbed documents. To switch to overlapping windows:</span></span></P>


<p></p>
<ol>
<li><p><span data-ttu-id="89e31-148">ファイル] タブをクリックし、[<strong>オプション</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="89e31-148">Click the File tab and then click <strong>Options</strong>.</span></span></p></li>
<li><p><span data-ttu-id="89e31-149">[ <strong>Access のオプション</strong>] ダイアログ ボックスの [ <strong>カレント データベース</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="89e31-149">In the <strong>Access Options</strong> dialog box, click <strong>Current Database</strong>.</span></span></p></li>
<li><p><span data-ttu-id="89e31-150">[<strong>アプリケーション オプション</strong>] の [<strong>ドキュメント ウィンドウ オプション</strong>] で [<strong>ウィンドウを重ねて表示する</strong>] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="89e31-150">In the <strong>Application Options</strong>section, under <strong>Document Window Options</strong>, click <strong>Overlapping Windows</strong>.</span></span></p></li>
<li><p><span data-ttu-id="89e31-151">[ <strong>OK</strong>] をクリックして、データベースを閉じて再度開きます。</span><span class="sxs-lookup"><span data-stu-id="89e31-151">Click <strong>OK</strong>, then close and reopen the database.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="89e31-152">注釈</span><span class="sxs-lookup"><span data-stu-id="89e31-152">Remarks</span></span>

<span data-ttu-id="89e31-153">このアクションの動作は、ナビゲーション ウィンドウでフォームをダブルクリックした場合や、ナビゲーション ウィンドウでフォームを右クリックしてビューを選択した場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="89e31-153">This action is similar to double-clicking a form in the Navigation Pane, or right-clicking the form in the Navigation Pane and then selecting a view.</span></span>

<span data-ttu-id="89e31-p112">フォームは作業ウィンドウ固定 (モーダル) またはモードレスで使用できます。作業ウィンドウ固定 (モーダル) の場合、フォームを閉じるか非表示にしないとユーザーが他のアクションを実行できません。モードレスの場合は、フォームを開いたままユーザーが他のウィンドウに移動できます。また、ポップアップ フォームとしてフォームを開くこともできます。これは、情報の表示または収集に使用されるフォームで、常に他の Access ウィンドウよりも前面に表示されます。" **Modal/作業ウィンドウ固定** " または " **PopUp/ポップアップ** " プロパティは、フォームをデザインするときに設定します。" **Window Mode/ウィンドウ モード** " 引数に [ **標準**] を指定すると、フォームはこれらのプロパティの設定で指定されたモードで開きます。 **Window Mode/ウィンドウ モード** " 引数に [ **ダイアログ**] を指定すると、プロパティは両方とも [ **はい** ] に設定されます。非表示のフォームを表示した場合、またはアイコンとして開かれたフォームのサイズを元に戻した場合は、プロパティによって指定されたモードになります。</span><span class="sxs-lookup"><span data-stu-id="89e31-p112">A form can be modal (it must be closed or hidden before the user can perform any other action) or modeless (the user can move to other windows while the form is open). It can also be a pop-up form (a form used to collect or display information that remains on top of all other Access windows). You set the **Modal** and **PopUp** properties when you design the form. If you use **Normal** for the **Window Mode** argument, the form opens in the mode specified by these property settings. If you use **Dialog** for the **Window Mode** argument, these properties are both set to **Yes**. A form opened as hidden or as an icon returns to the mode specified by its property settings when you show or restore it.</span></span>

<span data-ttu-id="89e31-p113">" **Window Mode/ウィンドウ モード** " 引数を [ **ダイアログ**] に設定してフォームを開くと、フォームが閉じるか非表示になるまでマクロが中断されます。フォームを非表示にするには、" **SetValue/値の代入** " アクションを使用して、 **Visible** プロパティを **No** に設定します。</span><span class="sxs-lookup"><span data-stu-id="89e31-p113">When you open a form with the **Window Mode** argument set to **Dialog**, Access suspends the macro until the form is closed or hidden. You can hide a form by setting its **Visible** property to **No** by using the **SetValue** action.</span></span>


> [!TIP]
> <P><span data-ttu-id="89e31-p114">[!ヒント] フォームをナビゲーション ウィンドウで選択し、マクロのアクション行にドラッグすると、フォームをフォーム ビューで開く " <STRONG>OpenForm/フォームを開く</STRONG> " アクションが自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="89e31-p114">You can select a form in the Navigation Pane and drag it to a macro action row. This automatically creates an <STRONG>OpenForm</STRONG> action that opens the form in Form view.</span></span></P>



<span data-ttu-id="89e31-164">フィルターおよび WHERE 条件式を指定すると、フォームの " **Filter/フィルター** " プロパティの設定値として使用されます。</span><span class="sxs-lookup"><span data-stu-id="89e31-164">The filter and WHERE condition you apply become the setting of the form's **Filter** property.</span></span>

## <a name="examples"></a><span data-ttu-id="89e31-165">例</span><span class="sxs-lookup"><span data-stu-id="89e31-165">Examples</span></span>

<span data-ttu-id="89e31-166">**マクロによるコントロールの値の設定**</span><span class="sxs-lookup"><span data-stu-id="89e31-166">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="89e31-p115">次のマクロは、[仕入先] フォーム上のボタンから [商品の追加] フォームを開きます。このマクロは、" **Echo/エコー** "、" **CloseWindow/ウィンドウを閉じる** "、" **OpenForm/フォームを開く** "、" **SetValue/値の代入** "、および " **GoToControl/コントロールの移動** " の各アクションの使い方を示します。" **SetValue/値の代入** " アクションは、[商品] フォームの [仕入先コード] コントロールを [仕入先] フォームの現在の仕入先に設定します。次に、" **GoToControl/コントロールの移動** " アクションがフォーカスを [カテゴリ ID] フィールドに移動します。ユーザーは、ここで、新しい製品のデータの入力を開始できます。このマクロを [仕入先] フォームの [商品の追加] ボタンに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="89e31-p115">The following macro opens the Add Products form from a button on the Suppliers form. It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions. The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form. The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product. This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89e31-172">アクション</span><span class="sxs-lookup"><span data-stu-id="89e31-172">Action</span></span></p></th>
<th><p><span data-ttu-id="89e31-173">引数: 設定値</span><span class="sxs-lookup"><span data-stu-id="89e31-173">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="89e31-174">コメント</span><span class="sxs-lookup"><span data-stu-id="89e31-174">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89e31-175"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-175"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-176"><strong>Echo On/エコーの設定</strong>: <strong>No/いいえ</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-176"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-177">画面の更新は停止しますが、マクロは実行されています。</span><span class="sxs-lookup"><span data-stu-id="89e31-177">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89e31-178"><strong>CloseWindow</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-178"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-179"><strong>オブジェクトの種類</strong>: <strong>FormObject 名</strong>: 製品の一覧<strong>を保存</strong>:<strong>なし</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-179"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-180">[製品リスト] フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="89e31-180">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89e31-181"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-181"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-182"><strong>フォーム名</strong>: 製品の<strong>表示</strong>: <strong>FormData モード</strong>: <strong>AddWindow モード</strong>:<strong>標準</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-182"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-183">[製品] フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="89e31-183">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89e31-184"><strong>値の代入</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-184"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-185"><strong>Item/アイテム</strong>: [フォーム]![製品]![SupplierID] <strong>Expression/式</strong>: SupplierID</span><span class="sxs-lookup"><span data-stu-id="89e31-185"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="89e31-186">[仕入先コード] コントロールを [仕入先] フォームの現在の仕入先に設定します。</span><span class="sxs-lookup"><span data-stu-id="89e31-186">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89e31-187"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-187"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-188"><strong>Control Name/コントロール名</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="89e31-188"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="89e31-189">[カテゴリ ID] コントロールに移動します。</span><span class="sxs-lookup"><span data-stu-id="89e31-189">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="89e31-p116">次のマクロは、[仕入先] フォームの右下に [製品リスト] フォームを開き、現在の仕入先の商品を表示します。このマクロは、" **Echo/エコー** "、" **MessageBox/メッセージボックス** "、" **GoToControl/コントロールの移動** "、" **StopMacro/マクロの中止** "、" **OpenForm/フォームを開く** "、および " **MoveAndSizeWindow/ウィンドウの移動とサイズ変更** " の各アクションの使い方を示します。また、" **MessageBox/メッセージボックス** "、" **"GoToControl/コントロールの移動** "、" **StopMacro/マクロの中止** " の各アクションで条件式を使用する方法も示しています。このマクロを [仕入先] フォームの [商品の参照] ボタンに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="89e31-p116">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products. It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions. It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions. This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<span data-ttu-id="89e31-194">**マクロによるフォームの同期**</span><span class="sxs-lookup"><span data-stu-id="89e31-194">**Synchronize forms by using a macro**</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89e31-195">条件</span><span class="sxs-lookup"><span data-stu-id="89e31-195">Condition</span></span></p></th>
<th><p><span data-ttu-id="89e31-196">アクション</span><span class="sxs-lookup"><span data-stu-id="89e31-196">Action</span></span></p></th>
<th><p><span data-ttu-id="89e31-197">引数: 設定値</span><span class="sxs-lookup"><span data-stu-id="89e31-197">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="89e31-198">コメント</span><span class="sxs-lookup"><span data-stu-id="89e31-198">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="89e31-199"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-199"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-200"><strong>Echo On/エコーの設定</strong>: <strong>No/いいえ</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-200"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-201">画面の更新は停止しますが、マクロは実行されています。</span><span class="sxs-lookup"><span data-stu-id="89e31-201">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89e31-202">IsNull([SupplierID])</span><span class="sxs-lookup"><span data-stu-id="89e31-202">IsNull([SupplierID])</span></span></p></td>
<td><p><span data-ttu-id="89e31-203"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-203"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-204"><strong>Message/メッセージ</strong>: 表示する商品を扱う仕入先のレコードに移動し、[商品の参照] ボタンを再度クリックします。</span><span class="sxs-lookup"><span data-stu-id="89e31-204"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="89e31-205"><strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: 仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="89e31-205"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="89e31-206">[仕入先] フォームに現在の仕入先が存在しない場合、メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="89e31-206">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89e31-207">...</span><span class="sxs-lookup"><span data-stu-id="89e31-207"></span></span></p></td>
<td><p><span data-ttu-id="89e31-208"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-208"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-209"><strong>Control Name/コントロール名</strong>: 会社名</span><span class="sxs-lookup"><span data-stu-id="89e31-209"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="89e31-210">フォーカスを [仕入先名] コントロールに移動します。</span><span class="sxs-lookup"><span data-stu-id="89e31-210">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89e31-211">...</span><span class="sxs-lookup"><span data-stu-id="89e31-211"></span></span></p></td>
<td><p><span data-ttu-id="89e31-212"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-212"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="89e31-213">マクロを停止します。</span><span class="sxs-lookup"><span data-stu-id="89e31-213">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="89e31-214"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-214"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-215"><strong>フォーム名</strong>: 製品リストの<strong>表示</strong>: <strong>DatasheetFilter の名前</strong>: <strong>Where 条件式</strong>: [仕入先コード] = [Forms]![仕入先]![仕入先コード]<strong>データ モード</strong>:<strong>読み取り OnlyWindow モード</strong>:<strong>標準</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-215"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-216">[製品リスト] フォームを開き、現在の仕入先の製品を表示します。</span><span class="sxs-lookup"><span data-stu-id="89e31-216">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="89e31-217"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="89e31-217"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="89e31-218"><strong>右</strong>: 0.7799&quot; <strong>ダウン</strong>: 1.8&quot;</span><span class="sxs-lookup"><span data-stu-id="89e31-218"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="89e31-219">[製品リスト] を [仕入先] フォームの右下に配置します。</span><span class="sxs-lookup"><span data-stu-id="89e31-219">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

