---
title: MoveAndSizeWindow マクロ アクション
TOCTitle: MoveAndSizeWindow macro action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c1b127995a2f9a0af7da80e9df862259b570870e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288807"
---
# <a name="moveandsizewindow-macro-action"></a>MoveAndSizeWindow マクロ アクション

**適用先:** Access 2013、Office 2013

タブ付きドキュメントではなくウィンドウを重ねて使用するようにドキュメント ウィンドウ オプションを設定すると、" **MoveAndSizeWindow/ウィンドウの移動とサイズ変更** " アクションを使用して、アクティブ ウィンドウの移動またはサイズ変更を行うことができます。ドキュメント ウィンドウ オプションを設定する方法については、「注釈」セクションを参照してください。

## <a name="setting"></a>Setting

"**MoveAndSizeWindow/ウィンドウの移動とサイズ変更**" アクションの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>アクションの引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Right</strong></p></td>
<td><p>移動またはサイズ変更するウィンドウの左上隅の水平位置を、そのウィンドウを表示するウィンドウの左端からの距離で指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>右</strong>] ボックスに、位置を入力します。</p></td>
</tr>
<tr class="even">
<td><p><strong>Down</strong></p></td>
<td><p>移動またはサイズ変更するウィンドウの左上隅の垂直位置を、そのウィンドウを表示するウィンドウの上端からの距離で指定します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Width</strong></p></td>
<td><p>ウィンドウの幅を指定します。</p></td>
</tr>
<tr class="even">
<td><p><strong>Height</strong></p></td>
<td><p>ウィンドウの高さを指定します。</p></td>
</tr>
</tbody>
</table>


この引数を指定しないと、ウィンドウの現在の設定が使用されます。

少なくとも 1 つの引数に対して値を入力する必要があります。

> [!NOTE]
> 各測定値はインチまたはセンチメートル単位で指定します。どちらの単位を使用するかは、Windows コントロール パネルの地域の設定によって決まります。

## <a name="remarks"></a>注釈

タブ付きドキュメントではなくウィンドウを重ねて使用するようにアプリケーションを設定するには、次の手順を実行します。

1.  [**オプション**] をクリックします。

2.  [ **カレント データベース**] をクリックします。

3.  [ **アプリケーション オプション**] の [ **ドキュメント ウィンドウ オプション**] で [ **ウィンドウを重ねて表示する**] をクリックします。

4.  [ **OK**] をクリックし、データベースを閉じて再度開きます。

このアクションは、ウィンドウの [ **コントロール**] メニューの [ **移動**] または [ **サイズ**] をクリックした場合の操作と似ています。メニュー コマンドでは、キーボードの方向キーを使用してウィンドウの移動またはサイズ変更を行います。" **MoveAndSizeWindow/ウィンドウの移動とサイズ変更** " アクションの場合、位置とサイズの値を直接入力します。マウスを使用して、ウィンドウの移動およびサイズ変更を行うこともできます。

このアクションは、すべてのウィンドウおよびビューで使用できます。

> [!TIP]
> - サイズを変更せずにウィンドウを移動するには、" **Right/右** " および " **Down/下** " 引数に値を入力し、" **Width/幅** " および " **Height/高さ** " 引数は空白のままにしておきます。
> - 移動せずにウィンドウのサイズを変更するには、" **Width/幅** " および " **Height/高さ** " 引数に値を入力し、" **Right/右** " および " **Down/下** " 引数は空白のままにしておきます。

Visual Basic for Applications (VBA) モジュールで "**MoveAndSizeWindow/ウィンドウの移動とサイズ変更**" アクションを実行するには、**DoCmd** オブジェクトの **MoveSize** メソッドを使用します。

## <a name="example"></a>例

**マクロによるフォームの同期**

次のマクロは、[仕入先] フォームの右下に [製品リスト] フォームを開き、現在の仕入先の商品を表示します。このマクロは、" **Echo/エコー** "、" **MessageBox/メッセージボックス** "、" **GoToControl/コントロールの移動** "、" **StopMacro/マクロの中止** "、" **OpenForm/フォームを開く** "、および " **MoveAndSizeWindow/ウィンドウの移動とサイズ変更** " の各アクションの使い方を示します。また、" **MessageBox/メッセージボックス** "、" **"GoToControl/コントロールの移動** "、" **StopMacro/マクロの中止** " の各アクションで条件式を使用する方法も示しています。このマクロを [仕入先] フォームの [商品の参照] ボタンに割り当てる必要があります。

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>条件</p></th>
<th><p>アクション</p></th>
<th><p>引数: 設定値</p></th>
<th><p>Comment</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Echo On/エコーの設定</strong>: <strong>No/いいえ</strong></p></td>
<td><p>画面の更新は停止しますが、マクロは実行されています。</p></td>
</tr>
<tr class="even">
<td><p>IsNull([仕入先コード])</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message/メッセージ</strong>: 表示する商品を扱う仕入先のレコードに移動し、[商品の参照] ボタンを再度クリックします。 <strong>Beep</strong>: <strong>yestype</strong>: <strong>none title</strong>: 仕入先の選択</p></td>
<td><p>[仕入先] フォームに現在の仕入先が存在しない場合、メッセージを表示します。</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Control Name/コントロール名</strong>: 会社名</p></td>
<td><p>フォーカスを [仕入先名] コントロールに移動します。</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>StopMacro</strong></p></td>
<td><p></p></td>
<td><p>マクロを停止します。</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>フォーム名</strong>: 製品リスト<strong>ビュー</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![仕入先]!SupplierID<strong>データモード</strong>:<strong>読み取りのみウィンドウモード</strong>:<strong>標準</strong></p></td>
<td><p>[製品リスト] フォームを開き、現在の仕入先の製品を表示します。</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>MoveAndSizeWindow</strong></p></td>
<td><p><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</p></td>
<td><p>[製品リスト] を [仕入先] フォームの右下に配置します。</p></td>
</tr>
</tbody>
</table>

