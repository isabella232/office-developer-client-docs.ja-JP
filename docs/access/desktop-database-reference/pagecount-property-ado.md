---
title: PageCount プロパティ (ADO)
TOCTitle: PageCount property (ADO)
ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15)
ms:contentKeyID: 48546609
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: aab5455e4fd54316a2ef9af22b5322f85eb3a4e8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558143"
---
# <a name="pagecount-property-ado"></a>PageCount プロパティ (ADO)


**適用先:** Access 2013、Office 2013

[Recordset](recordset-object-ado.md) オブジェクトに含まれるデータのページ数を示します。

## <a name="return-value"></a>戻り値

**Recordset** のページ数を示す長整数型 (**Long**) の値を返します。

## <a name="remarks"></a>注釈

Use the **PageCount** property to determine how many pages of data are in the **Recordset** object. *ページ* は、PageSize プロパティ設定と同じサイズの [レコードのグループ](pagesize-property-ado.md) です。 Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value. If the **Recordset** object does not support this property, the value will be -1 to indicate that the **PageCount** is indeterminable.

ページ機能の詳細については、 **PageSize** プロパティおよび [AbsolutePage](absolutepage-property-ado.md) プロパティのトピックを参照してください。

