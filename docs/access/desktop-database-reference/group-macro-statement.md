---
title: Group マクロ ステートメント
TOCTitle: Group macro statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4c2504e30445b78d04e55bd5e8cab0ed0fd551eb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581148"
---
# <a name="group-macro-statement"></a>Group マクロ ステートメント


**適用先**: Access 2013、Office 2013

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
<td><p><strong>説明</strong></p></td>
<td><p>いいえ</p></td>
<td><p>折りたたんだときに、グループのタイトルとして表示する文字列。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

The **Group** statment does not define a region of a macro that can be executed separately. Use the **[Submacro](submacro-macro-statement.md)** statment to define a set of actions to be executed separately in the **Macro Designer** window.

