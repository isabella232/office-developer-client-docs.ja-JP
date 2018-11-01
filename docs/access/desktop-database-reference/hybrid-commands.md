---
title: ハイブリッド コマンド (デスクトップ データベース参照のアクセス)
TOCTitle: Hybrid Commands
ms:assetid: 55654274-0494-349f-820d-92108284449d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249286(v=office.15)
ms:contentKeyID: 48544929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 363f305fee12cb2e46ab9d4c628030f7dc4bcd78
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873853"
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

