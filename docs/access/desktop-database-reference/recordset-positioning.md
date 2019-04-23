---
title: レコードセットの配置
TOCTitle: Recordset positioning
ms:assetid: 1b8b08d5-a11c-ec6e-201c-1405171a1264
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248955(v=office.15)
ms:contentKeyID: 48543546
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cffb5adce1266bd7fdd08989e9f92110f4829ba0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284505"
---
# <a name="recordset-positioning"></a>レコードセットの配置

**適用先:** Access 2013、Office 2013

**Recordset** オブジェクト内での、順序に基づくレコードの移動、および現在のレコードの順序の確認には、 **AbsolutePosition** プロパティを使用します。このプロパティを使用するには、プロバイダーで該当する機能がサポートされている必要があります。

**AbsolutePosition** は 1 から始まり、現在のレコードが **Recordset** 内の最初のレコードの場合は、値が 1 になります。前に説明したように、 **Recordset** オブジェクト内のレコードの合計数は、 **RecordCount** プロパティで取得できます。

**AbsolutePosition** プロパティを設定すると、現在のキャッシュに存在するレコードが対象であっても、指定したレコードで始まる新しいレコード グループがキャッシュに再読み込みされます。 **CacheSize** プロパティにより、このグループのサイズが決定されます。

> [!NOTE]
> [!メモ] 代替レコード番号として **AbsolutePosition** プロパティを使用することはできません。特定のレコードの位置は、前のレコードを削除すると変更されます。また、 **Recordset** オブジェクトを再クエリした場合、または再び開いた場合は、特定のレコードの **AbsolutePosition** が同じ値になるとは限りません。特定の位置を保持し、その位置に戻るためにお勧めする方法、そしてすべての種類の **Recordset** オブジェクトで位置を決定できる唯一の方法は、ブックマークを使用することです。


