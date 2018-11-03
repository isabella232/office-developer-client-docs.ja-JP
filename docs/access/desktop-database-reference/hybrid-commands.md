---
title: ハイブリッド コマンド (デスクトップ データベース参照のアクセス)
TOCTitle: Hybrid commands
ms:assetid: 55654274-0494-349f-820d-92108284449d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249286(v=office.15)
ms:contentKeyID: 48544929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 046d005eb4a9e1c8097908e0104b8d1e5c76e2af
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946915"
---
# <a name="hybrid-commands"></a>ハイブリッド コマンド


**適用されます**Access 2013、Office 2013。

ハイブリッド コマンドとは、部分的にパラメーター化されたコマンドを指します。次に例を示します。

```vb 
 
SHAPE {select * from plants} 
 APPEND( {select * from customers where country = ?} 
 RELATE PlantCountry TO PARAMETER 0, 
 PlantRegion TO CustomerRegion ) 
```

ハイブリッド コマンドのキャッシュ動作は、通常のパラメーター化されたコマンドと同じです。

