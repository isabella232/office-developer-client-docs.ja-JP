---
title: SetOrderBy マクロ アクション
TOCTitle: SetOrderBy macro action
ms:assetid: 78f65ce9-b56f-f476-3bd6-f3307bc22a08
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196152(v=office.15)
ms:contentKeyID: 48545765
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98639
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b820b984972b4de7592f159884ebce3f3a59dec8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923316"
---
# <a name="setorderby-macro-action"></a>SetOrderBy マクロ アクション


**適用されます**Access 2013、Office 2013。

**SetOrderBy** アクションを使用し、フォーム、レポート、テーブル、またはクエリ結果のレコードを並べ替えることができます。

## <a name="setting"></a>設定

**SetOrderBy** アクションの引数は次のとおりです。

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
<td><p><strong>Order By/並び替え</strong></p></td>
<td><p>レコードを並べ替えるフィールド (複数可) の名前を含む文字列の式です。必要に応じて ASC キーワードまたは DESC キーワードを含めることもできます</p></td>
</tr>
<tr class="even">
<td><p><strong>Control Name/コントロール名</strong></p></td>
<td><p>アクティブ オブジェクトがフォームまたはレポートである場合、並べ替えるサブフォームまたはサブレポートに対応するコントロール名を示します。この引数を指定しないと、アクティブ オブジェクトがフォームまたはレポートである場合は、親フォームまたは親レポートが並べ替えられます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>備考

このマクロ アクションを実行すると、アクティブであり、かつフォーカスがあるテーブル、フォーム、レポート、またはデータシート (クエリ結果) に対して並べ替えが適用されます。

"Order By/並べ替え" 引数とは、レコードを並べ替えるフィールドの名前を指します。複数のフィールド名を指定する場合はコンマ (,) で区切ります。アクティブ オブジェクトの **OrderBy** プロパティを使用すると、順序値を保存し、後で適用できます。OrderBy プロパティの値は、そのプロパティを設定したオブジェクトに保存されます。オブジェクトを開くと自動的に開きますが、自動的には適用されません。

1 つ以上のフィールド名を入力し、"Order By/並べ替え" 引数を設定してマクロを実行すると、レコードは既定では昇順に並べ替えられます。

レコードを降順に並べ替えるには、"Order By/並べ替え" 引数式の最後に「DESC」と入力します。たとえば、連絡先の降順に顧客レコードを並べ替えるには、"Order By/並べ替え" 引数を "ContactName DESC" に設定します。名前を姓の降順および名の昇順に並べ替えるには、"Order By/並べ替え" 引数を "LastName DESC, FirstName ASC" に設定します。

