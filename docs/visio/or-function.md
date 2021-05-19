---
title: OR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251476
localization_priority: Normal
ms.assetid: 6c2154fa-4190-0699-61f7-f2bdf87173ec
description: パラメーターとして渡される論理式が TRUE の場合は、TRUE (1) を返します。
ms.openlocfilehash: 175a1c72f5109caca786b823966f07836f4737f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433508"
---
# <a name="or-function"></a>OR 関数

パラメーターとして渡される論理式が TRUE の場合は、TRUE (1) を返します。
  
## <a name="syntax"></a>構文

OR(** *logicalexpression1* **, ** *logicalexpression2 **,...,* ** *logicalexpressionN* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _logicalexpression1_ <br/> |必須  <br/> |**String** <br/> |真を評価する最初の式を指定します。  <br/> |
| _logicalexpression2_ <br/> |必須  <br/> |**String** <br/> |真を評価する 2 番目の式を指定します。  <br/> |
| _logicalexpressionN_ <br/> |必須  <br/> |**String** <br/> |真を評価する n 番目の式を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

Boolean
  
## <a name="remarks"></a>注釈

いずれかの式がゼロ以外の値に評価される場合は、TRUE と見なされます。すべての論理式が FALSE または 0 の場合に、この関数は FALSE を返します。 
  
## <a name="example"></a>例

OR(Height \> 1,PinX \> 1) 
  
どちらかの式が TRUE の場合、TRUE (1) を返します。両方の式が FALSE の場合にのみ、FALSE (0) を返します。 
  

