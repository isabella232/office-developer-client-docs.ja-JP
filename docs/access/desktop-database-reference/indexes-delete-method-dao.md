---
title: Indexes.Delete メソッド (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ab52f353b7a3e636f64ff2ad6ad5354d62bed48
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703546"
---
# <a name="indexesdelete-method-dao"></a>Indexes.Delete メソッド (DAO)

**適用されます**Access 2013、Office 2013。

指定した **Index** を **Indexes** コレクションから削除します。

## <a name="syntax"></a>構文

*式*です。(***名前***) を削除します。

*式***インデックス**オブジェクトを表す変数です。

## <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p>削除するインデックスの名前を指定します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**削除**メソッドは、**インデックス**オブジェクトは、新しいされ、データベースに追加されていない場合にのみでサポートされています。

