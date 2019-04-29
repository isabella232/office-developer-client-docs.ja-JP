---
title: REPLACE 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
localization_priority: Normal
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: 指定した文字の数に従って、テキスト文字列の一部を別のテキスト文字列に置き換えます。
ms.openlocfilehash: 75a156d720ca276e75fccf932124ae905e4350b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414355"
---
# <a name="replace-function-visioshapesheet"></a>REPLACE 関数 (VisioShapeSheet)

指定した文字の数に従って、テキスト文字列の一部を別のテキスト文字列に置き換えます。
  
## <a name="syntax"></a>構文

REPLACE (* **文字列** *、* **開始位置** *、* ** * 文字数 * *、* **置換** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _文字列_ <br/> |必須  <br/> |**String** <br/> |置き換えを行う文字列を指定します。  <br/> |
| _開始_ <br/> |必須  <br/> |**数値** <br/> |置換する文字列の文字の__ 位置を指定します。 __ 文字列の最初の文字位置は、1 になります。  <br/> |
| _文字数_ <br/> |必須  <br/> |**数値** <br/> |置換する_文字列_の文字数を指定します。  <br/> |
| _文字列_ <br/> |必須  <br/> |**String** <br/> |文字列を置換する文字列を入力__ します。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

文字列内の特定の位置にある文字列を置換するときは、REPLACE 関数を使用します。文字列内の特定の文字列を置換するときは、SUBSTITUTE 関数を使用します。
  
## <a name="example"></a>例

REPLACE ("01/03/2002",9,2,"03") 
  
01/03/2003 を返します。 
  

