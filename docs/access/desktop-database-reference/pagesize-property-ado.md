---
title: PageSize プロパティ (ADO)
TOCTitle: PageSize Property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 89b28e382f1597ff6466aa323565eaf2ff068605
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476606"
---
# <a name="pagesize-property-ado"></a>PageSize プロパティ (ADO)


**適用されます**Access 2013 |。Office 2013

[Recordset](recordset-object-ado.md) の 1 ページを構成するレコード数を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

1 ページのレコード数を示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 10 です。

## <a name="remarks"></a>解説

データの論理ページを構成するレコード数を調べるには、 **PageSize** プロパティを使用します。ページ サイズを設定すると、 [AbsolutePage](absolutepage-property-ado.md) プロパティを使用して、特定のページの最初のレコードに移動できます。これは、Web サーバーで、ユーザーが一度に特定の数のレコードを表示しながら、データのページ間を移動できるようにする場合に便利です。

このプロパティはいつでも設定でき、特定のページの最初のレコードの位置を計算するために使用されます。

