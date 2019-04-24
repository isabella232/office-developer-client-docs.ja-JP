---
title: MaxRecords プロパティ (ADO)
TOCTitle: MaxRecords property (ADO)
ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15)
ms:contentKeyID: 48544475
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ed643ca3b1341d7f933901e15c20c84acb025f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289722"
---
# <a name="maxrecords-property-ado"></a>MaxRecords プロパティ (ADO)


**適用先:** Access 2013、Office 2013

クエリから [Recordset](recordset-object-ado.md) に返す最大レコード数を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

返される最大レコード数を示す長整数型 ( **Long** ) の値を設定または取得します。 既定値は 0 (制限なし) です。

## <a name="remarks"></a>注釈

**MaxRecords** プロパティは、プロバイダーがデータ ソースから返すレコード数を制限するために使用します。このプロパティの既定値は 0 で、プロバイダーが要求されたすべてのレコードを返すことを意味します。

**MaxRecords** プロパティは、 **Recordset** が閉じているときは読み取り/書き込み可能で、開いているときは読み取り専用になります。

