---
title: Index プロパティ (DAO)
TOCTitle: Required Property
ms:assetid: ec8fafc4-8155-c48e-b3c8-2d9be425175a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836310(v=office.15)
ms:contentKeyID: 48548518
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052963
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2660a4cb422d91cf46b98a8d3870d2ab2db73fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291700"
---
# <a name="indexrequired-property-dao"></a>Index プロパティ (DAO)

**適用先:** Access 2013、Office 2013

**[Field](field-object-dao.md)** オブジェクトに非 Null 値が必要かどうかを示す値を設定または取得します。

## <a name="syntax"></a>構文

*式*。必須

*式***Index**オブジェクトを表す変数を取得します。

## <a name="remarks"></a>注釈

> [!NOTE]
> [!メモ] **Index** オブジェクトまたは **Field** オブジェクトのいずれかにこのプロパティを設定できる場合は、 **Field** オブジェクトに設定します。 **Field** オブジェクトのプロパティ設定の妥当性が検査された後、 **Index** オブジェクトの設定が検査されます。

**Required** プロパティを使用できるかどうかは、次の表に示すように、 [Fields](fields-collection-dao.md) コレクションが含まれているオブジェクトによって決まります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Fields コレクションの所属先</p></th>
<th><p>Required プロパティの使用</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong> オブジェクト</p></td>
<td><p>サポートされない</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong> オブジェクト</p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong> オブジェクト</p></td>
<td><p>値の取得のみ可能です。</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong> オブジェクト</p></td>
<td><p>サポートしません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong> オブジェクト</p></td>
<td><p>値の取得および設定が可能です。</p></td>
</tr>
</tbody>
</table>

