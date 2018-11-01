---
title: "'ClearMacroError/マクロエラーのクリア' マクロ アクション"
TOCTitle: ClearMacroError Macro Action
ms:assetid: 1091747e-e957-38c6-6454-5169f091323e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845338(v=office.15)
ms:contentKeyID: 48543296
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm109100
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e9b8232f24a837466529f8ce04f9f830af72e7a7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870192"
---
# <a name="clearmacroerror-macro-action"></a>"ClearMacroError/マクロエラーのクリア" マクロ アクション


**適用されます**Access 2013、Office 2013。


**ClearMacroError**アクションを使用すると、 **MacroError**オブジェクトに格納されているエラーについての情報をクリアします。

## <a name="setting"></a>設定値

**ClearMacroError**アクションの引数ではありません。

## <a name="remarks"></a>注釈

  - マクロでエラーが発生すると、エラーに関する情報が **MacroError** オブジェクトに格納されます。 エラー メッセージが表示されないようにするのには、**[エラー時](onerror-macro-action.md)** のアクションを使用しない場合は、マクロが停止し、エラー情報が標準エラー メッセージに表示されます。 ただし、エラー メッセージが表示されないようにするのには、**エラー時**のアクションを使用した場合を条件またはカスタム エラー メッセージでは、 **MacroError**オブジェクトに格納された情報を使用します。
    
    エラーが処理された後、 **MacroError**オブジェクト内の情報は古く、 **ClearMacroError**アクションを使用してオブジェクトを消去することをお勧めします。 これにより、 **MacroError**オブジェクトのエラー番号が 0 にリセットし、エラーの説明、マクロ名、アクション名、条件、および引数など、オブジェクトに格納されているエラーに関するその他の情報をクリアします。 このようにすると、後で再度 **MacroError** オブジェクトを調査して、別のエラーが発生していないかを確認できます。

  - **ClearMacroError**アクションを使用して、マクロの末尾にする必要はありませんのでは、 **MacroError**オブジェクトが任意のマクロが終了すると自動的にクリアされます。

  - **MacroError** オブジェクトには、一度に 1 つのエラー情報のみが格納されます。マクロで複数のエラーが発生した場合は、最後のエラーに関する情報だけが **MacroError** オブジェクトに格納されます。

  - **ClearMacroError**アクションは、VBA モジュールで実行するには、 **DoCmd**オブジェクトの**ClearMacroError**メソッドを使用します。

## <a name="example"></a>使用例

次のマクロは、**次**の引数**OnError**アクションを使用して、エラー メッセージが表示されないようにし **、このアクション**を使用して、フォームを開きます。 この例では、エラーが意図的に前のレコードに移動するのには、 **GoToRecord**アクションを使用して作成します。 条件**\[MacroError\]です\[。数\]\<\>0** 、 **MacroError**オブジェクトをテストします。 エラーが発生した場合、エラー番号は、0 以外の場合、および**メッセージ ボックス**のアクションを実行します。 メッセージ ボックスが表示されます (ここでは、 **GoToRecord**アクション)、エラーを発生させたアクションの名前と、エラー番号が表示されます。 最後に、 **ClearMacroError**アクションを実行すると、 **MacroError**オブジェクトがクリアされます。

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
<td><p><strong>OnError</strong></p></td>
<td><p><strong>移動</strong>:<strong>次へ</strong></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>フォーム名</strong>: CategoryForm<strong>ビュー</strong>: <strong>FormWindow モード</strong>:<strong>標準</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToRecord</strong></p></td>
<td><p><strong>オブジェクトの種類</strong>: <strong>FormObject 名</strong>: CategoryForm<strong>レコード</strong>: 前</p></td>
</tr>
<tr class="even">
<td><p>[MacroError] です。[番号]&lt; &gt;0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>メッセージ</strong>: =&quot;エラー # &quot; &amp; [MacroError] です。[番号]&amp; &quot; [ &quot; &amp; [MacroError] です。[アクション名]&amp; &quot;アクション。&quot;<strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>: 情報</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>ClearMacroError</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

