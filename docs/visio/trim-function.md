---
title: TRIM 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027318
ms.localizationpriority: medium
ms.assetid: 6f2d84fd-27eb-4c2f-a2e1-43d20e0c78be
description: 単語間の 1 つのスペースを除き、テキストからすべての領域を削除します。
ms.openlocfilehash: e6d8263585754db88a1500a5fbe20a56ef4fe633
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627262"
---
# <a name="trim-function"></a>TRIM 関数

単語間の 1 つのスペースを除き、テキストからすべての領域を削除します。 
  
## <a name="syntax"></a>構文

TRIM (** *text* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |必須  <br/> |**String** <br/> |空白を削除する文字列を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

他のアプリケーションから渡された文字列に無駄な空白が含まれているような場合に、TRIM 関数を使用します。
  
## <a name="example"></a>例

TRIM ("2003 年 1 月 1 日 ") 
  
"January 1, 2003" を返します。 
  

