---
title: PageCount プロパティ (ADO)
TOCTitle: PageCount property (ADO)
ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15)
ms:contentKeyID: 48546609
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b37ccc0c9a61e00b3c2e8f5eb3367831e5ddea43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288120"
---
# <a name="pagecount-property-ado"></a>PageCount プロパティ (ADO)


**適用先:** Access 2013、Office 2013

[Recordset](recordset-object-ado.md) オブジェクトに含まれるデータのページ数を示します。

## <a name="return-value"></a>戻り値

**Recordset** のページ数を示す長整数型 (**Long**) の値を返します。

## <a name="remarks"></a>注釈

Use the **PageCount** property to determine how many pages of data are in the **Recordset** object. *ページ*は、 [PageSize](pagesize-property-ado.md)プロパティの設定値に等しいサイズを持つレコードのグループです。 Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value. If the **Recordset** object does not support this property, the value will be -1 to indicate that the **PageCount** is indeterminable.

ページ機能の詳細については、 **PageSize** プロパティおよび [AbsolutePage](absolutepage-property-ado.md) プロパティのトピックを参照してください。

