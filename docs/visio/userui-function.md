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
description: 状態の値に応じて、2 つの式の 1 つを評価します。
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420347"
---
# <a name="userui-function"></a>USERUI 関数

状態の値に応じて、2 つの式の 1 つを評価  _します_。
  
## <a name="syntax"></a>構文

USERUI(** *state* **, ** *defaultexpression* **, ** *userexpression* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _state_ <br/> |必須  <br/> |**Boolean** <br/> |評価する式を決定します。  <br/> |
| _defaultexpression_ <br/> |必須  <br/> |**String** <br/> |既定の式。  <br/> |
| _userexpression_ <br/> |必須  <br/> |**String** <br/> |ユーザーが指定した式。  <br/> |
   
## <a name="remarks"></a>注釈

state  _が_ 0 の場合、USERUI 関数は  _defaultexpression を評価します_。 状態  _が_ 1 の場合  _、userexpression が評価されます_。
  
## <a name="example"></a>例

USERUI(1, if(Width \> 6in, 6in, Width), Width \* 0.75) 
  
Width \* .075 という式を評価し、結果を返します。 
  

