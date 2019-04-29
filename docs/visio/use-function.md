---
title: USE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251510
localization_priority: Normal
ms.assetid: 410c4187-21f3-d959-750e-9dc6095fba9a
description: '[linepattern]、[fillpattern]、[beginarrow]、または [endarrow] セルに配置されたときに、name という名前の線パターン、塗りつぶしパターン、または線の端点を図形に適用します。'
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422825"
---
# <a name="use-function"></a>USE 関数

[linepattern]、[fillpattern]、[beginarrow]、または [endarrow] セルに配置されたときに、name という_名前_の線パターン、塗りつぶしパターン、または線の端点を図形に適用します。 
  
## <a name="syntax"></a>構文

USE ("* * *name* * *") 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _name_ <br/> |必須  <br/> |**String** <br/> |有効なマスター シェイプの名前である、任意の文字列を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

数値
  
## <a name="remarks"></a>注釈

_名前_が付けられたマスターシェイプが文書のステンシルにある場合、パターンは、線のパターン、塗りつぶしのパターン、矢印の始点、または終点の矢印として適用されます。 
  
この関数は常に 254 を返します。
  
## <a name="example"></a>例

USE("線路") 
  
"線路" という名のマスター シェイプのパターンを、数式が含まれる図形に適用することにより、図形を書式設定します。 
  

