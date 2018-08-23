---
title: DOOLEVERB 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251421
localization_priority: Normal
ms.assetid: d276c122-6326-75a7-220c-6a78e94e0db0
description: OLE オブジェクトの動詞を実行します。
ms.openlocfilehash: a7786c3ef2b4039e288596ed367083a4ed3a6c13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805261"
---
# <a name="dooleverb-function"></a>DOOLEVERB 関数

OLE オブジェクトの動詞を実行します。
  
## <a name="syntax"></a>構文

DOOLEVERB ("* **動詞** *") 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _「動詞」_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |実行する動詞を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

以前のバージョンの Visio では、この関数は _DOOLEVERB に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。 
  
## <a name="example"></a>例

DOOLEVERB("edit")
  
OLE オブジェクト プログラムを実行し、リンクされた、または埋め込まれているオブジェクトを表示して編集できるようにします。
  

