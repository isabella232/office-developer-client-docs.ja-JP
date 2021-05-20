---
title: PLAYSOUND 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251479
localization_priority: Normal
ms.assetid: 098d216f-e699-0e74-f702-ccfa7809c19b
description: サウンド ファイルまたはシステム サウンドを再生します。
ms.openlocfilehash: 752412aab6584d2b01235fe88644e3ec3fa5daee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435840"
---
# <a name="playsound-function"></a>PLAYSOUND 関数

サウンド ファイルまたはシステム サウンドを再生します。 
  
## <a name="syntax"></a>構文

PLAYSOUND(" ** *filename* ** "|" ** *alias* ** ", ** *isAlias* **, ** *beep* **, ** *synch* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _filename_ <br/> |必須  <br/> |**String** <br/> |再生するサウンド ファイルの名前を指定します。  <br/> |
| _alias_ <br/> |必須  <br/> |**String** <br/> | エイリアスが示すシステム サウンドを指定します。  <br/> |
| _isAlias_ <br/> |必須  <br/> |**Boolean** <br/> | 直前の式 (引数) がエイリアスまたはファイル名のどちらであるかを指定します。エイリアスを指定するには、ゼロ以外の値を使用します。  <br/> |
| _ビープ音_ <br/> |必須  <br/> |**Boolean** <br/> |サウンドを再生できない場合にビープ音を鳴らすかどうかを指定します。ビープ音を鳴らすには、ゼロ以外の数値を使用します。  <br/> |
| _synch_ <br/> |必須  <br/> |**Boolean** <br/> |非同期 (0) または同期 (1) のどちらでサウンドを再生するかを指定します。  <br/> |
   
## <a name="remarks"></a>注釈

サウンド再生中に Visio が処理を続行できるようにするため、通常はサウンドを非同期で再生する必要があります。複数のサウンドを続けて再生するには、同期で再生します。同期で再生しないと、一部のサウンドが再生できない場合があります。
 
  
## <a name="example-1"></a>例 1

PLAYSOUND("chord.wav", 0, 0, 0)
  
ウェーブ オーディオ ファイル chord.wav を非同期で実行し、警告のビープ音を鳴らしません。
  
## <a name="example-2"></a>例 2

PLAYSOUND("SystemExclamation", 1, 0, 0)
  
システムのメッセージ (警告) サウンドを非同期で実行し、警告のビープ音を鳴らしません。
  

