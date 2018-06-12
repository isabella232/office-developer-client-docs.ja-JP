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
ms.openlocfilehash: ca54b749b764e9ea2c7db71d41268303542417f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806030"
---
# <a name="playsound-function"></a>PLAYSOUND 関数

サウンド ファイルまたはシステム サウンドを再生します。 
  
## <a name="syntax"></a>構文

PLAYSOUND ("* **ファイル名** *"|"* **エイリアス** *"、* * *isAlias* * *、* **ビープ音が** *、* **同期** *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| filename <br/> |必須  <br/> |**文字列型 (String)** <br/> |再生するサウンド ファイルの名前を指定します。  <br/> |
| _エイリアス_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | エイリアスが示すシステム サウンドを指定します。  <br/> |
| _isAlias_ <br/> |必須  <br/> |**ブール型 (Boolean)** <br/> | 直前の式 (引数) がエイリアスまたはファイル名のどちらであるかを指定します。エイリアスを指定するには、ゼロ以外の値を使用します。  <br/> |
| _ビープ音_ <br/> |必須  <br/> |**ブール型 (Boolean)** <br/> |サウンドを再生できない場合にビープ音を鳴らすかどうかを指定します。ビープ音を鳴らすには、ゼロ以外の数値を使用します。  <br/> |
| _同期_ <br/> |必須  <br/> |**ブール型 (Boolean)** <br/> |非同期 (0) または同期 (1) のどちらでサウンドを再生するかを指定します。  <br/> |
   
## <a name="remarks"></a>注釈

Visio がサウンドを再生して処理を続行することができますようにサウンドを非同期的に再生する必要があります通常。 いくつかのサウンドは、同期的に、その再生、または一部を再生できない場合があります。 
  
## <a name="example-1"></a>例 1

PLAYSOUND("chord.wav", 0, 0, 0)
  
ウェーブ オーディオ ファイル chord.wav を非同期で実行し、警告のビープ音を鳴らしません。
  
## <a name="example-2"></a>例 2

PLAYSOUND("SystemExclamation", 1, 0, 0)
  
システムのメッセージ (警告) サウンドを非同期で実行し、警告のビープ音を鳴らしません。
  

