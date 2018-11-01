---
title: Relations.Delete メソッド (DAO)
TOCTitle: Delete Method
ms:assetid: e95408d2-9dde-44e7-875e-8f2d4b837cf6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836064(v=office.15)
ms:contentKeyID: 48548438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1a7ad2345e547232b79085ec5942ce5ca7d8b5c8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870024"
---
# <a name="relationsdelete-method-dao"></a>Relations.Delete メソッド (DAO)


**適用されます**Access 2013、Office 2013。

指定された **Relation** を **Relations** コレクションから削除します。

## <a name="syntax"></a>構文

*式*です。(***名前***) を削除します。

*式***関係**オブジェクトを表す変数です。

### <a name="parameters"></a>パラメーター

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
<td><p>名前</p></td>
<td><p>必須</p></td>
<td><p><strong>文字列型 (String)</strong></p></td>
<td><p>削除するリレーションシップの名前です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**Delete** メソッドは、 **Relation** オブジェクトが何も追加されていない新しいオブジェクトである場合にのみ使用できます。

