---
title: Group マクロ ステートメント
TOCTitle: Group macro statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2dc25621a49d8fd23078a926d6ec6c5de54e54d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292112"
---
# <a name="group-macro-statement"></a>Group マクロ ステートメント


**適用先:** Access 2013、Office 2013

**Group** ステートメントでは、マクロ内で展開または折りたたみできるアクションのブロックを指定できます。

## <a name="setting"></a>Setting

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

