---
title: "'RemoveAllTempVars/すべての一時変数の削除' マクロ アクション"
TOCTitle: RemoveAllTempVars Macro Action
ms:assetid: 409fd836-4a53-cefd-4264-8cee0fa8ac52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192877(v=office.15)
ms:contentKeyID: 48544430
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117413
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 49b92f90fb26ea1f7ad5f0878a7479267b35bdaf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870794"
---
# <a name="removealltempvars-macro-action"></a>"RemoveAllTempVars/すべての一時変数の削除" マクロ アクション


**適用されます**Access 2013、Office 2013。


**SetTempVar**アクションを使用して作成したすべての一時変数を削除するのには**RemoveAllTempVars**アクションを使用することができます。

## <a name="setting"></a>設定値

**RemoveAllTempVars**アクションの引数ではありません。

## <a name="remarks"></a>解説

  - 一度に定義しておくことのできる一時変数は、最大 255 個です。一時変数は、削除しなければ、データベースまたはプロジェクトを閉じるまでメモリに残ったままとなります。不要となった一時変数は削除することをお勧めします。

  - データベースまたはプロジェクトを閉じると、すべての一時変数が自動的に削除されます。

  - 1 つの一時変数を削除するに**RemoveTempVar**アクションを使用して、その引数を削除する一時変数の名前に設定します。

  - VBA モジュールで**RemoveAllTempVars**アクションを実行するには、**一時変数**オブジェクトの**RemoveAll**メソッドを使用します。

## <a name="example"></a>使用例

次のマクロでは、一時変数を作成し、条件とメッセージ ボックスで使用して、 **RemoveAllTempVars**アクションを使用して一時変数を削除する方法を示します。

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
<td><p><strong>RemoveAllTempVars</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

