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
ms.localizationpriority: medium
ms.openlocfilehash: f2c98a02702409962f20289128b18e53835e071d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617497"
---
# <a name="removealltempvars-macro-action"></a>RemoveAllTempVars マクロ アクション


**適用先**: Access 2013、Office 2013


"RemoveAllTempVars/すべての一時変数の削除" アクションは、"SetTempVar/一時変数の設定" アクションを使用して作成したすべての一時変数を削除するために使用します。

## <a name="setting"></a>設定

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
<td><p><strong>名前</strong>: MyVar<strong>式</strong>: InputBox( &quot; 0 以外の数値を入力します。 &quot;</p></td>
</tr>
<tr class="even">
<td><p>[TempVars]![MyVar]&lt;&gt;0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>メッセージ</strong>: = &quot; &quot; &amp; [TempVars]と入力しました![MyVar] &amp; &quot; . &quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>RemoveAllTempVars</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

