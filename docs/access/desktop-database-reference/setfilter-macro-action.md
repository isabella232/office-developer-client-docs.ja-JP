---
title: SetFilter マクロ アクション
TOCTitle: SetFilter macro action
ms:assetid: dee699e2-0840-1612-23ce-199ef8d30566
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835438(v=office.15)
ms:contentKeyID: 48548203
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm122943
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: d21690a0444fcae2d45596935969d63ed69fff43
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611540"
---
# <a name="setfilter-macro-action"></a>SetFilter マクロ アクション

**適用先**: Access 2013、Office 2013

"SetFilter/フィルターの実行" アクションを使用すると、アクティブ データシート、アクティブ フォーム、アクティブ レポート、またはアクティブ テーブルのレコードに対してフィルターを適用できます。

## <a name="setting"></a>設定

"SetFilter/フィルターの実行" アクションの引数は次のとおりです。

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
<td><p>Filter Name/フィルター名</p></td>
<td><p>指定した場合は、クエリの名前、またはクエリとして保存されているフィルターの名前。 この引数または WhereCondition 引数は、クライアント データベースで必要です。 Web データベースでは、この引数は使用できません。</p></td>
</tr>
<tr class="even">
<td><p>Where Condition/Where 条件式</p></td>
<td><p>指定した場合は、データシート、フォーム、レポート、またはテーブルのレコードを制限する SQL WHERE 句。 Web データベースでは、この引数が必要です。</p></td>
</tr>
<tr class="odd">
<td><p>コントロール名</p></td>
<td><p>指定した場合は、フィルター処理するサブフォームまたはサブレポートに対応するコントロールの名前を示します。指定しない場合は、現在のオブジェクトがフィルター処理されます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

Web データベースでは、Where Condition 引数の先頭に (=) を付けることはできません。

このアクションを実行すると、アクティブであり、かつフォーカスがあるテーブル、フォーム、レポート、またはデータシート (クエリ結果など) に対してフィルターが適用されます。

アクティブなオブジェクトの **Filter** プロパティを使用すると、"WhereCondition/Where 条件式" 引数を保存して、後で適用できます。フィルターは、それを作成したオブジェクトに保存されます。そのオブジェクトが開くと自動的に読み込まれますが、自動的に適用されることはありません。

クライアント データベースで、オブジェクトを開いたときにフィルターを自動的に適用するには **、FilterOnLoad** プロパティを True に設定します。

Web データベースで、オブジェクトを開いたときにフィルターを自動的に適用するには、マクロに "SetFilter/フィルターの実行" アクションを追加し、このマクロをオブジェクトの OnLoad イベントに追加します。

## <a name="example"></a>例

次の例では、SetFilter アクションを使用して、マクロが定義されているフォームにフィルターを適用する方法を示します。

**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    SetFilter
        Filter Name
        Where Condtion =[display_name] Like "*cheese*"
        Control Name
```
