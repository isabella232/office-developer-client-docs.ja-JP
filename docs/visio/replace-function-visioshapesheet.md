---
title: REPLACE 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
ms.localizationpriority: medium
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: 指定した文字の数に従って、テキスト文字列の一部を別のテキスト文字列に置き換えます。
ms.openlocfilehash: 1288d18d148abc0e5bafe7fe855d140cc4e62d91
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554104"
---
# <a name="replace-function-visioshapesheet"></a>REPLACE 関数 (VisioShapeSheet)

指定した文字の数に従って、テキスト文字列の一部を別のテキスト文字列に置き換えます。
  
## <a name="syntax"></a>構文

REPLACE (** *old_text* **, ** *start_num* **, **** num_chars **, **** new_text ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _old_text_ <br/> |必須  <br/> |**String** <br/> |置き換えを行う文字列を指定します。  <br/> |
| _start_num_ <br/> |必須かどうか  <br/> |**数値** <br/> |置換する文字列内old_textの位置 _new_text。_ 文字列の最初の文字位置は、1 になります。  <br/> |
| _num_chars_ <br/> |必須かどうか  <br/> |**数値** <br/> |置換  _するold_text内_ の文字数  <br/> |
| _new_text_ <br/> |必須  <br/> |**String** <br/> |ファイル内の文字を置き _換えるold_text。_  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

文字列内の特定の位置にある文字列を置換するときは、REPLACE 関数を使用します。文字列内の特定の文字列を置換するときは、SUBSTITUTE 関数を使用します。
  
## <a name="example"></a>例

REPLACE ("01/03/2002",9,2,"03") 
  
01/03/2003 を返します。 
  

