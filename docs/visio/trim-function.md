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
description: 単語間のスペースを 1 つ残して、テキストからすべての空白を削除します。
ms.openlocfilehash: b396572041e880451ceb1ec6f0508528c0807bfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806696"
---
# <a name="trim-function"></a>TRIM 関数

単語間のスペースを 1 つ残して、テキストからすべての空白を削除します。 
  
## <a name="syntax"></a>構文

トリミング (* **テキスト** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |空白を削除する文字列を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

String
  
## <a name="remarks"></a>注釈

他のアプリケーションから渡された文字列に無駄な空白が含まれているような場合に、TRIM 関数を使用します。
  
## <a name="example"></a>例

トリム (「2003 年 1 月 1日」) 
  
"January 1, 2003" を返します。 
  

