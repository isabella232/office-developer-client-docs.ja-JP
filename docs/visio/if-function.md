---
title: IF 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251442
localization_priority: Normal
ms.assetid: 66771ad3-0fb3-68ff-81da-d1162d37c05a
description: 論理式が TRUE の場合は、valueiftrue を返します。 それ以外の場合は、valueiffalse を返します。
ms.openlocfilehash: 8780bd3dd5ded1a950a5bf3f79333687f3b6843c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405472"
---
# <a name="if-function"></a>IF 関数

論理式  _が TRUE の_ 場合  _は、valueiftrue を_ 返します。 それ以外の場合は  _、valueiffalse を返します_。
  
## <a name="syntax"></a>構文

IF(** *logicalexpression* **, ** *valueiftrue* **, ** *valueiffalse* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |必須  <br/> |**String** <br/> |評価する式を指定します。  <br/> |
| _valueiftrue_ <br/> |必須  <br/> |**さまざま** <br/> |_logicalexpression が true の場合に返す_ 値。  <br/> |
| _valueiffalse_ <br/> |必須  <br/> |**さまざま** <br/> | 論理式が  _false の場合に返す_ 値。  <br/> |
   
### <a name="return-value"></a>戻り値

さまざま
  
## <a name="example"></a>例

IF(Height \> 1.25 in,5,7)
  
図形の高さが 1.25 インチを超える場合は、5 を返します。図形の高さが 1.25 インチ以下の場合は、7 を返します。
  

