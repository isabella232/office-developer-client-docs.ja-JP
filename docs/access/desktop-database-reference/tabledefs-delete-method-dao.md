---
title: TableDefs.Delete メソッド (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b7c4c2176f43a6ae586131ad44567208ff7c0ae5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621718"
---
# <a name="tabledefsdelete-method-dao"></a>TableDefs.Delete メソッド (DAO)

**適用先**: Access 2013、Office 2013

指定された **TableDef** オブジェクトを **TableDefs** コレクションから削除します。

## <a name="syntax"></a>構文

*式* .Delete(***Name***)

*式* TableDefs オブジェクトを **表す変数** 。

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
<td><p>削除する TableDef の名前です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

Delete メソッドは、**TableDef** オブジェクトがデータベースに追加されていない新しいオブジェクトである場合、または **TableDef** の **Updatable** プロパティが **True** に設定されている場合にのみ使用できます。

