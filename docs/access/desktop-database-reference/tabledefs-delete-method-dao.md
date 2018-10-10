---
title: TableDefs.Delete メソッド (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e39a1390c9ea26baa83d8203967d603237a3ab1c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477904"
---
# <a name="tabledefsdelete-method-dao"></a>TableDefs.Delete メソッド (DAO)


**適用されます**Access 2013 |。Office 2013

指定された **TableDef** オブジェクトを **TableDefs** コレクションから削除します。

## <a name="syntax"></a>構文

*式*です。(***名前***) を削除します。

*式***テーブル定義**オブジェクトを表す変数です。

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
<td><p>削除する TableDef の名前です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**テーブル定義**オブジェクトが新しいし、データベースに追加されていない場合にのみ、または**テーブル定義**の**更新できる**プロパティが**True**に設定すると、Delete メソッドはサポートされています。

