---
title: MSOSHADE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: 指定された割合で明度を減らして色を変更します。
ms.openlocfilehash: 207893552c7378589d4a648bf29ed88fcfd15224
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414495"
---
# <a name="msoshade-function"></a>MSOSHADE 関数

指定された割合で明度を減らして色を変更します。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

MSOSHADE(** *color* **, ** *-deltaLum* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |必須  <br/> |**RGB** <br/> |標準の RGB (red、green、blue) による色の値または色への参照。  <br/> |
| _-deltaLum_ <br/> |必須  <br/> |**整数型 (Integer)** <br/> |白に向かって変化する割合 (-100%)または黒 (100%)色の  _値から取得_ します。  <br/> |
   
## <a name="remarks"></a>注釈

色の値  _が_ 白または黒に近いほど、特定の -deltaLum 値によって生成される網掛け  _への変更が小さ_ になります。 
  

