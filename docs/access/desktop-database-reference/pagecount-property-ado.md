---
title: PageCount プロパティ (ADO)
TOCTitle: PageCount property (ADO)
ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15)
ms:contentKeyID: 48546609
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef5179f44a2c7c153411ae33566f3806f1e93573
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867371"
---
# <a name="pagecount-property-ado"></a>PageCount プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

[Recordset](recordset-object-ado.md) オブジェクトに含まれるデータのページ数を示します。

## <a name="return-value"></a>戻り値

**Recordset** のページ数を示す長整数型 ( **Long** ) の値を返します。

## <a name="remarks"></a>解説

**PageCount**プロパティのデータ ページの数を決定するが、**レコード セット**オブジェクトでは使用します。 *ページ*は、 [PageSize](pagesize-property-ado.md)プロパティの設定のと同じサイズのレコードのグループです。 **PageSize**の値よりも少ないレコードがあるため、最後のページが完了しない場合でも、 **PageCount**の値に追加ページとしてカウントします。 **Recordset**オブジェクトがこのプロパティをサポートしていない場合、値は**PageCount**は決められていないことを示す-1 になります。

ページ機能の詳細については、 **PageSize** プロパティおよび [AbsolutePage](absolutepage-property-ado.md) プロパティのトピックを参照してください。

