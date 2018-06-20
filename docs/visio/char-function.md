---
title: CHAR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251406
localization_priority: Normal
ms.assetid: 0803d5d3-d804-5ffe-604d-661b35d1fc01
description: いくつかの ANSI 文字を返します。
ms.openlocfilehash: 209614d20dd663ed2f7ca030c25500d43f925c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804987"
---
# <a name="char-function"></a>CHAR 関数

いくつかの ANSI 文字を返します。
  
## <a name="syntax"></a>構文

文字 (* **番号** *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**番号** <br/> |取得する ANSI 文字の数です。  <br/> |
   
## <a name="remarks"></a>備考

結果の文字列は、1 つの文字の長さです。 _数_パラメーターは 1 から 255 まで (両端を含む) の間の整数である必要がありますか、エラーを返します。 
  
## <a name="example"></a>例

CHAR(9) 
  
タブ文字を返します。 
  

