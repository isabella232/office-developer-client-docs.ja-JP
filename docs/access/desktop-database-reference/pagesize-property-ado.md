---
title: PageSize プロパティ (ADO)
TOCTitle: PageSize property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 41a70c07939b979c632636352c5b0a642973b5e4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562560"
---
# <a name="pagesize-property-ado"></a>PageSize プロパティ (ADO)


**適用先:** Access 2013、Office 2013

[Recordset](recordset-object-ado.md) の 1 ページを構成するレコード数を示します。

## <a name="settings-and-return-values"></a>設定および戻り値

1 ページのレコード数を示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 10 です。

## <a name="remarks"></a>注釈

データの論理ページを構成するレコードの数を調べるには、 **PageSize** プロパティを使用します。 ページ サイズを設定すると、 [AbsolutePage](absolutepage-property-ado.md) プロパティを使用して、特定のページの最初のレコードに移動できます。 これは、ユーザーが一度に一定の数のレコードを表示して、データをページに移動できる Web サーバーのシナリオで役立ちます。

このプロパティはいつでも設定でき、その値は、特定のページの最初のレコードの位置を計算するために使用されます。

