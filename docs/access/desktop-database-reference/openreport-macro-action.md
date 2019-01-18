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
localization_priority: Normal
ms.openlocfilehash: cff57a185d226328792bef79072dfc46c6134f98
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707242"
---
# <a name="openreport-macro-action"></a>OpenReport マクロ アクション

**適用されます**Access 2013、Office 2013。

**OpenReport**アクションを使用するには、デザイン ビューまたは印刷プレビューでレポートを開くか、プリンターに直接レポートを送信します。 また、レポートに印刷するレコードを制限することもできます。

## <a name="setting"></a>設定値

**OpenReport**アクションには、次の引数があります。

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
<td><p>Report Name/レポート名</p></td>
<td><p>開くレポートの名前を指定します。[ <strong>マクロ ビルダー</strong>] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>レポート名</strong>] ボックスには、カレント データベース内のビューがすべて表示されます。この引数は省略できません。ライブラリ データベースで OpenReport アクションが定義されているマクロを実行すると、この名前のレポートが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。  </p></td>
</tr>
<tr class="even">
<td><p>View</p></td>
<td><p>レポートを開くときのビューを指定します。[ <strong>ビュー</strong>] ボックスで [ <strong>印刷</strong>] (レポートをすぐに印刷する場合)、[ <strong>デザイン</strong>]、または [ <strong>印刷プレビュー</strong>] をクリックします。既定値は [ <strong>印刷</strong>] です。  </p></td>
</tr>
<tr class="odd">
<td><p>Filter Name</p></td>
<td><p>レポートのレコードを制限するフィルターを使用します。 既存のクエリまたはクエリとして保存されているフィルターのいずれかの名前を入力することができます。 ただし、クエリでは、開こうとしているか、<strong>含まれる</strong>プロパティを [<strong>はい]</strong>が設定されてレポートにすべてのフィールドを含める必要があります。</p></td>
</tr>
<tr class="even">
<td><p>Where Condition</p></td>
<td><p>有効な SQL WHERE 句 (語を除く、)、またはレポートからレコードを選択するときに使用する式には、テーブルまたはクエリの基になります。 フィルター名の引数を指定してフィルターを選択する場合は、フィルターの結果に次の WHERE 句が適用されます。 レポートを開いて、フォームのコントロールの値を使ってレコードを制限するには、次の構文を使用します。<br /><strong> 
<strong>[</strong><em>フィールド名</em>] = フォームです。[</strong><em>フォーム</em><strong>]![</strong><em>名フォームに置き換えます</em><strong>]</strong><br />
<em>フィールド名</em>を基になるテーブルまたはクエリを開くには、レポートのフィールドの名前に置き換えます。 <em>フォーム名</em>と<em>名フォームに置き換えます</em>をフォームと一致するようにレポート内のレコードの値が含まれるフォーム上のコントロールの名前に置き換えます。</p>
<p><b>注</b>: 条件式の最大長は 255 文字、です。 複雑な SQL WHERE 句よりも長い時間を入力する場合は、 <b>DoCmd</b>オブジェクトの<b>OpenReport</b>メソッドで Visual Basic for Applications (VBA) モジュールの代わりに使用します。 VBA では、SQL 句のステートメントの最大 32,768 文字を入力できます。</p>
</td>
</tr>
<tr class="odd">
<td><p>Window Mode</p></td>
<td><p>レポートを開くときのモードを指定します。[ <strong>ウィンドウ モード</strong>] ボックスで、[ <strong>標準</strong>]、[ <strong>非表示</strong>]、[ <strong>アイコン</strong>]、または [ <strong>ダイアログ</strong>] をクリックします。既定値は [ <strong>標準</strong>] です。  </p>
<p><b>注</b>: タブ付きドキュメントを使用すると、引数のいくつかのウィンドウ モードの設定は適用されません。 重ねて表示されるウィンドウに切り替えるには
<ol>
<li><p>[ <strong>オプション</strong>] をクリックします。</p></li>
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

フィルターおよび WHERE 条件式を指定するレポートの**フィルター**のプロパティの設定になります。

**OpenReport**アクションは、ナビゲーション ウィンドウでレポートをダブルクリックすると、ナビゲーション ウィンドウでレポートを右クリックしてやビューまたは **[印刷**] コマンドを選択することに似ています。

> [!TIP] 
> - 複数のデータ セットに対して、類似したレポートを印刷するには、フィルターまたは WHERE 句を使用してレポートに印刷するレコードを制限します。 別のフィルターを適用または条件式を変更するマクロを編集します。
> 
> - ナビゲーション ウィンドウからマクロのアクション行にレポートをドラッグできます。 これにより、レポート ビューでレポートを開く**OpenReport**アクションが自動的に作成されます。

## <a name="example"></a>例

次の例では、 OpenReport アクションを使用して、レポートを開くときにフィルターを適用するパラメーターを渡す方法を示します。 **RptChapters**レポートは、SelectedAuthor パラメーターを**cboAuthors**のコンボ ボックスで選択したアイテムを渡すことによって、指定した作成者のレコードを表示します。

**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。

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
