---
title: DOOLEVERB 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251421
ms.localizationpriority: medium
ms.assetid: d276c122-6326-75a7-220c-6a78e94e0db0
description: OLE オブジェクトの動詞を実行します。
ms.openlocfilehash: 93f69735dbf1d2ae31f0d8c33306c422ecafbfb7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590283"
---
# <a name="dooleverb-function"></a>DOOLEVERB 関数

OLE オブジェクトの動詞を実行します。
  
## <a name="syntax"></a>構文

DOOLEVERB(" ** *verb* ** ") 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _"verb"_ <br/> |必須  <br/> |**String** <br/> |実行する動詞を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

以前のバージョンの Visio では、この関数は _DOOLEVERB に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。 
  
## <a name="example"></a>例

DOOLEVERB("edit")
  
OLE オブジェクト プログラムを実行し、リンクされた、または埋め込まれているオブジェクトを表示して編集できるようにします。
  

