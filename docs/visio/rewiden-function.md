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
description: 指定した文字セットを使用して、16 ビット Unicode 文字コードの文字列に拡張されたシングル バイトまたはマルチバイト文字セット コードは、16 ビットの文字コードを生成する数式に変換します。
ms.openlocfilehash: 66dc3e801585077a9521cd93f8ae78c47f8a746b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806239"
---
# <a name="rewiden-function"></a>REWIDEN 関数

指定した文字セットを使用して、16 ビット Unicode 文字コードの文字列に拡張されたシングル バイトまたはマルチバイト文字セット コードは、16 ビットの文字コードを生成する数式に変換します。 
  
## <a name="syntax"></a>構文

REWIDEN (* * *srcCharSet* * *、* * *dstCharSet* * *、* **テキスト** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _srcCharSet_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |変換前の図面の文字セットを指定します。  <br/> |
| _dstCharSet_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | 変換後の図面の文字セットを指定します。  <br/> |
| _text_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |変換するテキストを指定します。  <br/> |
   
## <a name="remarks"></a>注釈

REWIDEN 関数は、Visio 2002 の図面から Visio 2003 の図面への自動変換に使用されます。それ以外の使用はお勧めしません。
  

