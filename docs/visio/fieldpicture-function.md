---
title: FIELDPICTURE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251592
ms.localizationpriority: medium
ms.assetid: df88c55f-c098-dd4c-bf53-c7d7b60cf719
description: 内部テキスト フィールドの書式コードに一致する書式Visio文字列を返します。
ms.openlocfilehash: 1240386f38945dd7ede35f083ed4be87f75f5d81
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619016"
---
# <a name="fieldpicture-function"></a>FIELDPICTURE 関数

内部テキスト フィールドの書式コードに一致する書式Visio文字列を返します。
  
## <a name="syntax"></a>構文

FIELDPICTURE(** *code* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _code_ <br/> |必須かどうか  <br/> |**数値** <br/> | テキスト フィールドの書式設定コードを指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

日付、時刻、数値、および単位ラベルに対応した値を定義するには、FORMAT 関数で書式形式の文字列を使用します。
  
## <a name="example"></a>例

FIELDPICTURE(0) 
  
書式形式の文字列 "esc(0)" を返します。この文字列を FORMAT 関数で使用する場合、小数点以下 1 位までと小文字の単位を含む数値を指定することになります。 
  

