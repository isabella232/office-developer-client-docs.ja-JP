---
title: OPENFILE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251471
localization_priority: Normal
ms.assetid: ff59ab04-a589-cf9e-db3b-20658a7dffdc
description: ドキュメント ウィンドウがアクティブになりますが既に開いていない場合は、Microsoft Visio の図面を開きます。
ms.openlocfilehash: 7d4778fc4641465e88303b8515365172fd8be0ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805942"
---
# <a name="openfile-function"></a>OPENFILE 関数

ドキュメント ウィンドウがアクティブになりますが既に開いていない場合は、Microsoft Visio の図面を開きます。
  
## <a name="syntax"></a>構文

 **OPENFILE**(_ファイル名_)
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| filename <br/> |必須  <br/> |**文字列型 (String)** <br/> |開くには必要なファイルのパスを含むファイルの名前です。  <br/> |
   
## <a name="remarks"></a>注釈

複数の OPENFILE 関数を呼び出すと待ち行列に入り、評価する順序に従って実行されます。視覚的な編集ができるように、現在の Visio 図面をアクティブにすると (埋め込み先編集モード)、新しい Visio インスタンスが要求されたファイル名で起動されます。 
  
この関数は常に FALSE を返します。 
  
以前のバージョンの Visio アプリケーションでは、この関数は _OPENFILE に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。 
  
## <a name="example"></a>例

 `OPENFILE("C:/MyFile.vsdx")`
  
新しいウィンドウで、指定されたファイル"MyFile.vsdx"を開くか、ファイルが既に開いている場合にウィンドウを表示します。 
  

