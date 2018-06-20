---
title: TINT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Int パラメーターで指定した量 (正または負) で明度を上げて色を変更します。
ms.openlocfilehash: a4b15596a4742edb4f9e4746929f19d2eafe94d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806665"
---
# <a name="tint-function"></a>TINT 関数

_Int_パラメーターで指定した量 (正または負) で明度を上げて色を変更します。 
  
## <a name="syntax"></a>構文

濃淡 (* **色** *、* * *int* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |必須  <br/> |**数値** <br/> |Microsoft Visio カラー インデックスまたは RGB 値を指定します。  <br/> |
| _int_ <br/> |必須  <br/> |**Integer** <br/> |色の輝度を増加する量を指定します。正または負の値を指定できます。  <br/> |
   
### <a name="return-value"></a>�߂�l

 **RGB**
  
## <a name="remarks"></a>備考

明度の上限と下限は、それぞれ 0 と 240 です。 _Int_パラメーターに渡すことができます、整数のサイズに制限はありませんが、明度がこの制限を超えることはありません。 
  

