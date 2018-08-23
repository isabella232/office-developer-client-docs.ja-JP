---
title: FIELDPICTURE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251592
localization_priority: Normal
ms.assetid: df88c55f-c098-dd4c-bf53-c7d7b60cf719
description: Microsoft Visio の内部のテキスト フィールドの表示形式コードに一致する図の書式設定文字列を返します。
ms.openlocfilehash: 1528cefd65ed0c7c1dde02fa390babf26442b4d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805351"
---
# <a name="fieldpicture-function"></a>FIELDPICTURE 関数

Microsoft Visio の内部のテキスト フィールドの表示形式コードに一致する図の書式設定文字列を返します。
  
## <a name="syntax"></a>構文

FIELDPICTURE (* **コード** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _code_ <br/> |必須  <br/> |**番号** <br/> | テキスト フィールドの書式設定コードを指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

String
  
## <a name="remarks"></a>注釈

日付、時刻、数値、および単位ラベルに対応した値を定義するには、FORMAT 関数で書式形式の文字列を使用します。
  
## <a name="example"></a>例

FIELDPICTURE(0) 
  
書式形式の文字列 "esc(0)" を返します。この文字列を FORMAT 関数で使用する場合、小数点以下 1 位までと小文字の単位を含む数値を指定することになります。 
  

