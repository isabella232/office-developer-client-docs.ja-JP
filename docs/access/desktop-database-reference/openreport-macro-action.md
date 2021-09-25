---
title: OpenReport マクロ アクション
TOCTitle: OpenReport macro action
ms:assetid: cd35faf2-190d-ac48-cf59-81c1599eb764
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834462(v=office.15)
ms:contentKeyID: 48547758
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm188079
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: c25362594ca22a14663669847f0c20fd981b067d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552725"
---
# <a name="openreport-macro-action"></a>OpenReport マクロ アクション

**適用先:** Access 2013、Office 2013

You can use the **OpenReport** action to open a report in Design view or Print Preview, or to send the report directly to the printer. You can also restrict the records that are printed in the report.

## <a name="setting"></a>設定

"OpenReport/レポートを開く" アクションの引数は次のとおりです。

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
<td><p>レポート名</p></td>
<td><p>開くレポートの名前を指定します。[ <strong>マクロ ビルダー</strong>] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>レポート名</strong>] ボックスには、カレント データベース内のビューがすべて表示されます。この引数は省略できません。ライブラリ データベースで OpenReport アクションが定義されているマクロを実行すると、この名前のレポートが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。  </p></td>
</tr>
<tr class="even">
<td><p>表示</p></td>
<td><p>レポートを開くときのビューを指定します。[ <strong>ビュー</strong>] ボックスで [ <strong>印刷</strong>] (レポートをすぐに印刷する場合)、[ <strong>デザイン</strong>]、または [ <strong>印刷プレビュー</strong>] をクリックします。既定値は [ <strong>印刷</strong>] です。  </p></td>
</tr>
<tr class="odd">
<td><p>Filter Name/フィルター名</p></td>
<td><p>A filter that restricts the report's records. You can enter the name of either an existing query or a filter that was saved as a query. However, the query must include all the fields in the report you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.  </p></td>
</tr>
<tr class="even">
<td><p>Where Condition/Where 条件式</p></td>
<td><p>A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the report's underlying table or query. 引数 Filter Name でフィルターを選択した場合、Access はフィルターの結果にこの WHERE 句を適用します。 レポートを開き、そのレコードをフォーム上のコントロールの値で指定されたレコードに制限するには、次の式を使用します。<br />
<strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on form</em><strong>]</strong><br />
fieldname <em>を</em> 、開くレポートの基になるテーブルまたはクエリ内のフィールドの名前に置き換える。 フォーム <em>の formname</em> と <em>controlname</em> をフォームの名前と、レポート内のレコードに一致する値を含むフォーム上のコントロールを置き換える。</p>
<p><b>注</b>: 引数 Where Condition の最大長は 255 文字です。 If you need to enter a more complex SQL WHERE clause longer than this, use the <b>OpenReport</b> method of the <b>DoCmd</b> object in a Visual Basic for Applications (VBA) module instead. You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</p>
</td>
</tr>
<tr class="odd">
<td><p>Window Mode/ウィンドウ モード</p></td>
<td><p>レポートを開くときのモードを指定します。[ <strong>ウィンドウ モード</strong>] ボックスで、[ <strong>標準</strong>]、[ <strong>非表示</strong>]、[ <strong>アイコン</strong>]、または [ <strong>ダイアログ</strong>] をクリックします。既定値は [ <strong>標準</strong>] です。  </p>
<p><b>注</b>: タブ付きドキュメントを使用する場合、一部のウィンドウ モードの引数設定は適用されません。 ウィンドウを重ねて表示するように切り替えるには、次の操作を行います。
<ol>
<li><p>[<strong>オプション</strong>] をクリックします。</p></li>
<li><p>[ <strong>Access のオプション</strong>] ダイアログ ボックスの [ <strong>カレント データベース</strong>] をクリックします。</p></li>
<li><p>[ <strong>アプリケーション オプション</strong>] の [ <strong>ドキュメント ウィンドウ オプション</strong>] で [ <strong>ウィンドウを重ねて表示する</strong>] をクリックします。</p></li>
<li><p>[ <strong>OK</strong>] をクリックし、データベースを閉じて再度開きます。</p></li>
</ol>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

" **View/ビュー** " 引数で [ **印刷**] を選択すると、現在のプリンター設定を使用してすぐにレポートが印刷されますが、[ **印刷**] ダイアログ ボックスは表示されません。また、" **OpenReport/レポートを開く** " アクションを使用すると、レポートを開いて設定した後に、 PrintOut アクションを使用してレポートを印刷することもできます。たとえば、印刷前に、レポートを修正したり、" **PrintOut/印刷** " アクションを使用してプリンター設定を変更することができます。

The filter and WHERE condition you apply become the setting of the report's **Filter** property.

The **OpenReport** action is similar to double-clicking the report in the Navigation Pane, or right-clicking the report in the Navigation Pane and selecting a view or the **Print** command.

> [!TIP] 
> - 複数のデータ セットに対して、類似したレポートを印刷するには、フィルターまたは WHERE 句を使用してレポートに印刷するレコードを制限します。 次に、マクロを編集して別のフィルターを適用するか、Where Condition 引数を変更します。
> 
> - レポートをナビゲーション ウィンドウで選択し、マクロのアクション行にドラッグすると、レポートをレポート ビューで開く "OpenReport/レポートを開く" アクションが自動的に作成されます。

## <a name="example"></a>例

次の例では、OpenReport アクションを使用して、レポートを開くときにフィルターを適用するパラメーターを渡す方法を示します。[**cboAuthors**] コンボ ボックスで選択されたアイテムが SelectedAuthor パラメーターに渡されることで、指定された作成者のレポートが **rptChapters** レポートに表示されます。

**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。

```vb
    OpenReport
        Report Name rptChapters
        View Report
        Filter Name
        Where Condition
        Window Mode Normal
    
    Parameters
        SelectedAuthor =[cboAuthor]
```
