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
description: state の値に応じて、2つの式のいずれかを評価します。
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331326"
---
# <a name="userui-function"></a>USERUI 関数

_state_の値に応じて、2つの式のいずれかを評価します。
  
## <a name="syntax"></a>構文

userui (* * *state* * *, * * *defaultexpression* * *, * * *userui* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _state_ <br/> |必須  <br/> |**Boolean** <br/> |評価する式を指定します。  <br/> |
| _defaultexpression_ <br/> |必須  <br/> |**String** <br/> |既定の式を指定します。  <br/> |
| _userexpression_ <br/> |必須  <br/> |**String** <br/> |ユーザーによって指定された式。  <br/> |
   
## <a name="remarks"></a>解説

_state_が0の場合、userui 関数は_defaultexpression_を評価します。 _state_が1の場合は、 _userexpression_を評価します。
  
## <a name="example"></a>例

userui (1, if (幅\>6in, 6in, width), 幅\*0.75) 
  
式の幅\*075 を評価し、結果を返します。 
  

