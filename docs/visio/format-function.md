---
title: FORMAT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251424
ms.localizationpriority: medium
ms.assetid: 52f5ef4d-07c6-ab36-bf74-b30b50eea221
description: 式の結果を、書式指定に従って書式設定された文字列として返します。
ms.openlocfilehash: bc5af650fdb4f5012963206f24a56d4bdd1c2592
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618946"
---
# <a name="format-function"></a>FORMAT 関数

式の結果を  _、書式_ に従って書式設定された文字列  _として返します_。
  
## <a name="syntax"></a>構文

FORMAT(** *expression* **," ** *formatpicture* ** ") 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須  <br/> |**String** <br/> |定数、演算子、関数、およびシェイプシートのセルに対する参照を組み合わせたもので、結果が値となる式です。  <br/> |
| _formatpicture_ <br/> |必須  <br/> |**String** <br/> |文字列を書式設定するための書式形式です。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

式の種類および書式形式で指定されている形式に応じて、返される文字列の書式が決まります。 _formatpicture は_、式の種類に適している必要があります。 書式画像の指定の詳細については、「書式画像について [」を参照してください](about-format-pictures.md)。
  
式の結果と、formatpictureで予期される型が異なる種類の場合、または _formatpicture_ に構文エラーがある場合にエラーを _返します_。
  
## <a name="example-1"></a>例 1

FORMAT(1cm/4, "0.000 u")
  
"0.250 cm" を返します。
  
## <a name="example-2"></a>例 2

FORMAT(1cm/4, "0.00 U")
  
"0.25 CM" を返します。
  
## <a name="example-3"></a>例 3

FORMAT(1cm/4, "0.0 u")
  
"0.3 cm" を返します。
  

