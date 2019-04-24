---
title: ページを使用する (Access デスクトップデータベースリファレンス)
TOCTitle: Using Pages
ms:assetid: 516fb7c2-c7a2-385b-83e7-2091c7283ea2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249261(v=office.15)
ms:contentKeyID: 48544817
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92d6185c3234a58ea9a84310291d0c37e0272535
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305874"
---
# <a name="using-pages"></a>ページの使用


**適用先:** Access 2013、Office 2013

Use the **PageCount** property to determine how many pages of data are in the **Recordset** object. *ページ*は、 **PageSize**プロパティの設定値に等しいサイズを持つレコードのグループです。 Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value. If the **Recordset** object does not support this property, **PageCount** will be -1 to indicate that the **PageCount** is indeterminable.

データの論理ページを構成するレコードの数を調べるには、 **PageSize** プロパティを使用します。ページ サイズを設定すると、 **AbsolutePage** プロパティを使用して、特定のページの最初のレコードに移動できます。これは、Web サーバー上で、ユーザーが一度に一定の数のレコードを表示し、ページを移動できるようにする場合などに便利です。

このプロパティはいつでも設定でき、その値は、特定のページの最初のレコードの位置を計算するために使用されます。

現在のレコードが置かれているページ番号を確認するには、 **AbsolutePage** プロパティを使用します。ただし、このプロパティを使用するには、プロバイダーで該当する機能がサポートされている必要があります。

**AbsolutePage** は 1 から始まり、現在のレコードが **Recordset** 内の最初のレコードの場合は、値が 1 になります。特定のページの最初のレコードに移動するには、このプロパティを設定します。ページ数の合計は、 **PageCount** プロパティから取得します。

