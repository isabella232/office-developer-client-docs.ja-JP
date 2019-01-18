---
title: GoToRecord マクロ アクション
TOCTitle: GoToRecord macro action
ms:assetid: 76f936de-739b-63be-9b28-5b0e111408e6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196037(v=office.15)
ms:contentKeyID: 48545712
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm58124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7534ae84b57d14450009865ea330a4c54d4cfb44
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708481"
---
# <a name="gotorecord-macro-action"></a>GoToRecord マクロ アクション


**適用されます**Access 2013、Office 2013。

**GoToRecord**アクションを使用するには、開いているテーブル、フォーム、またはクエリの結果セットで、指定されたレコードをカレント レコードにします。

## <a name="setting"></a>設定値

" **GoToRecord/レコードの移動** " アクションの引数は次のとおりです。

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
<td><p><strong>Object Type/オブジェクトの種類</strong></p></td>
<td><p>カレント レコードにするレコードが含まれているオブジェクトの種類を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>オブジェクトの種類</strong>] ボックスで、[<strong>テーブル</strong>]、[<strong>クエリ</strong>]、[<strong>フォーム</strong>]、[<strong>サーバー ビュー</strong>]、[<strong>ストアド プロシージャ</strong>]、[<strong>関数</strong>] のいずれかをクリックします。この引数を指定しない場合は、アクティブ オブジェクトが選択されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>オブジェクト名</strong></p></td>
<td><p>現在のレコードにレコードを格納するオブジェクトの名前。 <strong>オブジェクト名</strong>] ボックスでは、<strong>オブジェクトの型</strong>引数で指定した型の現在のデータベース内のすべてのオブジェクトを示しています。 <strong>オブジェクトの型</strong>引数を空白のままにする場合は、この引数を指定しないも。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Record</strong></p></td>
<td><p>カレント レコードにするレコードを指定します。[<strong>レコード</strong>] ボックスで、[<strong>前のレコード</strong>]、[<strong>次のレコード</strong>]、[<strong>先頭のレコード</strong>]、[<strong>最後のレコード</strong>]、[<strong>移動先指定</strong>]、[<strong>新しいレコード</strong>] のいずれかをクリックします。既定値は [<strong>次のレコード</strong>] です。</p></td>
</tr>
<tr class="even">
<td><p><strong>Offset</strong></p></td>
<td><p>整数型または整数値に評価される式です。 式の前に等号 (=) (<strong>=</strong>)。 この引数は、カレント レコードのレコードを指定します。 2 つの方法では、<strong>この引数</strong>を使用できます。</p>
<ul>
<li><p><strong>Record</strong>引数は、<strong>次</strong>または<strong>前</strong>に、Microsoft Office Access 2007 は、前方または後方は、<strong>この引数</strong>で指定されたレコードの数を移動します。</p></li>
<li><p><strong>レコード</strong>の引数が<strong>移動先</strong>にある場合は、<strong>オフセット</strong>の引数に等しい数のレコードに移動します。 レコード番号は、ウィンドウの下部にあるレコード番号ボックスに表示されます。</p>
<p><strong>注</strong>:<strong>最初</strong>、<strong>最後</strong>、または<strong>新しい</strong><strong>レコード</strong>の引数の設定を使用する場合<strong>、この引数</strong>は無視されます。 大きすぎて<strong>オフセット</strong>の引数を入力する場合は、エラー メッセージが表示されます。 <strong>オフセット</strong>の引数に負の値を入力できません。</p></li>
<li><p><strong>Record</strong>引数は、<strong>次</strong>または<strong>前</strong>に、Microsoft Office Access 2007 は、前方または後方は、<strong>この引数</strong>で指定されたレコードの数を移動します。</p></li>
<li><p><strong>レコード</strong>の引数が<strong>移動先</strong>にある場合は、<strong>オフセット</strong>の引数に等しい数のレコードに移動します。 レコード番号は、ウィンドウの下部にあるレコード番号ボックスに表示されます。</p></li>
</ul>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

レコードの特定のコントロールにフォーカスがある場合、このアクションを実行しても、新しいフォームの同じコントロールにフォーカスがとどまります。

**** **新規**設定を使用すると、フォームまたはテーブルの末尾に空白のレコードに移動して新しいデータを入力することができます。

このアクションでは、[**ホーム**] タブの [**検索**] ボタンの下の矢印をクリックし、[移動]**を**クリックすると似ています。 **最初**、**最後**、**次****前**、および、[**移動**] コマンドのサブコマンドを**新しいレコード**に、**最初**、**最後**、**次****前**、選択したオブジェクトに同じ効果があります。**** **新規**設定します。 ウィンドウの下部にあるナビゲーション ボタンを使用してレコードに移動することもできます。

**GoToRecord**アクションを使用すると、**オブジェクト型**および**オブジェクト名**の引数を非表示のフォームを指定する場合、非表示のフォームの現在のレコードにレコードを作成します。

**GoToRecord**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**GoToRecord**メソッドを使用します。

