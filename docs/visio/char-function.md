---
title: CHAR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251406
ms.localizationpriority: medium
ms.assetid: 0803d5d3-d804-5ffe-604d-661b35d1fc01
description: 数値の ANSI 文字を返します。
ms.openlocfilehash: 9e29a518f81a59fcf63313ef06391a4984944d81
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603754"
---
# <a name="char-function"></a>CHAR 関数

数値の ANSI 文字を返します。
  
## <a name="syntax"></a>構文

CHAR(** *number* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須かどうか  <br/> |**数値** <br/> |ANSI 文字を取得する番号。  <br/> |
   
## <a name="remarks"></a>注釈

結果の文字列の長さは 1 文字です。 number  _パラメーター_ は、1 ~ 255 の整数 (含む) である必要があります。または、関数はエラーを返します。 
  
## <a name="example"></a>例

CHAR(9) 
  
タブ文字を返します。 
  

