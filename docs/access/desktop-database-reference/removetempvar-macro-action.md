---
title: RemoveTempVar マクロ アクション
TOCTitle: RemoveTempVar macro action
ms:assetid: 7bcc5010-3e30-ecef-2c5d-a35e73c8e325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196352(v=office.15)
ms:contentKeyID: 48545822
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm147125
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5051cfd74f2a745ee430f2ed8a20445d2f9965f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306756"
---
# <a name="removetempvar-macro-action"></a>RemoveTempVar マクロ アクション


**適用先:** Access 2013、Office 2013



"RemoveTempVar/一時変数の削除" アクションは、"SetTempVar/一時変数の設定" アクションを使用して作成した １ つの一時変数を削除するために使用します。

## <a name="setting"></a>Setting

"RemoveTempVar/一時変数の削除" アクションの引数は次のとおりです。

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
<td><p><strong>名前</strong></p></td>
<td><p>削除する一時変数の名前を入力します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

  - 一度に定義しておくことのできる一時変数は、最大 255 個です。一時変数は、削除しなければ、データベースを閉じるまでメモリに残ったままとなります。不要となった一時変数は削除することをお勧めします。

  - データベースまたはプロジェクトを閉じると、すべての一時変数が自動的に削除されます。

  - 削除対象の変数の名前を誤って入力しても、エラーは表示されません。その削除対象の変数は、データベースを閉じるまでメモリに残ったままとなります。

  - If you have created more than one temporary variable and you want to remove them all at once, use the **RemoveAllTempVars** action.

  - To run the **RemoveTempVar** action in a VBA module, use the **Remove** method of the **TempVars** object.

## <a name="example"></a>例

The following macro demonstrates how to create a temporary variable, use it in a condition and a message box, and then remove the temporary variable by using the **RemoveTempVar** action.

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
<td><p><strong>RemoveTempVar</strong></p></td>
<td><p><strong>Name/名前</strong>: MyVar</p></td>
</tr>
</tbody>
</table>

