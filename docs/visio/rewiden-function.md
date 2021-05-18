---
title: REWIDEN 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033808
localization_priority: Normal
ms.assetid: c20842cd-86b1-83fa-49ba-118936013b6f
description: 指定した文字セットを使用して、1 バイトまたはマルチバイトの文字セット コードを拡大した 16 ビット文字コードを生成する数式を 16 ビット Unicode 文字コードの文字列に変換します。
ms.openlocfilehash: c885487f91e541027b7ba09812e7321a9deb00ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405213"
---
# <a name="rewiden-function"></a>REWIDEN 関数

指定した文字セットを使用して、1 バイトまたはマルチバイトの文字セット コードを拡大した 16 ビット文字コードを生成する数式を 16 ビット Unicode 文字コードの文字列に変換します。 
  
## <a name="syntax"></a>構文

REWIDEN(** *srcCharSet* **, ** *dstCharSet* **, ** *text* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _srcCharSet_ <br/> |必須  <br/> |**String** <br/> |変換前の図面の文字セットを指定します。  <br/> |
| _dstCharSet_ <br/> |必須  <br/> |**String** <br/> | 変換後の図面の文字セットを指定します。  <br/> |
| _text_ <br/> |必須  <br/> |**String** <br/> |変換するテキストを指定します。  <br/> |
   
## <a name="remarks"></a>注釈

REWIDEN 関数は、Visio 2002 の図面から Visio 2003 の図面への自動変換に使用されます。それ以外の使用はお勧めしません。
  

