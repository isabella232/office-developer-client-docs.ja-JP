---
title: MaxRecords プロパティ (ADO)
TOCTitle: MaxRecords Property (ADO)
ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15)
ms:contentKeyID: 48544475
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d8753bf09655371042e97ead083c6849f1736b8b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477737"
---
# <a name="maxrecords-property-ado"></a>MaxRecords プロパティ (ADO)


**適用されます**Access 2013 |。Office 2013

クエリから [Recordset](recordset-object-ado.md) に返す最大レコード数を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

返される最大レコード数を示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 0 (制限なし) です。

## <a name="remarks"></a>解説

**MaxRecords** プロパティは、プロバイダーがデータ ソースから返すレコード数を制限するために使用します。このプロパティの既定値は 0 で、プロバイダーが要求されたすべてのレコードを返すことを意味します。

**MaxRecords** プロパティは、 **Recordset** が閉じているときは読み取り/書き込み可能で、開いているときは読み取り専用になります。

