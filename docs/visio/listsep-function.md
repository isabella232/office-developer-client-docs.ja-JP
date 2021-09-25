---
title: LISTSEP 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251882
ms.localizationpriority: medium
ms.assetid: 73dc5981-2c8c-e76e-e4bd-e65a7c8db242
description: 現在のユーザー ロケールのリスト区切り文字列を返します。
ms.openlocfilehash: 5538d8e101ceffe86d33cd4a2e334789203840bc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574007"
---
# <a name="listsep-function"></a>LISTSEP 関数

現在のユーザー ロケールのリスト区切り文字列を返します。
  
## <a name="syntax"></a>構文

LISTSEP ()
  
### <a name="return-value"></a>戻り値

String
  
## <a name="example"></a>例

SETF(GETREF(user.extent), "MAX(Width" &amp; ListSep() &amp; "Height)") 
  

