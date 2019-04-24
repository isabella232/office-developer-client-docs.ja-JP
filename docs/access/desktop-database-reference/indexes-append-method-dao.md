---
title: Append メソッド (DAO)
TOCTitle: Append Method
ms:assetid: 60dce80f-505b-e988-3ac1-8ecaae3d3d09
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194835(v=office.15)
ms:contentKeyID: 48545191
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bcebcf2f7fbce59c6050100f1763923a6025526e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291652"
---
# <a name="indexesappend-method-dao"></a>Append メソッド (DAO)

**適用先:** Access 2013、Office 2013

新しい **Index** を **Indexes** コレクションに追加します。

## <a name="syntax"></a>構文

*式*。Append (***Object***)

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
<td><p><em>Object</em></p></td>
<td><p>必須</p></td>
<td><p><strong>Object</strong></p></td>
<td><p>コレクションに追加する項目を表すオブジェクト変数。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

追加されたオブジェクトは、ディスクに格納され、**Delete** メソッドを使用して削除するまで持続します。

新しいオブジェクトの追加は直ちに実行されますが、データベース構造の変更によって他のコレクションが影響を受ける場合は、そのコレクションの **Refresh** メソッドを使用する必要があります。

追加しようとしているオブジェクトが不完全である (たとえば、**Indexes** コレクションに追加する前に **Index** オブジェクトの **Fields** コレクションに **Field** オブジェクトが 1 つも追加されていない) 場合や、1 つ以上の従属オブジェクトのプロパティが正しく設定されていない場合、**Append** メソッドを使用すると、エラーが発生します。たとえば、フィールドの種類が指定されていないのに、**TableDef** オブジェクトの **Fields** コレクションに **Field** オブジェクトを追加しようとすると、**Append** メソッドで実行時エラーが発生します。

