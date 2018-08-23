---
title: MASTERNAME 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251581
localization_priority: Normal
ms.assetid: 519d79d4-9178-2231-c26d-aa7f31a43412
description: シートのマスター シェイプの名前として、文字列を返しますか、シートは、マスターを持っていない場合は、'マスターなし' を文字列を返します。
ms.openlocfilehash: c1d5891fba0f967cde4a4e9ca58d07f87239f0b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805833"
---
# <a name="mastername-function"></a>MASTERNAME 関数

シートのマスター シェイプの名前として、文字列を取得または設定の文字列を返します"\<マスターなし\>」シートは、マスターを持っていない場合。
  
## <a name="syntax"></a>構文

MASTERNAME ([* * *langID_opt* * *]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |省略可能  <br/> |**番号** <br/> |関数が返す文字列の言語を指定します。ローカル言語を指定するには、0 (既定値) を使用します。汎用言語を指定するには、750 を使用します。  <br/> |
   
### <a name="return-value"></a>戻り値

String
  
## <a name="remarks"></a>注釈

無効な言語コードを渡した場合、ローカル言語が使用されます。 
  

