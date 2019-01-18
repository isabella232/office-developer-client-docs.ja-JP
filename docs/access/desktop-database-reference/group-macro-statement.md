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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713997"
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


## <a name="remarks"></a>注釈

**グループ**・ ステートメントでは、個別に実行できるマクロの領域が定義されていません。 **[サブマクロ](submacro-macro-statement.md)** ステートメントを使用すると、**マクロ デザイナー** ] ウィンドウで個別に実行するアクションのセットを定義します。

