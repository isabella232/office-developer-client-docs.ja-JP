---
title: Group マクロ ステートメント
TOCTitle: Group macro statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c82169ac430496587c6ebab5e439d70bc9319b5e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930890"
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

