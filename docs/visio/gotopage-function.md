---
title: GOTOPAGE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251432
localization_priority: Normal
ms.assetid: b131badf-1656-132e-0aae-eeedb917ba7a
description: 現在作業中のウィンドウで名前の指定した pagename を持つページが表示されます。
ms.openlocfilehash: 67f8a79b854fd6f2ae47e39877ffcdbe4a1be5cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805494"
---
# <a name="gotopage-function"></a>GOTOPAGE 関数

現在作業中のウィンドウで名前の*指定した pagename*を持つページが表示されます。 
  
## <a name="syntax"></a>構文

GOTOPAGE ("* **指定した pagename* * *") 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _pagename_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |移動先のページの名前を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

ウィンドウには、既にページが表示されて、そのウィンドウがアクティブになります。 アプリケーションが http://*指定した pagename*に移動しようとした*pagename*が存在しない場合とします。 Visio が埋め込み先サーバーとして動作している場合は、GOTOPAGE 関数に影響はありません。 
  
DOS、UNC、または URL のパスに従って移動するには、HYPERLINK 関数を使用します。 
  
以前のバージョンの Visio 製品では、この関数は _GOTOPAGE に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。 
  

