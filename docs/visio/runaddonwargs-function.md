---
title: RUNADDONWARGS 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251493
localization_priority: Normal
ms.assetid: c154413f-c366-a66b-94e3-ed71ad23f325
description: 文字列を実行し、コマンドライン引数を文字列としてプログラムに渡します。
ms.openlocfilehash: 7bc05a0cbf32550d1e39bee39bec83101882cf19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806339"
---
# <a name="runaddonwargs-function"></a>RUNADDONWARGS 関数

_文字列_を実行し、コマンド ・ ライン_引数_を文字列としてプログラムに渡します。 
  
## <a name="syntax"></a>構文

RUNADDONWARGS ("* **文字列** *","* **引数** *") 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | アドオンの名前を指定します。  <br/> |
| _arguments_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |ユーザーのプログラムに渡す引数を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

実際には、_引数_は 50 文字以下にする必要があります。 RUNADDONWARGS 関数を使用すると、アクションまたはイベント セル、セルに、アドオンなどのプログラムをバインドします。 
  
RUNADDONWARGS 関数は、アプリケーションの**Addons**コレクションのメンバーであるアドオンのみ実行できます。 そのコレクション内に存在するには、アドオンは EXE ファイルまたは VSL ファイルである必要があります。 
  
- アプリケーションの**起動時**または**アドオン**のパスにインストールされます。 
    
- **Addons**コレクションの**Add**メソッドを使用してプログラムを使用して追加します。 
    
Visio のコードの実行の詳細について[セキュリティ設定について、Visio でのコードの実行](about-security-settings-and-running-code-in-visio-shapesheet.md)でこの「シェイプ シート リファレンスを参照してください。 
  
以前のバージョンの Visio では、この関数は _RUNADDONWARGS に相当します。Visio アプリケーション バージョン 4.0 以降では、どちらのスタイルも使用できます。
  
## <a name="example"></a>例

RUNADDONWARGS ("GRAPHMKR。EXE"、"/GraphMaker = スタック」) 
  
アドオン Graphmkr.exe を起動し、これに引数 /GraphMaker=Stack を渡します。 
  

