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
description: 式の結果を formatpicture に従って書式設定された文字列として返します。
ms.openlocfilehash: 5eb2195c2bc52e9cc8e7aa8bc4068826a5cd14c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339894"
---
# <a name="format-function"></a>FORMAT 関数

_式_の結果を_formatpicture_に従って書式設定された文字列として返します。
  
## <a name="syntax"></a>構文

FORMAT (* **式** *、"* * *formatpicture* * *") 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須  <br/> |**String** <br/> |定数、演算子、関数、およびシェイプシートのセルに対する参照を組み合わせたもので、結果が値となる式です。  <br/> |
| _formatpicture_ <br/> |必須  <br/> |**String** <br/> |文字列を書式設定するための書式形式です。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

式の種類および書式形式で指定されている形式に応じて、返される文字列の書式が決まります。 _formatpicture_は、式の種類に適している必要があります。 書式設定画像の指定の詳細については、「 [format pictures](about-format-pictures.md)」を参照してください。
  
_式_の結果と_formatpicture_で想定される種類が異なる場合、または_formatpicture_に構文エラーがある場合は、エラーを返します。
  
## <a name="example-1"></a>例 1

FORMAT(1cm/4, "0.000 u")
  
"0.250 cm" を返します。
  
## <a name="example-2"></a>例 2

FORMAT(1cm/4, "0.00 U")
  
"0.25 CM" を返します。
  
## <a name="example-3"></a>例 3

FORMAT(1cm/4, "0.0 u")
  
"0.3 cm" を返します。
  

