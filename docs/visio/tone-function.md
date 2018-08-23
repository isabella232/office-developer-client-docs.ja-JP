---
title: TONE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: 色を変更するには、int パラメーターで指定した量によって鮮やかさを減少します。
ms.openlocfilehash: be89764c849299288963c272f8ffb2d5d728f270
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806675"
---
# <a name="tone-function"></a>TONE 関数

色を変更するには、 _int_パラメーターで指定した量によって鮮やかさを減少します。 
  
## <a name="syntax"></a>構文

トーン (* **色** *、* * *int* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |Microsoft Visio カラー インデックスまたは RGB 値を指定します。  <br/> |
| _int_ <br/> |必須  <br/> |**Integer** <br/> |色の鮮やかさを減少する量を指定します。正または負の値を指定できます。  <br/> |
   
### <a name="return-value"></a>戻り値

 **RGB**
  
## <a name="remarks"></a>注釈

鮮やかさの上限と下限は、それぞれ 0 と 240 です。 _Int_パラメーターに渡すことができます、整数のサイズに制限はありませんが、鮮やかさがこの制限を超えることはありません。 
  

