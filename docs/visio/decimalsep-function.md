---
title: DECIMALSEP 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251883
ms.localizationpriority: medium
ms.assetid: 091fe401-05b2-464f-9333-7bb7118cd7cd
description: 現在のユーザー ロケールの小数点記号文字列を返します。
ms.openlocfilehash: 6f4262aa649d96514d5a0939f464d99404cce9d3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594630"
---
# <a name="decimalsep-function"></a>DECIMALSEP 関数

現在のユーザー ロケールの小数点記号文字列を返します。
  
## <a name="syntax"></a>構文

DECIMALSEP( )
  
## <a name="example"></a>例

SETF(GETREF(user.size), user.wholePart &amp; DECIMALSEP() &amp; user.fracPart) 
  

