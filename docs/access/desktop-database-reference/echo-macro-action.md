---
title: Echo マクロ アクション (デスクトップ データベース参照のアクセス)
TOCTitle: Echo macro action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 03eeab3884e093b7c22f8fd23d5471d1dc620bc8
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997456"
---
# <a name="echo-macro-action"></a><span data-ttu-id="7c42e-102">Echo マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="7c42e-102">Echo macro action</span></span>

<span data-ttu-id="7c42e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="7c42e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7c42e-p101">**Echo** アクションを使用すると、エコーが有効かどうかを指定できます。たとえば、このアクションを使用して、マクロの実行中にその結果を表示または非表示にすることができます。</span><span class="sxs-lookup"><span data-stu-id="7c42e-p101">You can use the **Echo** action to specify whether echo is turned on. For example, you can use this action to hide or show the results of a macro while it runs.</span></span>

## <a name="setting"></a><span data-ttu-id="7c42e-106">設定</span><span class="sxs-lookup"><span data-stu-id="7c42e-106">Setting</span></span>

> [!NOTE]
> <span data-ttu-id="7c42e-107">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。</span><span class="sxs-lookup"><span data-stu-id="7c42e-107">This action will not be allowed if the database is not trusted.</span></span>

<span data-ttu-id="7c42e-108">**Echo** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="7c42e-108">The **Echo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c42e-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="7c42e-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="7c42e-110">説明</span><span class="sxs-lookup"><span data-stu-id="7c42e-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c42e-111"><strong>Echo On/エコーの設定</strong></span><span class="sxs-lookup"><span data-stu-id="7c42e-111"><strong>Echo On</strong></span></span></p></td>
<td><p><span data-ttu-id="7c42e-p102">[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>エコーの設定</strong>] ボックスで、[ <strong>はい</strong>] (エコーをオンにする) または [ <strong>いいえ</strong>] (エコーをオフにする) をクリックします。既定値は [ <strong>はい</strong>] です。  </span><span class="sxs-lookup"><span data-stu-id="7c42e-p102">Click <strong>Yes</strong> (turn echo on) or <strong>No</strong> (turn echo off) in the <strong>Echo On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c42e-114"><strong>Status Bar Text/ステータス バー テキスト</strong></span><span class="sxs-lookup"><span data-stu-id="7c42e-114"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="7c42e-115">エコーがオフのときにステータス バーに表示されるテキストです。</span><span class="sxs-lookup"><span data-stu-id="7c42e-115">The text to display in the status bar when echo is turned off.</span></span> <span data-ttu-id="7c42e-116">たとえば、エコーをオフにすると、ステータス バーを表示できます&quot;マクロが実行されます。&quot;</span><span class="sxs-lookup"><span data-stu-id="7c42e-116">For example, when echo is turned off, the status bar can display &quot;The macro is running.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7c42e-117">マクロが実行されると、画面の更新多くの場合ない情報が表示、マクロの機能に不可欠です。</span><span class="sxs-lookup"><span data-stu-id="7c42e-117">When a macro runs, screen updating often shows information not essential to the functioning of the macro.</span></span> <span data-ttu-id="7c42e-118">**Echo On/エコーの設定** 引数を [ **いいえ** ] に設定すると、画面を更新せずにマクロが実行されます。</span><span class="sxs-lookup"><span data-stu-id="7c42e-118">When you set the **Echo On** argument to **No**, the macro runs without updating the screen.</span></span> <span data-ttu-id="7c42e-119">マクロが完了すると、エコーが自動的にオンになり、ウィンドウが再描画されます。</span><span class="sxs-lookup"><span data-stu-id="7c42e-119">When the macro finishes, Access automatically turns echo back on and repaints the window.</span></span> <span data-ttu-id="7c42e-120">**Echo On/エコーの設定** 引数を [ **いいえ** ] に設定しても、マクロの機能またはその結果には影響しません。</span><span class="sxs-lookup"><span data-stu-id="7c42e-120">The **No** setting for the **Echo On** argument doesn't affect the functionality of the macro or its results.</span></span>

<span data-ttu-id="7c42e-p105">**Echo** アクションでは、エラー メッセージなどの作業ウィンドウ固定 (モーダル) ダイアログ ボックス、またはプロパティ シートなどのポップアップ フォームの表示は抑制されません。エコーがオフの場合でも、ダイアログ ボックスおよびポップアップフォームを使用して、情報を収集または表示することができます。すべてのメッセージまたはダイアログ ボックス (ユーザーが情報を入力する必要があるエラー メッセージ ボックスおよびダイアログ ボックスを除く) が表示されないようにするには、 **SetWarnings** アクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="7c42e-p105">The **Echo** action doesn't suppress the display of modal dialog boxes, such as error messages, or pop-up forms, such as property sheets. You can use dialog boxes and pop-up forms to gather or display information, even if echo is turned off. To suppress all message or dialog boxes except error message boxes and dialog boxes that require the user to enter information, use the **SetWarnings** action.</span></span>

