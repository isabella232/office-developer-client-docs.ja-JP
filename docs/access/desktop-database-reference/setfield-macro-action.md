---
title: SetField マクロ アクション
TOCTitle: SetField macro action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d8ca2315a9a84000aa29b88043e4edea05ffb0ea
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922826"
---
# <a name="setfield-macro-action"></a>SetField マクロ アクション


**適用されます**Access 2013、Office 2013。

" **SetField** /フィールドの設定" アクションを使用すると、フィールドに値を割り当てることができます。


> [!NOTE]
> <P>[!メモ] " <STRONG>SetField</STRONG> /フィールドの設定" アクションは、データ マクロでのみ使用できます。</P>



## <a name="setting"></a>設定

" **SetField** /フィールドの設定" アクションの引数は次のとおりです。

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
<td><p><strong>Name</strong></p></td>
<td><p>フィールドを識別する文字列。</p></td>
</tr>
<tr class="even">
<td><p><strong>値</strong></p></td>
<td><p>フィールドに割り当てる値を指定する式。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>備考

**SetField**アクションは、 **[CreateRecord](createrecord-data-block.md)** または**[EditRecord](editrecord-data-block.md)** のデータ ブロックの外部では使用できません。

