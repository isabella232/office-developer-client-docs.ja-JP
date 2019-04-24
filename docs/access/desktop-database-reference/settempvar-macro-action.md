---
title: SetTempVar マクロ アクション
TOCTitle: SetTempVar macro action
ms:assetid: 9c3b7bee-02c5-efbf-1276-4c4a1f7802d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198102(v=office.15)
ms:contentKeyID: 48546593
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm150219
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b630304774e521162687d4c78a6a97cf18ddb419
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306523"
---
# <a name="settempvar-macro-action"></a>SetTempVar マクロ アクション


**適用先:** Access 2013、Office 2013



**SetTempVar** アクションは、一時変数を作成し、特定の値に設定するために使用します。作成した変数は、後続のアクションで条件や引数として使用したり、別のマクロ、イベント プロシージャ、フォーム、またはレポートで使用することができます。

## <a name="setting"></a>Setting

**SetTempVar** アクションの引数は次のとおりです。

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
<td><p>一時変数の名前を入力します。</p></td>
</tr>
<tr class="even">
<td><p><strong>Expression/式</strong></p></td>
<td><p>この一時変数の値を設定するために使用する式を入力します。 式の前に等号 (<strong>=</strong>) 記号を付けないでください。 [<strong>ビルド</strong>] ボタンをクリックすることができます。 <img src="media/access-build-button.gif" title="buildbut_ZA06047218" alt="buildbut_ZA06047218" /> 式ビルダーを使用して、この引数を設定することができます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

- 一度に定義しておくことのできる一時変数は、最大 255 個です。一時変数は、削除しなければ、データベースを閉じるまでメモリに残ったままとなります。不要になった一時変数は削除することをお勧めします。特定の一時変数を削除するには、削除する一時変数の名前を引数に指定して **[RemoveTempVar](removetempvar-macro-action.md)** アクションを実行します。複数の一時変数を一括して削除するには、 **RemoveAllTempVars** アクションを使用します。

- 一時変数はグローバルな変数です。 一時変数は、作成されると、イベント プロシージャ、Visual Basic for Applications (VBA) モジュール、クエリ、または式で参照できます。 たとえば、 *MyVar*という名前の一時変数を作成した場合は、次の構文を使用して、テキストボックスのコントロールソースとして変数を使用することができます。
    
  `=[TempVars]![MyVar]`
    
  > [!NOTE]
  > [!メモ] マクロ、クエリ、およびイベント プロシージャでは、式の前に等号 (=) を付ける必要はありません。
 
  一時変数は、アドインまたは参照先データベースでも参照できます。

- VBA モジュールで **SetTempVar** アクションを実行するには、**TempVars** オブジェクトの **Add** メソッドを使用します。

## <a name="example"></a>例

次のマクロでは、**SetTempVar** アクションを使用して一時変数を作成し、条件およびメッセージ ボックスで一時変数を使用してから削除する方法を示しています。

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

