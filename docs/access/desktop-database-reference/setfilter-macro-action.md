---
title: "\"SetFilter/フィルターの実行\" マクロ アクション"
TOCTitle: SetFilter Macro Action
ms:assetid: dee699e2-0840-1612-23ce-199ef8d30566
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835438(v=office.15)
ms:contentKeyID: 48548203
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm122943
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4fe2bceb53b835d4c8adab1a1550185c3a7a122a
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606396"
---
# <a name="setfilter-macro-action"></a>"SetFilter/フィルターの実行" マクロ アクション

**適用されます**Access 2013 |。Office 2013

**SetFilter**アクションを使用すると、アクティブなデータシート、フォーム、レポート、またはテーブル内のレコードにフィルターを適用します。

## <a name="setting"></a>設定

**SetFilter**アクションには、次の引数があります。

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
<<<<<<< ヘッド
<td><p>指定した場合は、クエリの名前、またはクエリとして保存されているフィルターの名前です。 クライアント データベースでこの引数または WhereCondition 引数が必要です。 Web データベースでは、この引数は使用できません。</p></td>
</tr>
<tr class="even">
<td><p>Where Condition</p></td>
<td><p>指定した場合は、データシート、フォーム、レポート、またはテーブルでレコードを制限する SQL WHERE 句を示します。Web データベースの場合、この引数は必須です。</p></td>
=======
<td><p>指定した場合は、クエリの名前、またはクエリとして保存されているフィルターの名前です。 クライアント データベースでこの引数または WhereCondition 引数が必要です。 Web データベースでこの引数は使用できません。</p></td>
</tr>
<tr class="even">
<td><p>Where Condition</p></td>
<td><p>指定した場合は、データシート、フォーム、レポート、またはテーブルでレコードを制限する SQL WHERE 句を示します。 Web データベースでは、この引数が必要です。</p></td>
>>>>>>>マスター
</tr>
<tr class="odd">
<td><p>コントロール名</p></td>
<td><p>指定した場合は、フィルター処理するサブフォームまたはサブレポートに対応するコントロールの名前を示します。指定しない場合は、現在のオブジェクトがフィルター処理されます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>備考

Web データベースでは、"Where Condition/Where 条件式" 引数の先頭に (=) を付けることはできません。

このアクションを実行すると、アクティブであり、かつフォーカスがあるテーブル、フォーム、レポート、またはデータシート (クエリ結果など) に対してフィルターが適用されます。

アクティブなオブジェクトの **Filter** プロパティを使用すると、"WhereCondition/Where 条件式" 引数を保存して、後で適用できます。フィルターは、それを作成したオブジェクトに保存されます。そのオブジェクトが開くと自動的に読み込まれますが、自動的に適用されることはありません。

クライアントでは、オブジェクトが開かれると、自動的にフィルターを適用するのには、データベースは、 **FilterOnLoad**プロパティを True に設定します。

Web データベースでは、オブジェクトを開いたときに自動的にフィルターを適用するに**SetFilter**アクションをマクロに追加でオブジェクトの**OnLoad**イベントにマクロを追加します。

## <a name="example"></a>例

次の例では、 SetFilter アクションを使用して、マクロが定義されているフォームにフィルターを適用する方法を示します。

**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。

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
