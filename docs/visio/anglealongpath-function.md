---
title: ANGLEALONGPATH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: 指定されたポイントのパスに対する接線の角度を返します。
ms.openlocfilehash: ec5529037275fc8661972cc7403886cd33150b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804797"
---
# <a name="anglealongpath-function"></a>ANGLEALONGPATH 関数

指定されたポイントのパスに対する接線の角度を返します。
  
## <a name="version-information"></a>バージョン情報

Visio 2010 のバージョンが追加されます。 
  
## <a name="syntax"></a>構文

ANGLEALONGPATH (* **で** *、* **旅行** * * * *[] セグメント** *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。  <br/> |
| _旅行_ <br/> |必須  <br/> |**Double** <br/> |パスの始点から終点までの割合。0 ～ 1 の値を指定する必要があります。  <br/> |
| _セグメント_ <br/> |省略可能  <br/> |**整数型 (Integer)** <br/> |接線角度を計算するパスの 1 から始まるセグメント。  <br/> |
   
### <a name="return-value"></a>�߂�l

 **Double**
  
## <a name="remarks"></a>解説

_セグメント_の値を含めると、ANGLEALONGPATH はそのセグメントのみの値を返します。 
  
_セグメント_の値を含めると、ANGLEALONGPATH は_旅行_を使用して_セグメント_に沿って percertage を計算するのには、接線の点を決定します。
  
_セクション_または_セグメント_のいずれかが存在しない場合 Microsoft Visio は #ref! を返します。 
  

