---
title: RUNADDONWARGS 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251493
ms.localizationpriority: medium
ms.assetid: c154413f-c366-a66b-94e3-ed71ad23f325
description: 文字列を実行し、コマンド ラインの引数を文字列としてプログラムに渡します。
ms.openlocfilehash: 34de0d5024e761e9f8f0b4c39d3ed70e717a789e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573405"
---
# <a name="runaddonwargs-function"></a>RUNADDONWARGS 関数

文字列  _を実行_ し、コマンド ラインの  _引数を文字列_ としてプログラムに渡します。 
  
## <a name="syntax"></a>構文

RUNADDONWARGS(" ** *string* ** "," ** *arguments* ** ") 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |必須  <br/> |**String** <br/> | アドオンの名前を指定します。  <br/> |
| _arguments_ <br/> |必須  <br/> |**String** <br/> |ユーザーのプログラムに渡す引数を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

実際には、  _引数は_ 50 文字以下である必要があります。 たとえば [Action] や [Events] などのセルにアドオンなどのプログラムをバインドする場合に、RUNADDONWARGS 関数を使用します。 
  
RUNADDONWARGS 関数は、アプリケーションの **Addons** コレクションのメンバーであるアドオンのみ実行できます。このコレクションのメンバーになるためには、アドオンの EXE ファイルまたは VSL ファイルが次の条件を満たしている必要があります。 
  
- アプリケーションの Startup パスまたは Addons パスにインストールされている。 
    
- **Addons** コレクションの **Add** メソッドを使用してプログラムから追加されている。 
    
Visio でのコードの実行に関する詳細については、この『シェイプシート リファレンス』の「[Visio のセキュリティ設定とコードの実行について](about-security-settings-and-running-code-in-visio-shapesheet.md)」を参照してください。 
  
以前のバージョンの Visio では、この関数は _RUNADDONWARGS に相当します。Visio アプリケーション バージョン 4.0 以降では、どちらのスタイルも使用できます。
  
## <a name="example"></a>例

RUNADDONWARGS("GRAPHMKR.EXE","/GraphMaker=Stack") 
  
アドオン Graphmkr.exe を起動し、これに引数 /GraphMaker=Stack を渡します。 
  

