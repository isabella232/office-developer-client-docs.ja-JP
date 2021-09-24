---
title: USERUI 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251511
ms.localizationpriority: medium
ms.assetid: c01dd938-677c-b2ba-8f56-4638e7e988fd
description: 状態の値に応じて、2 つの式の 1 つを評価します。
ms.openlocfilehash: 8e26154b6d6f4f8102380d03ee95417a09994567
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549358"
---
# <a name="userui-function"></a>USERUI 関数

状態の値に応じて、2 つの式の 1 つを評価  _します_。
  
## <a name="syntax"></a>構文

USERUI(** *state* **, ** *defaultexpression* **, ** *userexpression* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _state_ <br/> |必須  <br/> |**ブール型 (Boolean)** <br/> |評価する式を決定します。  <br/> |
| _defaultexpression_ <br/> |必須  <br/> |**String** <br/> |既定の式。  <br/> |
| _userexpression_ <br/> |必須  <br/> |**String** <br/> |ユーザーが指定した式。  <br/> |
   
## <a name="remarks"></a>注釈

state  _が_ 0 の場合、USERUI 関数は  _defaultexpression を評価します_。 状態  _が_ 1 の場合  _、userexpression が評価されます_。
  
## <a name="example"></a>例

USERUI(1, if(Width \> 6in, 6in, Width), Width \* 0.75) 
  
Width \* .075 という式を評価し、結果を返します。 
  

