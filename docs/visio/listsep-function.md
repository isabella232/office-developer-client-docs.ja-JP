---
title: LISTSEP 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251882
localization_priority: Normal
ms.assetid: 73dc5981-2c8c-e76e-e4bd-e65a7c8db242
description: 現在のユーザーロケールのリスト区切り文字列を返します。
ms.openlocfilehash: 901442a3c2af8509855b8b038057e7f813634ea1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322345"
---
# <a name="listsep-function"></a>LISTSEP 関数

現在のユーザーロケールのリスト区切り文字列を返します。
  
## <a name="syntax"></a>構文

LISTSEP ()
  
### <a name="return-value"></a>戻り値

String
  
## <a name="example"></a>例

setf (getref (ユーザーエクステント), "MAX (Width" &amp; listsep () &amp; "Height)") 
  

