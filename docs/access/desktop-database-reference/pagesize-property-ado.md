---
title: PageSize プロパティ (ADO)
TOCTitle: PageSize property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e9b2a5857ef5d04bd45a36176d7daeebaf63678d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883275"
---
# <a name="pagesize-property-ado"></a>PageSize プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

[Recordset](recordset-object-ado.md) の 1 ページを構成するレコード数を示します。

## <a name="settings-and-return-values"></a>設定値および戻り値

1 ページのレコード数を示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 10 です。

## <a name="remarks"></a>解説

データの論理ページを構成するレコード数を調べるには、 **PageSize** プロパティを使用します。 ページ サイズを設定すると、 [AbsolutePage](absolutepage-property-ado.md) プロパティを使用して、特定のページの最初のレコードに移動できます。 これは、機能は、同時にレコード数を表示、データのページにユーザーを許可すると、web サーバーのシナリオで便利です。

このプロパティはいつでも設定でき、その値は、特定のページの最初のレコードの位置を計算するために使用されます。

