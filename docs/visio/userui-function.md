---
title: USERUI 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251511
localization_priority: Normal
ms.assetid: c01dd938-677c-b2ba-8f56-4638e7e988fd
description: 状態の値に応じて、2 つの式のいずれかを評価します。
ms.openlocfilehash: 2cfdf23986a06dcc109106bd50a1a38e5af91313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806746"
---
# <a name="userui-function"></a>USERUI 関数

_状態_の値に応じて、2 つの式のいずれかを評価します。
  
## <a name="syntax"></a>構文

USERUI (* **状態** *、* * *defaultexpression* * *、* * *userexpression* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _state_ <br/> |必須  <br/> |**ブール型 (Boolean)** <br/> |評価する式を指定します。  <br/> |
| _defaultexpression_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |既定の式。  <br/> |
| _userexpression_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |ユーザーによって指定された式を指定します。  <br/> |
   
## <a name="remarks"></a>備考

_状態_が 0 の場合、USERUI 関数は_defaultexpression_を評価します。 _状態_が 1 の場合は、 _userexpression_を評価します。
  
## <a name="example"></a>例

USERUI (1, 場合 (幅\>6 インチ、6 インチ、幅)、幅\*0.75) 
  
幅の式を評価\*.075、結果を返します。 
  

