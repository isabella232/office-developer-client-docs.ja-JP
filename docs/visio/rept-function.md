---
title: REPT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027335
localization_priority: Normal
ms.assetid: 53362a32-ac27-42a3-ace1-c6184ab20b52
description: テキストを指定した回数だけ繰り返されます。
ms.openlocfilehash: 761f2f95824d5bdab4995b2867bfeac6be64bc12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806251"
---
# <a name="rept-function"></a>REPT 関数

テキストを指定した回数だけ繰り返されます。 
  
## <a name="syntax"></a>構文

REPT (* **テキスト** *、* **繰り返し** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | 繰り返す文字列を指定します。  <br/> |
| _繰り返し回数_ <br/> |必須  <br/> |**番号** <br/> |文字列の繰り返す回数を、正の数値で指定します。  <br/> |
   
## <a name="remarks"></a>注釈

場合は、*繰り返し回数*は、次のとおりです。 
  
- number_times がゼロ (0) の場合、"" (空文字列) を返します。
    
- number_times が整数でない場合、小数点以下は切り捨てられます。
    
## <a name="example"></a>例

REPT ("\*", 5) 
  
返します。 \* \* \* \* \*。 
  

