---
title: TRIM 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027318
localization_priority: Normal
ms.assetid: 6f2d84fd-27eb-4c2f-a2e1-43d20e0c78be
description: 単語間のスペースを除くすべてのスペースをテキストから削除します。
ms.openlocfilehash: b947c9500012d0ceefe3e8044be387f7b810dda9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280844"
---
# <a name="trim-function"></a>TRIM 関数

単語間のスペースを除くすべてのスペースをテキストから削除します。 
  
## <a name="syntax"></a>構文

TRIM (* * *text* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |必須  <br/> |**String** <br/> |空白を削除する文字列を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

他のアプリケーションから渡された文字列に無駄な空白が含まれているような場合に、TRIM 関数を使用します。
  
## <a name="example"></a>例

TRIM ("January 1, 2003") 
  
"January 1, 2003" を返します。 
  

