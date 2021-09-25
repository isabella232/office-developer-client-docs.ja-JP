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
ms.localizationpriority: medium
ms.openlocfilehash: b9f746bc0024b4882454bca686ab6170c3c0b446
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552536"
---
# <a name="removetempvar-macro-action"></a>RemoveTempVar マクロ アクション


**適用先:** Access 2013、Office 2013



"RemoveTempVar/一時変数の削除" アクションは、"SetTempVar/一時変数の設定" アクションを使用して作成した １ つの一時変数を削除するために使用します。

## <a name="setting"></a>設定

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
<td><p><strong>名前</strong>: MyVar<strong>式</strong>: InputBox( &quot; 0 以外の数値を入力します。 &quot;</p></td>
</tr>
<tr class="even">
<td><p>[TempVars]![MyVar]&lt;&gt;0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>メッセージ</strong>: = &quot; &quot; &amp; [TempVars]と入力しました![MyVar] &amp; &quot; . &quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>RemoveTempVar</strong></p></td>
<td><p><strong>Name/名前</strong>: MyVar</p></td>
</tr>
</tbody>
</table>

