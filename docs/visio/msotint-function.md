---
title: MSOTINT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: 指定した割合で明度を増やして色を変更します。
ms.openlocfilehash: 50e81b5202174c61905d3914c50feddcb05a91cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805940"
---
# <a name="msotint-function"></a>MSOTINT 関数

指定した割合で明度を増やして色を変更します。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

MSOTINT (* **色** *、* * *deltaLum* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |必須  <br/> |**RGB** <br/> |標準の RGB (red、green、blue) による色の値または色への参照。  <br/> |
| _deltaLum_ <br/> |必須  <br/> |**Integer** <br/> |白に向かって変化率 (-100%)] または [_色_の値から黒 (100%)。  <br/> |
   
## <a name="remarks"></a>注釈

近い_色_の値は、白または黒、小さな変更には特定の_deltaLum_の値によって生成される濃淡。 
  

