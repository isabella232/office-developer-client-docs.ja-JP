---
title: Indexes.Delete メソッド (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ed6fa376b4e0205f33ee5515d908c810f4b4b31d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615333"
---
# <a name="indexesdelete-method-dao"></a>Indexes.Delete メソッド (DAO)

**適用先**: Access 2013、Office 2013

指定した **Index** を **Indexes** コレクションから削除します。

## <a name="syntax"></a>構文

*式* .Delete(***Name***)

*式* Indexes オブジェクトを **表す変数** 。

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
<th><p>必須かどうか</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>名前</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p>削除するインデックスの名前を指定します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**Delete** メソッドは、**Index** オブジェクトが新しく作成されたものであり、まだデータベースに追加されていない場合のみ使用できます。