<span data-ttu-id="7c42e-p106">**Echo** アクションは、マクロで複数回実行できます。これにより、マクロの実行中にステータス バーのテキストを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="7c42e-p106">You can run the **Echo** action more than once in a macro. This allows you to change the status bar text while the macro runs.</span></span>

<span data-ttu-id="7c42e-126">エコーをオフにすると、 **DisplayHourglassPointer** アクションを使用して、マクロ ポインターを砂時計のアイコン (または "待ち状態" に対して設定したマウス ポインターのアイコン) に変更し、マクロが実行中であることを視覚的に示すことができます。</span><span class="sxs-lookup"><span data-stu-id="7c42e-126">If you turn echo off, you can use the **DisplayHourglassPointer** action to change the mouse pointer into an hourglass icon (or whatever mouse pointer icon you've set for "Busy") to provide a visual indication that the macro is running.</span></span>

<span data-ttu-id="7c42e-127">Visual Basic for Applications (VBA) モジュールで **Echo** アクションを実行するには、 **DoCmd** オブジェクトの **Echo** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="7c42e-127">To run the **Echo** action in a Visual Basic for Applications (VBA) module, use the **Echo** method of the **DoCmd** object.</span></span>

## <a name="examples"></a><span data-ttu-id="7c42e-128">例</span><span class="sxs-lookup"><span data-stu-id="7c42e-128">Examples</span></span>

### <a name="set-the-value-of-a-control-by-using-a-macro"></a><span data-ttu-id="7c42e-129">マクロによるコントロールの値の設定</span><span class="sxs-lookup"><span data-stu-id="7c42e-129">Set the value of a control by using a macro</span></span>

<span data-ttu-id="7c42e-p107">次のマクロは、[仕入先] フォーム上のボタンから [商品の追加] フォームを開きます。このマクロは、" **Echo/エコー** "、" **CloseWindow/ウィンドウを閉じる** "、" **OpenForm/フォームを開く** "、" **SetValue/値の代入** "、および " **GoToControl/コントロールの移動** " の各アクションの使い方を示します。" **SetValue/値の代入** " アクションは、[商品] フォームの [仕入先コード] コントロールを [仕入先] フォームの現在の仕入先に設定します。次に、" **GoToControl/コントロールの移動** " アクションがフォーカスを [カテゴリ ID] フィールドに移動します。ユーザーは、ここで、新しい製品のデータの入力を開始できます。このマクロを [仕入先] フォームの [商品の追加] ボタンに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7c42e-p107">The following macro opens the Add Products form from a button on the Suppliers form. It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions. The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form. The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product. This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c42e-135">アクション</span><span class="sxs-lookup"><span data-stu-id="7c42e-135">Action</span></span></p></th>
<th><p><span data-ttu-id="7c42e-136">引数: 設定値</span><span class="sxs-lookup"><span data-stu-id="7c42e-136">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="7c42e-137">コメント</span><span class="sxs-lookup"><span data-stu-id="7c42e-137">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c42e-138"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="7c42e-138"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="7c42e-139"><strong>Echo On/エコーの設定</strong>: <strong>No/いいえ</strong></span><span class="sxs-lookup"><span data-stu-id="7c42e-139"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="7c42e-140">画面の更新は停止しますが、マクロは実行されています。</span><span class="sxs-lookup"><span data-stu-id="7c42e-140">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c42e-141"><strong>CloseWindow</strong></span><span class="sxs-lookup"><span data-stu-id="7c42e-141"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="7c42e-142"><strong>オブジェクトの種類</strong>: <strong>FormObject 名</strong>: 製品の一覧<strong>を保存</strong>:<strong>なし</strong></span><span class="sxs-lookup"><span data-stu-id="7c42e-142"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="7c42e-143">[製品リスト] フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7c42e-143">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c42e-144"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="7c42e-144"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="7c42e-145"><strong>フォーム名</strong>: 製品の<strong>表示</strong>: <strong>FormData モード</strong>: <strong>AddWindow モード</strong>:<strong>標準</strong></span><span class="sxs-lookup"><span data-stu-id="7c42e-145"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="7c42e-146">[製品] フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="7c42e-146">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c42e-147"><strong>値の代入</strong></span><span class="sxs-lookup"><span data-stu-id="7c42e-147"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="7c42e-148"><strong>Item/アイテム</strong>: [フォーム]![製品]![SupplierID] <strong>Expression/式</strong>: SupplierID</span><span class="sxs-lookup"><span data-stu-id="7c42e-148"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="7c42e-149">[仕入先コード] コントロールを [仕入先] フォームの現在の仕入先に設定します。</span><span class="sxs-lookup"><span data-stu-id="7c42e-149">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c42e-150"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="7c42e-150"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="7c42e-151"><strong>Control Name/コントロール名</strong>: CategoryID</span><span class="sxs-lookup"><span data-stu-id="7c42e-151"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="7c42e-152">[カテゴリ ID] コントロールに移動します。</span><span class="sxs-lookup"><span data-stu-id="7c42e-152">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="synchronize-forms-by-using-a-macro"></a><span data-ttu-id="7c42e-153">マクロによるフォームの同期</span><span class="sxs-lookup"><span data-stu-id="7c42e-153">Synchronize forms by using a macro</span></span>

<span data-ttu-id="7c42e-p108">次のマクロは、[仕入先] フォームの右下に [製品リスト] フォームを開き、現在の仕入先の商品を表示します。このマクロは、 **Echo** 、 **MessageBox** 、 **GoToControl** 、 **StopMacro** 、 **OpenForm** 、および **MoveAndSizeWindow** の各アクションの使い方を示します。また、 **MessageBox** 、 **GoToControl** 、 **StopMacro** の各アクションで条件式を使用する方法も示しています。このマクロを [仕入先] フォームの [商品のレビュー] ボタンに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7c42e-p108">The following macro opens the Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products. It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions. It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions. This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c42e-158">条件</span><span class="sxs-lookup"><span data-stu-id="7c42e-158">Condition</span></span></p></th>
<th><p><span data-ttu-id="7c42e-159">アクション</span><span class="sxs-lookup"><span data-stu-id="7c42e-159">Action</span></span></p></th>
<th><p><span data-ttu-id="7c42e-160">引数: 設定値</span><span class="sxs-lookup"><span data-stu-id="7c42e-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="7c42e-161">コメント</span><span class="sxs-lookup"><span data-stu-id="7c42e-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="7c42e-162"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="7c42e-162"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="7c42e-163"><strong>Echo On/エコーの設定</strong>: <strong>No/いいえ</strong></span><span class="sxs-lookup"><span data-stu-id="7c42e-163"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="7c42e-164">画面の更新は停止しますが、マクロは実行されています。</span><span class="sxs-lookup"><span data-stu-id="7c42e-164">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c42e-165">IsNull([仕入先コード])</span><span class="sxs-lookup"><span data-stu-id="7c42e-165">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="7c42e-166"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="7c42e-166"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="7c42e-167"><strong>Message/メッセージ</strong>: 表示する商品を扱う仕入先のレコードに移動し、[商品の参照] ボタンを再度クリックします。</span><span class="sxs-lookup"><span data-stu-id="7c42e-167"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="7c42e-168"><strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: 仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="7c42e-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="7c42e-169">[仕入先] フォームに現在の仕入先が存在しない場合、メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="7c42e-169">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c42e-170">...</span><span class="sxs-lookup"><span data-stu-id="7c42e-170"></span></span></p></td>
<td><p><span data-ttu-id="7c42e-171"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="7c42e-171"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="7c42e-172"><strong>Control Name/コントロール名</strong>: 会社名</span><span class="sxs-lookup"><span data-stu-id="7c42e-172"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="7c42e-173">フォーカスを [仕入先名] コントロールに移動します。</span><span class="sxs-lookup"><span data-stu-id="7c42e-173">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c42e-174">...</span><span class="sxs-lookup"><span data-stu-id="7c42e-174"></span></span></p></td>
<td><p><span data-ttu-id="7c42e-175"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="7c42e-175"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="7c42e-176">マクロを停止します。</span><span class="sxs-lookup"><span data-stu-id="7c42e-176">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="7c42e-177"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="7c42e-177"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="7c42e-178"><strong>フォーム名</strong>: 製品リストの<strong>表示</strong>: <strong>DatasheetFilter の名前</strong>: <strong>Where 条件式</strong>: [仕入先コード] = [Forms]![仕入先]![仕入先コード]<strong>データ モード</strong>:<strong>読み取り OnlyWindow モード</strong>:<strong>標準</strong></span><span class="sxs-lookup"><span data-stu-id="7c42e-178"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="7c42e-179">[製品リスト] フォームを開き、現在の仕入先の製品を表示します。</span><span class="sxs-lookup"><span data-stu-id="7c42e-179">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="7c42e-180"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="7c42e-180"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="7c42e-181"><strong>右</strong>: 0.7799&quot; <strong>ダウン</strong>: 1.8&quot;</span><span class="sxs-lookup"><span data-stu-id="7c42e-181"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="7c42e-182">[製品リスト] を [仕入先] フォームの右下に配置します。</span><span class="sxs-lookup"><span data-stu-id="7c42e-182">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

