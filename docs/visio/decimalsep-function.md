---
title: DECIMALSEP 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251883
localization_priority: Normal
ms.assetid: 091fe401-05b2-464f-9333-7bb7118cd7cd
description: 現在のユーザー ロケールの小数点区切り文字の文字列を返します。
ms.openlocfilehash: a47bc20702262ab7d4a072694c36e424e6949919
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805196"
---
# <a name="decimalsep-function"></a>DECIMALSEP 関数

現在のユーザー ロケールの小数点区切り文字の文字列を返します。
  
## <a name="syntax"></a>構文

DECIMALSEP( )
  
## <a name="example"></a>例

SETF(GETREF(user.size)、user.wholePart &amp; DECIMALSEP() &amp; user.fracPart) 
  

