---
title: Requery マクロ アクション
TOCTitle: Requery macro action
ms:assetid: 6dbdcae5-81b6-9925-4cad-64b178c23060
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195544(v=office.15)
ms:contentKeyID: 48545499
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm30402
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 8b90af8d1cda073ffa37022bb5db5e8cf8e3b978
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306707"
---
# <a name="requery-macro-action"></a>Requery マクロ アクション

**適用先:** Access 2013、Office 2013

You can use the **Requery** action to update the data in a specified control on the active object by requerying the source of the control. If no control is specified, this action requeries the source of the object itself. Use this action to ensure that the active object or one of its controls displays the most current data.

## <a name="setting"></a>Setting

"Requery/再クエリ" アクションの引数は次のとおりです。

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
<td><p><strong>Control Name/コントロール名</strong></p></td>
<td><p>更新するコントロールの名前を指定します。 [マクロビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>コントロール名</strong>] ボックスに、コントロール名を入力します。 完全修飾識別子ではなく、コントロールの名前のみを使用する必要があります ( <strong>Forms</strong>! など)。<em>formname</em>!<em>controlname</em>) アクティブオブジェクトのソースを再クエリするには、この引数を指定しないでください。 アクティブオブジェクトがデータシートまたはクエリの結果セットの場合は、この引数を指定しないでください。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

"Requery/再クエリ" アクションは、次のいずれかの処理を行います。

- 指定したコントロールやオブジェクトの基になるクエリの再実行。

- コントロールやオブジェクトの基になるテーブルで追加、変更、または削除されたレコードの反映。

> [!NOTE]
> The **Requery** action does not affect the position of the record pointer.

クエリやテーブルに基づくコントロールには次のようなものがあります。

- リスト ボックスとコンボ ボックス。

- サブフォーム コントロール。

- グラフなどの OLE オブジェクト。

- **DSum** などの定義域集計関数が含まれるコントロール。

指定されたコントロールがクエリまたはテーブルに基づいていない場合、このアクションによってコントロールの再計算が実行されます。

If you leave the **Control Name** argument blank, the **Requery** action has the same effect as pressing SHIFT+F9 when the object has the focus. If a subform control has the focus, this action requeries only the source of the subform (just as pressing SHIFT+F9 does).

> [!NOTE]
> The **Requery** action requeries the source of the control or object. In contrast, the **RepaintObject** action repaints controls in the specified object but doesn't requery the database or display new records. The **ShowAllRecords** action not only requeries the active object, but it also removes any applied filters, which the **Requery** action doesn't do.

If you want to requery a control that isn't on the active object, you must use the **Requery** method in a Visual Basic for Applications (VBA) module, not the **Requery** action or its corresponding **Requery** method of the **DoCmd** object. The **Requery** method in VBA is faster than the **Requery** action or the **DoCmd.Requery** method. In addition, when you use the **Requery** action or the **DoCmd.Requery** method, Microsoft Access closes the query and reloads it from the database, but when you use the **Requery** method, Access reruns the query without closing and reloading it. ActiveX データオブジェクト (ADO) **requery**メソッドは、Access **requery**メソッドと同じように動作します。

