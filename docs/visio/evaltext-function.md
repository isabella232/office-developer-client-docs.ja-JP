---
title: EVALTEXT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251422
localization_priority: Normal
ms.assetid: c9b5b96c-d8c8-6119-e3f1-a2ce9d7c043e
description: および結果を返す数式をされたかのようになります内のテキストを評価します。
ms.openlocfilehash: 69e79a23faa9d09aa2ad51f83363064b54742152
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805327"
---
# <a name="evaltext-function"></a>EVALTEXT 関数

および結果を返す数式をされたかのように_なります_内のテキストを評価します。 
  
## <a name="syntax"></a>構文

EVALTEXT (* **なります! テキスト** *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _なります! テキスト_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |関連付けられている図形のテキスト構成が変更されたときにトリガーされるセルを指定します。  <br/> |
   
### <a name="return-value"></a>�߂�l

String
  
## <a name="remarks"></a>Remarks

 _なります_は、現在の図形以外の図形のテキストを参照するために使用できます。 
  
テキストがない場合、結果はゼロになります。テキストを評価できない場合、関数はエラーを返します。
  
## <a name="example"></a>例

EVALTEXT(Line.2!theText) 
  
[線 2] 図形に含まれているテキストを評価します。たとえば、[線 2] に "4 ft + 0.5 ft" が含まれている場合、値 4.5 ft を返します。 
  

