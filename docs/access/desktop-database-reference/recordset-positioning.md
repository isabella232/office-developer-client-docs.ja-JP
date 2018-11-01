---
title: レコードセットを配置する
TOCTitle: Recordset Positioning
ms:assetid: 1b8b08d5-a11c-ec6e-201c-1405171a1264
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248955(v=office.15)
ms:contentKeyID: 48543546
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 34b767e50893f62a30f075bee82a4f19ce4696c5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882113"
---
# <a name="recordset-positioning"></a>レコードセットを配置する


**適用されます**Access 2013、Office 2013。

**Recordset** オブジェクト内での、順序に基づくレコードの移動、および現在のレコードの順序の確認には、 **AbsolutePosition** プロパティを使用します。このプロパティを使用するには、プロバイダーで該当する機能がサポートされている必要があります。

**AbsolutePosition** は 1 から始まり、現在のレコードが **Recordset** 内の最初のレコードの場合は、値が 1 になります。前に説明したように、 **Recordset** オブジェクト内のレコードの合計数は、 **RecordCount** プロパティで取得できます。

**AbsolutePosition** プロパティを設定すると、現在のキャッシュに存在するレコードが対象であっても、指定したレコードで始まる新しいレコード グループがキャッシュに再読み込みされます。 **CacheSize** プロパティにより、このグループのサイズが決定されます。


> [!NOTE]
> <P>[!メモ] 代替レコード番号として <STRONG>AbsolutePosition</STRONG> プロパティを使用することはできません。特定のレコードの位置は、前のレコードを削除すると変更されます。また、 <STRONG>Recordset</STRONG> オブジェクトを再クエリした場合、または再び開いた場合は、特定のレコードの <STRONG>AbsolutePosition</STRONG> が同じ値になるとは限りません。特定の位置を保持し、その位置に戻るためにお勧めする方法、そしてすべての種類の <STRONG>Recordset</STRONG> オブジェクトで位置を決定できる唯一の方法は、ブックマークを使用することです。</P>


