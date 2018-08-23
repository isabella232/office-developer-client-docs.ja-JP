---
title: MSOSHADE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: 指定された割合で明度を減らして色を変更します。
ms.openlocfilehash: f5f6eb0b6009473dcec017e951cca2f90b6c4d55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805911"
---
# <a name="msoshade-function"></a>MSOSHADE 関数

指定された割合で明度を減らして色を変更します。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

MSOSHADE (* **色** *、* * *deltaLum-* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |必須  <br/> |**RGB** <br/> |標準の RGB (red、green、blue) による色の値または色への参照。  <br/> |
| _-deltaLum_ <br/> |必須  <br/> |**Integer** <br/> |白に向かって変化率 (-100%)] または [_色_の値から黒 (100%)。  <br/> |
   
## <a name="remarks"></a>注釈

近い_色_の値は、白または黒、小さな変更には特定_の deltaLum_の値によって生成される影。 
  

