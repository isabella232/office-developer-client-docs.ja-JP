---
title: レコード セットを配置
TOCTitle: Recordset positioning
ms:assetid: 1b8b08d5-a11c-ec6e-201c-1405171a1264
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248955(v=office.15)
ms:contentKeyID: 48543546
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5116adbf68e4e98c7fbda8285348e00638465742
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946273"
---
# <a name="recordset-positioning"></a>レコード セットを配置


**適用されます**Access 2013、Office 2013。

**Recordset** オブジェクト内での、順序に基づくレコードの移動、および現在のレコードの順序の確認には、 **AbsolutePosition** プロパティを使用します。このプロパティを使用するには、プロバイダーで該当する機能がサポートされている必要があります。

**AbsolutePosition** は 1 から始まり、現在のレコードが **Recordset** 内の最初のレコードの場合は、値が 1 になります。前に説明したように、 **Recordset** オブジェクト内のレコードの合計数は、 **RecordCount** プロパティで取得できます。

**AbsolutePosition** プロパティを設定すると、現在のキャッシュに存在するレコードが対象であっても、指定したレコードで始まる新しいレコード グループがキャッシュに再読み込みされます。 **CacheSize** プロパティにより、このグループのサイズが決定されます。


> [!NOTE]
> <P>[!メモ] 代替レコード番号として <STRONG>AbsolutePosition</STRONG> プロパティを使用することはできません。特定のレコードの位置は、前のレコードを削除すると変更されます。また、 <STRONG>Recordset</STRONG> オブジェクトを再クエリした場合、または再び開いた場合は、特定のレコードの <STRONG>AbsolutePosition</STRONG> が同じ値になるとは限りません。特定の位置を保持し、その位置に戻るためにお勧めする方法、そしてすべての種類の <STRONG>Recordset</STRONG> オブジェクトで位置を決定できる唯一の方法は、ブックマークを使用することです。</P>


