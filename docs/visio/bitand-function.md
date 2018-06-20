---
title: BITAND 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251398
localization_priority: Normal
ms.assetid: c437de23-d2e0-469d-62e6-8eb8b8cfea5c
description: Binarynumber1 と binarynumber2 の両方に対応するビットが 1 である場合にのみでは、各ビットを 1 に設定するように 16 ビットのバイナリ数値を返します。 それ以外の場合、ビットが 0 に設定されています。
ms.openlocfilehash: 0b501bb383596e3f2f39ea14f2cb9eb4bf40b25b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804873"
---
# <a name="bitand-function"></a>BITAND 関数

Binarynumber1 と binarynumber2 の両方に対応するビットが 1 である場合にのみでは、各ビットを 1 に設定するように 16 ビットのバイナリ数値を返します。 それ以外の場合、ビットが 0 に設定されています。 
  
## <a name="syntax"></a>構文

BITAND (* * *binarynumber1* * *、* * *binarynumber2* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _バイナリの数値 1_ <br/> |必須  <br/> |**数値** <br/> |最初の 16 ビットのバイナリ数値を指定します。  <br/> |
| _バイナリ数値 2_ <br/> |必須  <br/> |**数値** <br/> |2 番目の 16 ビットのバイナリ数値を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

この関数を使用して、ビットマスクとして保存されている図形のプロパティ (図形の文字書式など) をテストしたり、変更したりできます。
  
## <a name="example"></a>例

BITAND(12,6)
  
4 を返します。12 = 0...01100、6 = 0...00110 であり、したがって BITAND(12,6) = 0...00100 となります。
  

