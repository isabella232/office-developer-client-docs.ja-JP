---
title: Delete メソッド (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63f543fd86e309372e0432c3e45513cd9d3942ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313994"
---
# <a name="tabledefsdelete-method-dao"></a>Delete メソッド (DAO)

**適用先:** Access 2013、Office 2013

指定された **TableDef** オブジェクトを **TableDefs** コレクションから削除します。

## <a name="syntax"></a>構文

*式*。削除 (***名前***)

*式***テーブル定義**オブジェクトを表す変数を取得します。

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
<td><p>削除する TableDef の名前です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

Delete メソッドは、**TableDef** オブジェクトがデータベースに追加されていない新しいオブジェクトである場合、または **TableDef** の **Updatable** プロパティが **True** に設定されている場合にのみ使用できます。

