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
description: 行パターン、塗りつぶしパターン、または LinePattern、FillPattern、BeginArrow、または [endarrow] セルに格納するときの図形に名前と呼ばれる線の端点を適用します。
ms.openlocfilehash: 0b6668e57a8f997a69fece51cbc5bd1b1574a576
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806732"
---
# <a name="use-function"></a>USE 関数

行パターン、塗りつぶしパターン、または LinePattern、FillPattern、BeginArrow、または [endarrow] セルに格納するときの図形に_名前_と呼ばれる線の端点を適用します。 
  
## <a name="syntax"></a>構文

使用 ("* **名前** *") 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _name_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |有効なマスター シェイプの名前である、任意の文字列を指定します。  <br/> |
   
### <a name="return-value"></a>�߂�l

数値
  
## <a name="remarks"></a>備考

_Name_という名前のマスター ドキュメントの図面ステンシル上にある場合は、行パターン、塗りつぶしパターン、矢印の始点、または矢印の終点でパターンが適用されます。 
  
この関数は常に 254 を返します。
  
## <a name="example"></a>例

USE("線路") 
  
"線路" という名のマスター シェイプのパターンを、数式が含まれる図形に適用することにより、図形を書式設定します。 
  

