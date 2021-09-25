---
title: SetField マクロ アクション
TOCTitle: SetField macro action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 693a81a26aea22e934046c221ade55810287da95
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572691"
---
# <a name="setfield-macro-action"></a>SetField マクロ アクション

**適用先:** Access 2013、Office 2013

The **SetField** action can be used to assign a value to a field.

> [!NOTE]
> "**SetField**/フィールドの設定" アクションは、データ マクロでのみ使用できます。

## <a name="setting"></a>設定

"SetField/フィールドの設定" アクションの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>名前</strong></p></td>
<td><p>フィールドを識別する文字列。</p></td>
</tr>
<tr class="even">
<td><p><strong>値</strong></p></td>
<td><p>フィールドに割り当てる値を指定する式。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

The **SetField** action cannot be used outside of an **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block.

