---
title: PATHSEGMENT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: 指定したパスに沿って指定した割合のマークで 1 ベースのセグメント数を返します。
ms.openlocfilehash: b25f43ffa3c719cfc5ffbd1e417f2da9640e483b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805986"
---
# <a name="pathsegment-function"></a>PATHSEGMENT 関数

指定したパスに沿って指定した割合のマークで 1 ベースのセグメント数を返します。
  
## <a name="syntax"></a>構文

PATHSEGMENT (* **で** *、* **旅行** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。  <br/> |
| _旅行_ <br/> |必須  <br/> |**Double** <br/> |スキャンするパスの始点から終点までの割合。0 ～ 1 の値を指定する必要があります。  <br/> |
   
### <a name="return-value"></a>戻り値

整数型 (Integer)
  

