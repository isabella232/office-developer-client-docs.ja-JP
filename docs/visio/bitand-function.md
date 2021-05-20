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
description: binarynumber1 と binarynumber2 の両方の対応するビットが 1 の場合にのみ、各ビットを 1 に設定する 16 ビットのバイナリ番号を返します。 それ以外の場合、ビットは 0 に設定されます。
ms.openlocfilehash: a3c76a9122d0f02d5ab61460cf3457bb15da4d7b
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293493"
---
# <a name="bitand-function"></a>BITAND 関数

binarynumber1 と binarynumber2 の両方の対応するビットが 1 の場合にのみ、各ビットを 1 に設定する 16 ビットのバイナリ番号を返します。 それ以外の場合、ビットは 0 に設定されます。 
  
## <a name="syntax"></a>構文

BITAND(***binarynumber1***, ***binarynumber2*** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _バイナリ番号 1_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |最初の 16 ビットのバイナリ数値を指定します。  <br/> |
| _バイナリ番号 2_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |2 番目の 16 ビットのバイナリ数値を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

この関数を使用して、ビットマスクとして保存されている図形のプロパティ (図形の文字書式など) をテストしたり、変更したりできます。
  
## <a name="example"></a>例

BITAND(12,6)
  
4 を返します。12 = 0...01100、6 = 0...00110 であり、したがって BITAND(12,6) = 0...00100 となります。
  

