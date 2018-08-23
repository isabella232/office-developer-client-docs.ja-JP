---
title: FORMAT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251424
localization_priority: Normal
ms.assetid: 52f5ef4d-07c6-ab36-bf74-b30b50eea221
description: Formatpicture に従って書式設定された文字列としての式の結果を返します。
ms.openlocfilehash: dcb898b3cb21d8cc5ebee7e56540d9e2eefcffdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805444"
---
# <a name="format-function"></a>FORMAT 関数

_Formatpicture_に従って書式設定された文字列としての_式_の結果を返します。
  
## <a name="syntax"></a>構文

形式 (* **式** *、"* * *formatpicture* * *") 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |定数、演算子、関数、およびシェイプシートのセルに対する参照を組み合わせたもので、結果が値となる式です。  <br/> |
| _formatpicture_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |文字列を書式設定するための書式形式です。  <br/> |
   
### <a name="return-value"></a>戻り値

String
  
## <a name="remarks"></a>注釈

式の型と、図の書式設定で指定された型は、返される文字列の動作を制御します。 _Formatpicture_は、式のタイプに対応する必要があります。 書式形式を指定する方法の詳細については、[書式形式について](about-format-pictures.md)を参照してください。
  
_式_と_formatpicture_での型の結果は、異なる種類の場合、または_formatpicture_で構文エラーがある場合は、エラーを返します。
  
## <a name="example-1"></a>例 1

FORMAT(1cm/4, "0.000 u")
  
"0.250 cm" を返します。
  
## <a name="example-2"></a>例 2

FORMAT(1cm/4, "0.00 U")
  
"0.25 CM" を返します。
  
## <a name="example-3"></a>例 3

FORMAT(1cm/4, "0.0 u")
  
"0.3 cm" を返します。
  

