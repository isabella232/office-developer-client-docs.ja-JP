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
description: サウンドファイルまたはシステムサウンドを再生します。
ms.openlocfilehash: 752412aab6584d2b01235fe88644e3ec3fa5daee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346845"
---
# <a name="playsound-function"></a>PLAYSOUND 関数

サウンドファイルまたはシステムサウンドを再生します。 
  
## <a name="syntax"></a>構文

PLAYSOUND ("* * *filename* * *" | "* **エイリアス** *", * * *isalias* * *, * * *beep* * *, * * *synch* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _filename_ <br/> |必須  <br/> |**String** <br/> |再生するサウンド ファイルの名前を指定します。  <br/> |
| _alias_ <br/> |必須  <br/> |**String** <br/> | エイリアスが示すシステム サウンドを指定します。  <br/> |
| _isalias_ <br/> |必須  <br/> |**Boolean** <br/> | 直前の式 (引数) がエイリアスまたはファイル名のどちらであるかを指定します。エイリアスを指定するには、ゼロ以外の値を使用します。  <br/> |
| _鳴り_ <br/> |必須  <br/> |**Boolean** <br/> |サウンドを再生できない場合にビープ音を鳴らすかどうかを指定します。ビープ音を鳴らすには、ゼロ以外の数値を使用します。  <br/> |
| _とれ_ <br/> |必須  <br/> |**Boolean** <br/> |非同期 (0) または同期 (1) のどちらでサウンドを再生するかを指定します。  <br/> |
   
## <a name="remarks"></a>解説

通常、サウンドを再生している間に Visio が処理を続行できるように、サウンドを非同期で再生する必要があります。 複数のサウンドを文字列でつなぎ合わせるには、それらを同時に再生するか、再生に失敗することがあります。 
  
## <a name="example-1"></a>例 1

PLAYSOUND("chord.wav", 0, 0, 0)
  
ウェーブ オーディオ ファイル chord.wav を非同期で実行し、警告のビープ音を鳴らしません。
  
## <a name="example-2"></a>例 2

PLAYSOUND("SystemExclamation", 1, 0, 0)
  
システムのメッセージ (警告) サウンドを非同期で実行し、警告のビープ音を鳴らしません。
  

