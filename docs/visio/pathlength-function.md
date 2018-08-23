---
title: PATHLENGTH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: 指定した [Geometry] セクションで定義されているパスの長さを返します。
ms.openlocfilehash: 37cabbde9fc0782bc1fde46f3065d0c945c9dada
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805981"
---
# <a name="pathlength-function"></a>PATHLENGTH 関数

指定した [Geometry] セクションで定義されているパスの長さを返します。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

PATHLENGTH (* **で** * * * *[] セグメント** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。  <br/> |
| _セグメント_ <br/> |省略可能  <br/> |**整数型 (Integer)** <br/> |測定するパスの 1 から始まるセグメント。  <br/> |
   
### <a name="return-value"></a>戻り値

 **Double**
  
## <a name="remarks"></a>注釈

_セクション_または_セグメント_が存在しない場合 Microsoft Visio は #ref! を返します。 
  
_セグメント_の値を含めると、PATHLENGTH はその部分だけの長さを返します。 
  

