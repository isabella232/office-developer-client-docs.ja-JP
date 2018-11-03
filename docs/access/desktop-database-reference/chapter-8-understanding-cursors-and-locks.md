---
title: '第 8 章: カーソルとロック'
TOCTitle: 'Chapter 8: Understanding cursors and locks'
ms:assetid: 889356f9-53ca-3c46-6781-b37e1f065717
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249598(v=office.15)
ms:contentKeyID: 48546139
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ca76b5635e057251aff845ecf45146e6e0d89a6
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936940"
---
# <a name="chapter-8-understanding-cursors-and-locks"></a>第 8 章: カーソルとロック

**適用されます**Access 2013、Office 2013。

アプリケーションのデータ アクセス要件に最も適した、最も効率的な種類のカーソルを選択するには、カーソルの動作を理解することが大切です。カーソルの構成が最適でない場合、データ アクセス操作の速度が極端に低下することがあります。

ADO **Recordset** オブジェクトの機能の多くは、カーソルの種類と位置、さらにはロックの種類に左右されます。

この章では、次のトピックについて説明します。

- [カーソルとは何ですか。](what-is-a-cursor.md)
- [カーソル位置の重要性](the-significance-of-cursor-location.md)
- [OLE DB 用 Microsoft Cursor Service](the-microsoft-cursor-service-for-ole-db.md)
- [CacheSize を使用する](using-cachesize.md)
- [カーソルとロックの特徴](cursor-and-lock-characteristics.md)
- [(ADO) のカーソルの種類](types-of-cursors.md)
- [ロックとは何ですか。(ADO)](what-is-a-lock.md)

