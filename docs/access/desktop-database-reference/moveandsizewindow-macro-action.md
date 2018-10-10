---
title: MoveAndSizeWindow マクロ アクション
TOCTitle: MoveAndSizeWindow Macro Action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d423668f5ef53abf4216fa8f976c674474a752ed
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478169"
---
# <a name="moveandsizewindow-macro-action"></a><span data-ttu-id="dfe5d-102">MoveAndSizeWindow マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="dfe5d-102">MoveAndSizeWindow Macro Action</span></span>


<span data-ttu-id="dfe5d-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="dfe5d-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="dfe5d-p101">タブ付きドキュメントではなくウィンドウを重ねて使用するようにドキュメント ウィンドウ オプションを設定すると、" **MoveAndSizeWindow/ウィンドウの移動とサイズ変更** " アクションを使用して、アクティブ ウィンドウの移動またはサイズ変更を行うことができます。ドキュメント ウィンドウ オプションを設定する方法については、「注釈」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-p101">If you have set your document window options to use overlapping windows instead of tabbed documents, you can use the **MoveAndSizeWindow** action to move or resize the active window. For information on how to set document window options, see the Remarks section.</span></span>

## <a name="setting"></a><span data-ttu-id="dfe5d-106">設定</span><span class="sxs-lookup"><span data-stu-id="dfe5d-106">Setting</span></span>

<span data-ttu-id="dfe5d-107">" **MoveAndSizeWindow/ウィンドウの移動とサイズ変更** " アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-107">The **MoveAndSizeWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dfe5d-108">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="dfe5d-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="dfe5d-109">説明</span><span class="sxs-lookup"><span data-stu-id="dfe5d-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dfe5d-110"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="dfe5d-110"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="dfe5d-p102">移動またはサイズ変更するウィンドウの左上隅の水平位置を、そのウィンドウを表示するウィンドウの左端からの距離で指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>右</strong>] ボックスに、位置を入力します。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-p102">The new horizontal position of the window's upper-left corner, measured from the left edge of its containing window. Enter the position in the <strong>Right</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfe5d-113"><strong>Down</strong></span><span class="sxs-lookup"><span data-stu-id="dfe5d-113"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="dfe5d-114">移動またはサイズ変更するウィンドウの左上隅の垂直位置を、そのウィンドウを表示するウィンドウの上端からの距離で指定します。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-114">The new vertical position of the window's upper-left corner, measured from the top edge of its containing window.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dfe5d-115"><strong>Width</strong></span><span class="sxs-lookup"><span data-stu-id="dfe5d-115"><strong>Width</strong></span></span></p></td>
<td><p><span data-ttu-id="dfe5d-116">ウィンドウの幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-116">The window's new width.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfe5d-117"><strong>Height</strong></span><span class="sxs-lookup"><span data-stu-id="dfe5d-117"><strong>Height</strong></span></span></p></td>
<td><p><span data-ttu-id="dfe5d-118">ウィンドウの高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-118">The window's new height.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dfe5d-119">この引数を指定しないと、ウィンドウの現在の設定が使用されます。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-119">If you leave an argument blank, Microsoft Access uses the window's current setting.</span></span>

<span data-ttu-id="dfe5d-120">少なくとも 1 つの引数に対して値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-120">You must enter a value for at least one argument.</span></span>


> [!NOTE]
> <P><span data-ttu-id="dfe5d-121">[!メモ] 各測定値はインチまたはセンチメートル単位で指定します。どちらの単位を使用するかは、Windows コントロール パネルの地域の設定によって決まります。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-121">Each measurement is in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="dfe5d-122">注釈</span><span class="sxs-lookup"><span data-stu-id="dfe5d-122">Remarks</span></span>

<span data-ttu-id="dfe5d-123">タブ付きドキュメントではなくウィンドウを重ねて使用するようにアプリケーションを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-123">To set up an application to use overlapping windows instead of tabbed documents, use the following procedure:</span></span>

