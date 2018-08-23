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
ms.openlocfilehash: 4112339d772248ac033674808d97c3f9c55b6f0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806192"
---
# <a name="replace-function-visioshapesheet"></a>REPLACE 関数 (VisioShapeSheet)

指定した文字の数に従って、テキスト文字列の一部を別のテキスト文字列に置き換えます。
  
## <a name="syntax"></a>構文

置換 (* **文字列** *、* **開始位置** *、* **文字** *、* **と** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _文字列_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |置き換えを行う文字列を指定します。  <br/> |
| _開始位置_ <br/> |必須  <br/> |**番号** <br/> |_置換文字列_と置き換える_文字列_の文字の位置。 文字列の最初の文字は、位置 1 です。  <br/> |
| _文字数_ <br/> |必須  <br/> |**番号** <br/> |置換する_文字列_の文字数  <br/> |
| _置換_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |このテキストは、_文字列_内の文字に置き換えられます。  <br/> |
   
### <a name="return-value"></a>戻り値

String
  
## <a name="remarks"></a>注釈

文字列内の特定の位置にある文字列を置換するときは、REPLACE 関数を使用します。文字列内の特定の文字列を置換するときは、SUBSTITUTE 関数を使用します。
  
## <a name="example"></a>例

REPLACE ("01/03/2002",9,2,"03") 
  
01/03/2003 を返します。 
  

