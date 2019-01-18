---
title: PageSize プロパティ (ADO)
TOCTitle: PageSize property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9365acb13820f898c053d4c90fc252bfd3b228c4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709552"
---
# <a name="pagesize-property-ado"></a>PageSize プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

[Recordset](recordset-object-ado.md) の 1 ページを構成するレコード数を示します。

## <a name="settings-and-return-values"></a>設定値および戻り値

1 ページのレコード数を示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 10 です。

## <a name="remarks"></a>解説

データの論理ページを構成するレコード数を調べるには、 **PageSize** プロパティを使用します。 ページ サイズを設定すると、 [AbsolutePage](absolutepage-property-ado.md) プロパティを使用して、特定のページの最初のレコードに移動できます。 これは、機能は、同時にレコード数を表示、データのページにユーザーを許可すると、web サーバーのシナリオで便利です。

このプロパティはいつでも設定でき、その値は、特定のページの最初のレコードの位置を計算するために使用されます。

