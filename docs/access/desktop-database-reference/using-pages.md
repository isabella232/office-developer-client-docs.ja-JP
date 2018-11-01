---
title: ページ (デスクトップ データベース参照のアクセス) を使用します。
TOCTitle: Using Pages
ms:assetid: 516fb7c2-c7a2-385b-83e7-2091c7283ea2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249261(v=office.15)
ms:contentKeyID: 48544817
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9ff4c0368d2811767b3211a664a42dfc8aac16ba
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874770"
---
# <a name="using-pages"></a>ページの使用


**適用されます**Access 2013、Office 2013。

**PageCount**プロパティのデータ ページの数を決定するが、**レコード セット**オブジェクトでは使用します。 *ページ*は、 **PageSize**プロパティの設定のと同じサイズのレコードのグループです。 **PageSize**の値よりも少ないレコードがあるため、最後のページが完了しない場合でも、 **PageCount**の値に追加ページとしてカウントします。 **Recordset**オブジェクトがこのプロパティをサポートしていない場合は、 **PageCount**は**PageCount**は決められていないことを示す-1 になります。

データの論理ページを構成するレコードの数を調べるには、 **PageSize** プロパティを使用します。ページ サイズを設定すると、 **AbsolutePage** プロパティを使用して、特定のページの最初のレコードに移動できます。これは、Web サーバー上で、ユーザーが一度に一定の数のレコードを表示し、ページを移動できるようにする場合などに便利です。

このプロパティはいつでも設定でき、その値は、特定のページの最初のレコードの位置を計算するために使用されます。

現在のレコードが置かれているページ番号を確認するには、 **AbsolutePage** プロパティを使用します。ただし、このプロパティを使用するには、プロバイダーで該当する機能がサポートされている必要があります。

**AbsolutePage** は 1 から始まり、現在のレコードが **Recordset** 内の最初のレコードの場合は、値が 1 になります。特定のページの最初のレコードに移動するには、このプロパティを設定します。ページ数の合計は、 **PageCount** プロパティから取得します。

