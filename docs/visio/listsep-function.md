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
description: 現在のユーザー ロケールのリスト区切り文字列を返します。
ms.openlocfilehash: 901442a3c2af8509855b8b038057e7f813634ea1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431408"
---
# <a name="listsep-function"></a>LISTSEP 関数

現在のユーザー ロケールのリスト区切り文字列を返します。
  
## <a name="syntax"></a>構文

LISTSEP ()
  
### <a name="return-value"></a>戻り値

String
  
## <a name="example"></a>例

SETF(GETREF(user.extent), "MAX(Width" &amp; ListSep() &amp; "Height)") 
  

