---
title: Group マクロ ステートメント
TOCTitle: Group Macro Statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35f9ad1d445dbddaa5487e28da60b9202a72dae1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879852"
---
# <a name="group-macro-statement"></a>Group マクロ ステートメント


**適用されます**Access 2013、Office 2013。

**Group** ステートメントでは、マクロ内で展開または折りたたみできるアクションのブロックを指定できます。

## <a name="setting"></a>設定

**Group** アクションの引数は次のとおりです。

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
<td><p><strong>Description</strong></p></td>
<td><p>いいえ</p></td>
<td><p>折りたたんだときに、グループのタイトルとして表示する文字列。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>備考

**グループ**・ ステートメントでは、個別に実行できるマクロの領域が定義されていません。 **[サブマクロ](submacro-macro-statement.md)** ステートメントを使用すると、**マクロ デザイナー** ] ウィンドウで個別に実行するアクションのセットを定義します。

