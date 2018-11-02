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
ms.openlocfilehash: e43181626b885664eaf370decb7d471082c7a263
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928118"
---
# <a name="removetempvar-macro-action"></a>RemoveTempVar マクロ アクション


**適用されます**Access 2013、Office 2013。



**RemoveTempVar**アクションを使用すると、 **SetTempVar**アクションを使用して作成した 1 つの一時変数を削除します。

## <a name="setting"></a>設定値

**RemoveTempVar**アクションには、次の引数があります。

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
<td><p><strong>Name</strong></p></td>
<td><p>削除する一時変数の名前を入力します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

  - 一度に定義しておくことのできる一時変数は、最大 255 個です。一時変数は、削除しなければ、データベースを閉じるまでメモリに残ったままとなります。不要となった一時変数は削除することをお勧めします。

  - データベースまたはプロジェクトを閉じると、すべての一時変数が自動的に削除されます。

  - 削除対象の変数の名前を誤って入力しても、エラーは表示されません。その削除対象の変数は、データベースを閉じるまでメモリに残ったままとなります。

  - 1 つ以上の一時的な変数を作成し、それらを一度にすべて削除する、 **RemoveAllTempVars**アクションを使用してください。

  - VBA モジュールで**RemoveTempVar**アクションを実行するには、**一時変数**オブジェクトの**Remove**メソッドを使用します。

## <a name="example"></a>使用例

次のマクロでは、一時変数を作成し、条件とメッセージ ボックスで使用して、 **RemoveTempVar**アクションを使用して一時変数を削除する方法を示します。

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
<td><p><strong>名前</strong>: MyVar<strong>式</strong>: InputBox (&quot;、0 以外の数値を入力してください&quot;)。</p></td>
</tr>
<tr class="even">
<td><p>[TempVars]![MyVar]&lt;&gt;0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>メッセージ</strong>: =&quot;を入力する&quot; &amp; [一時変数]![MyVar]&amp; &quot;.&quot;<strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>:<strong>情報</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>RemoveTempVar</strong></p></td>
<td><p><strong>Name/名前</strong>: MyVar</p></td>
</tr>
</tbody>
</table>

