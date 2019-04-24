---
title: Delete メソッド (DAO)
TOCTitle: Delete Method
ms:assetid: 8d3c3221-3b2e-15ba-32ff-f2dfc592d82c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197351(v=office.15)
ms:contentKeyID: 48546252
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ab52f353b7a3e636f64ff2ad6ad5354d62bed48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291553"
---
# <a name="indexesdelete-method-dao"></a>Delete メソッド (DAO)

**適用先:** Access 2013、Office 2013

指定した **Index** を **Indexes** コレクションから削除します。

## <a name="syntax"></a>構文

*式*。削除 (***名前***)

*式***Indexes**オブジェクトを表す変数を取得します。

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
<td><p><em>名前</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p>削除するインデックスの名前を指定します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**Delete** メソッドは、**Index** オブジェクトが新しく作成されたものであり、まだデータベースに追加されていない場合のみ使用できます。

