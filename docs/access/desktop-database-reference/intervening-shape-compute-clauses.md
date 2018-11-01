---
title: COMPUTE 句を使って Shape を仲介する
TOCTitle: Intervening Shape COMPUTE Clauses
ms:assetid: 3e9dcef2-776c-0365-4a92-68e325f7dbb5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249174(v=office.15)
ms:contentKeyID: 48544380
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 72be68975f0f4977198120b92055abd89d0da987
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889939"
---
# <a name="intervening-shape-compute-clauses"></a>COMPUTE 句を使って Shape を仲介する


**適用されます**Access 2013、Office 2013。

パラメーター化されたシェイプ コマンドでは、親と子の間に 1 つ以上の COMPUTE 句を埋め込むことができます。次に例を示します。

```vb 
 
SHAPE {select au_lname, state from authors} APPEND 
 ((SHAPE 
 (SHAPE 
 {select * from authors where state = ?} rs 
 COMPUTE rs, ANY(rs.state) state, ANY(rs.au_lname) au_lname 
 BY au_id) rs2 
 COMPUTE rs2, ANY(rs2.state) BY au_lname) 
RELATE state TO PARAMETER 0) 
```

