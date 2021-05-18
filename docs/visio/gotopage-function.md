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
description: 現在アクティブなウィンドウに名前のページ名を持つページを表示します。
ms.openlocfilehash: c96585406b6104aeedbe46c35024a4f13bb0953e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302969"
---
# <a name="gotopage-function"></a>GOTOPAGE 関数

現在アクティブなウィンドウに名前  *のページ名*  を持つページを表示します。 
  
## <a name="syntax"></a>構文

GOTOPAGE(" ** *pagename* ** ") 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _pagename_ <br/> |必須  <br/> |**String** <br/> |移動先のページの名前を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

ウィンドウに既にそのページが表示されている場合、そのウィンドウがアクティブになります。 pagename  *が存在*  しない場合、アプリケーションはページ名 /に移動 https://  *移動します*  。 Visio が埋め込み先サーバーとして機能している場合は、GOTOPAGE 関数は無効になります。 
  
DOS、UNC、または URL のパスに従って移動するには、HYPERLINK 関数を使用します。 
  
以前のバージョンの Visio 製品では、この関数は _GOTOPAGE に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。 
  

