---
title: SetLocalVar マクロ アクション
TOCTitle: SetLocalVar macro action
ms:assetid: 8a6af395-0f76-72e2-37f3-2cff22a38b3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197097(v=office.15)
ms:contentKeyID: 48546190
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm176660
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 091b9717b9a2e35cfc8d0c8555e28570628065ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314589"
---
# <a name="setlocalvar-macro-action"></a>SetLocalVar マクロ アクション

**適用先:** Access 2013、Office 2013

"SetLocalVar/ローカル変数の設定" アクションは、一時変数を作成し、それを特定の値に設定します。

## <a name="setting"></a>設定

"SetLocalVar/ローカル変数の設定" アクションの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>引数</p></th>
<th><p>必須</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>名前</strong></p></td>
<td><p>はい</p></td>
<td><p>変数の名前を指定する文字列。</p></td>
</tr>
<tr class="even">
<td><p><strong>Expression</strong></p></td>
<td><p>はい</p></td>
<td><p>An expression that will be used to set the value for this temporary variable. Do not precede the expression with the equal sign (=). You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.  </p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>注釈

Variables created by the **SetLocalVar** action can be used only in the macro in which they are defined. Use the **[SetTempVar](settempvar-macro-action.md)** action to define a variable that can be used in another macro, in an event procedure, or on a form or report.

一時変数を作成すると、それを式で参照できます。たとえば、TotalAmount という一時変数を作成した場合、次の構文でこの変数をテキスト ボックスのコントロール ソースとして使用できます。

`=[LocalVars]![TotalAmount]`

> [!NOTE]
> データ マクロでは、変数を参照するために LocalVars コレクションを使用する必要はありません。 たとえば、データ マクロで TotalAmount という一時変数を作成した場合、次の構文でこの変数をテキスト ボックスのコントロール ソースとして使用できます: `=[TotalAmount]`。

