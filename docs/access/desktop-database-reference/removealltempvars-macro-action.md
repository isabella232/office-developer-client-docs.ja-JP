---
title: RemoveAllTempVars マクロ アクション
TOCTitle: RemoveAllTempVars macro action
ms:assetid: 409fd836-4a53-cefd-4264-8cee0fa8ac52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192877(v=office.15)
ms:contentKeyID: 48544430
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117413
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: eade809a6e3982dc0dc4cf94ae382af72e8f454e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306798"
---
# <a name="removealltempvars-macro-action"></a>RemoveAllTempVars マクロ アクション


**適用先:** Access 2013、Office 2013


"RemoveAllTempVars/すべての一時変数の削除" アクションは、"SetTempVar/一時変数の設定" アクションを使用して作成したすべての一時変数を削除するために使用します。

## <a name="setting"></a>Setting

"RemoveAllTempVars/すべての一時変数の削除" アクションには、引数はありません。

## <a name="remarks"></a>注釈

  - 一度に定義しておくことのできる一時変数は、最大 255 個です。一時変数は、削除しなければ、データベースまたはプロジェクトを閉じるまでメモリに残ったままとなります。不要となった一時変数は削除することをお勧めします。

  - データベースまたはプロジェクトを閉じると、すべての一時変数が自動的に削除されます。

  - To remove a single temporary variable, use the **RemoveTempVar** action and set its argument to the name of the temporary variable you want to remove.

  - To run the **RemoveAllTempVars** action in a VBA module, use the **RemoveAll** method of the **TempVars** object.

## <a name="example"></a>例

The following macro demonstrates how to create a temporary variable, use it in a condition and a message box, and then remove the temporary variable by using the **RemoveAllTempVars** action.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>条件</p></th>
<th><p>アクション</p></th>
<th><p>引数</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>SetTempVar</strong></p></td>
<td><p><strong>名前</strong>: MyVar<strong>Expression</strong>: InputBox (&quot;0 以外の数値を入力し&quot;ます。)</p></td>
</tr>
<tr class="even">
<td><p>[TempVars]![MyVar]&lt;&gt;0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>メッセージ</strong>: =&quot;入力&quot; &amp;した [TempVars]!MyVar&amp; &quot;.&quot;<strong>警告音</strong>: <strong>yestype</strong>:<strong>情報</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>RemoveAllTempVars</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

