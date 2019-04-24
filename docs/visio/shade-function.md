---
title: SHADE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: int パラメーターで指定された正または負の値で明度を減らして色を変更します。
ms.openlocfilehash: b31b4c49a823ace3f6474b94ba3737791928520d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326599"
---
# <a name="shade-function"></a>SHADE 関数

_int_パラメーターで指定された正または負の値で明度を減らして色を変更します。 
  
## <a name="syntax"></a>構文

網掛け (* * *color* * *, * * *int* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |Microsoft Visio カラー インデックスまたは RGB 値を指定します。  <br/> |
| _int_ <br/> |必須  <br/> |**整数型 (Integer)** <br/> |色の輝度を減少する量を指定します。 正または負の値を指定できます。  <br/> |
   
### <a name="return-value"></a>戻り値

 **RGB**
  
## <a name="remarks"></a>解説

明度の上限と下限は、それぞれ 0 と 240 です。 _int_パラメーターに渡すことができる整数のサイズに制限はありませんが、明度がこれらの制限を超えることはありません。 
  
![明度の上限と下限](media/image199_ZA10173627.gif)
  