1.  <span data-ttu-id="dfe5d-124">次に、[ **オプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-124">and then click **Options**</span></span>

2.  <span data-ttu-id="dfe5d-125">[ **カレント データベース**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-125">Click **Current Database**.</span></span>

3.  <span data-ttu-id="dfe5d-126">[ **アプリケーション オプション**] の [ **ドキュメント ウィンドウ オプション**] で [ **ウィンドウを重ねて表示する**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-126">In the **Application Options** section, under **Document Window Options**, click **Overlapping Windows**.</span></span>

4.  <span data-ttu-id="dfe5d-127">[ **OK**] をクリックし、データベースを閉じて再度開きます。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-127">Click **OK**, and then close and reopen the database.</span></span>

<span data-ttu-id="dfe5d-p103">このアクションは、ウィンドウの [ **コントロール**] メニューの [ **移動**] または [ **サイズ**] をクリックした場合の操作と似ています。メニュー コマンドでは、キーボードの方向キーを使用してウィンドウの移動またはサイズ変更を行います。" **MoveAndSizeWindow/ウィンドウの移動とサイズ変更** " アクションの場合、位置とサイズの値を直接入力します。マウスを使用して、ウィンドウの移動およびサイズ変更を行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-p103">This action is similar to clicking **Move** or **Size** on the window's **Control** menu. With the menu commands, you use the keyboard's arrow keys to move or resize the window. With the **MoveAndSizeWindow** action, you enter the position and size measurements directly. You can also use the mouse to move and size windows.</span></span>

<span data-ttu-id="dfe5d-132">このアクションは、すべてのウィンドウおよびビューで使用できます。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-132">You can use this action on any window, in any view.</span></span>

<span data-ttu-id="dfe5d-133">**ヒント**</span><span class="sxs-lookup"><span data-stu-id="dfe5d-133">**Tips**</span></span>

  - <span data-ttu-id="dfe5d-134">サイズを変更せずにウィンドウを移動するには、" **Right/右** " および " **Down/下** " 引数に値を入力し、" **Width/幅** " および " **Height/高さ** " 引数は空白のままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-134">To move a window without resizing it, enter values for the **Right** and **Down** arguments but leave the **Width** and **Height** arguments blank.</span></span>

  - <span data-ttu-id="dfe5d-135">移動せずにウィンドウのサイズを変更するには、" **Width/幅** " および " **Height/高さ** " 引数に値を入力し、" **Right/右** " および " **Down/下** " 引数は空白のままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-135">To resize a window without moving it, enter values for the **Width** and **Height** arguments but leave the **Right** and **Down** arguments blank.</span></span>

<span data-ttu-id="dfe5d-136">Visual Basic for Applications (VBA) モジュールで " **MoveAndSizeWindow/ウィンドウの移動とサイズ変更** " アクションを実行するには、 **DoCmd** オブジェクトの **MoveSize** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-136">To run the **MoveAndSizeWindow** action in a Visual Basic for Applications (VBA) module, use the **MoveSize** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="dfe5d-137">例</span><span class="sxs-lookup"><span data-stu-id="dfe5d-137">Example</span></span>

<span data-ttu-id="dfe5d-138">**マクロによるフォームの同期**</span><span class="sxs-lookup"><span data-stu-id="dfe5d-138">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="dfe5d-p104">次のマクロは、[仕入先] フォームの右下に [製品リスト] フォームを開き、現在の仕入先の商品を表示します。このマクロは、" **Echo/エコー** "、" **MessageBox/メッセージボックス** "、" **GoToControl/コントロールの移動** "、" **StopMacro/マクロの中止** "、" **OpenForm/フォームを開く** "、および " **MoveAndSizeWindow/ウィンドウの移動とサイズ変更** " の各アクションの使い方を示します。また、" **MessageBox/メッセージボックス** "、" **"GoToControl/コントロールの移動** "、" **StopMacro/マクロの中止** " の各アクションで条件式を使用する方法も示しています。このマクロを [仕入先] フォームの [商品の参照] ボタンに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-p104">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products. It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions. It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions. This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dfe5d-143">条件</span><span class="sxs-lookup"><span data-stu-id="dfe5d-143">Condition</span></span></p></th>
<th><p><span data-ttu-id="dfe5d-144">アクション</span><span class="sxs-lookup"><span data-stu-id="dfe5d-144">Action</span></span></p></th>
<th><p><span data-ttu-id="dfe5d-145">引数: 設定値</span><span class="sxs-lookup"><span data-stu-id="dfe5d-145">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="dfe5d-146">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="dfe5d-146">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="dfe5d-147"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="dfe5d-147"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="dfe5d-148"><strong>Echo On/エコーの設定</strong>: <strong>No/いいえ</strong></span><span class="sxs-lookup"><span data-stu-id="dfe5d-148"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="dfe5d-149">画面の更新は停止しますが、マクロは実行されています。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-149">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfe5d-150">IsNull([仕入先コード])</span><span class="sxs-lookup"><span data-stu-id="dfe5d-150">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="dfe5d-151"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="dfe5d-151"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="dfe5d-152"><strong>Message/メッセージ</strong>: 表示する商品を扱う仕入先のレコードに移動し、[商品の参照] ボタンを再度クリックします。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-152"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="dfe5d-153"><strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: 仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-153"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="dfe5d-154">[仕入先] フォームに現在の仕入先が存在しない場合、メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-154">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="dfe5d-155"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="dfe5d-155"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="dfe5d-156"><strong>Control Name/コントロール名</strong>: 会社名</span><span class="sxs-lookup"><span data-stu-id="dfe5d-156"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="dfe5d-157">フォーカスを [仕入先名] コントロールに移動します。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-157">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfe5d-158">...</span><span class="sxs-lookup"><span data-stu-id="dfe5d-158"></span></span></p></td>
<td><p><span data-ttu-id="dfe5d-159"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="dfe5d-159"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="dfe5d-160">マクロを停止します。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-160">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="dfe5d-161"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="dfe5d-161"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="dfe5d-162"><strong>フォーム名</strong>: 製品リストの<strong>表示</strong>: <strong>DatasheetFilter の名前</strong>: <strong>Where 条件式</strong>: [仕入先コード] = [Forms]![仕入先]![仕入先コード]<strong>データ モード</strong>:<strong>読み取り OnlyWindow モード</strong>:<strong>標準</strong></span><span class="sxs-lookup"><span data-stu-id="dfe5d-162"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="dfe5d-163">[製品リスト] フォームを開き、現在の仕入先の製品を表示します。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-163">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="dfe5d-164"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="dfe5d-164"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="dfe5d-165"><strong>右</strong>: 0.7799&quot; <strong>ダウン</strong>: 1.8&quot;</span><span class="sxs-lookup"><span data-stu-id="dfe5d-165"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="dfe5d-166">[製品リスト] を [仕入先] フォームの右下に配置します。</span><span class="sxs-lookup"><span data-stu-id="dfe5d-166">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

