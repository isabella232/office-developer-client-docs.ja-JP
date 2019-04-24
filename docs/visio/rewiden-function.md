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
description: 指定した文字セットを使用して、拡張されたシングルバイトまたはマルチバイト文字セットコードの16ビット文字コードを生成する数式を、16ビットの Unicode 文字コードの文字列に変換します。
ms.openlocfilehash: c885487f91e541027b7ba09812e7321a9deb00ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326769"
---
# <a name="rewiden-function"></a>REWIDEN 関数

指定した文字セットを使用して、拡張されたシングルバイトまたはマルチバイト文字セットコードの16ビット文字コードを生成する数式を、16ビットの Unicode 文字コードの文字列に変換します。 
  
## <a name="syntax"></a>構文

再拡大 (* * *srccharset* * *、* * *dstcharset* * *、* * *text* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _srccharset_ <br/> |必須  <br/> |**String** <br/> |変換前の図面の文字セットを指定します。  <br/> |
| _dstcharset_ <br/> |必須  <br/> |**String** <br/> | 変換後の図面の文字セットを指定します。  <br/> |
| _text_ <br/> |必須  <br/> |**String** <br/> |変換するテキストを指定します。  <br/> |
   
## <a name="remarks"></a>解説

REWIDEN 関数は、Visio 2002 の図面から Visio 2003 の図面への自動変換に使用されます。それ以外の使用はお勧めしません。
  

