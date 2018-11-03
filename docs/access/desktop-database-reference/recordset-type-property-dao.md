---
title: Recordset.Type プロパティ (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 540e5b8226907dc580d34ab3215d3c0dca67e3f6
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936883"
---
# <a name="recordsettype-property-dao"></a>Recordset.Type プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得のみ可能です。整数型 ( **Integer** ) の値を使用します。

## <a name="syntax"></a>構文

*式*です。タイプ

*式***レコード セット**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Recordset** オブジェクトの場合、設定できる値と戻り値は次のようになります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>レコードセットの種類</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbOpenTable</strong></p></td>
<td><p>テーブル (Microsoft Access ワークスペースのみ)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbOpenDynamic</strong></p></td>
<td><p>動的 (ODBCDirect ワークスペースのみ)</p>

> [!NOTE]
> [!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。


<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>dbOpenDynaset</strong></p></td>
<td><p>ダイナセット</p></td>
</tr>
<tr class="even">
<td><p><strong>dbOpenSnapshot</strong></p></td>
<td><p>スナップショット</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbOpenForwardOnly</strong></p></td>
<td><p>前方スクロール</p></td>
</tr>
</tbody>
</table>

