---
title: SETATREFEVAL 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1042150
localization_priority: Normal
ms.assetid: b3f3a0a0-7b14-0b71-d247-ada81b93b66b
description: SETATREF 関数の set_expression パラメーターで使用して、SETATREF の参照パラメーターに割りset_expression前に評価する必要があるかどうかを示します。
ms.openlocfilehash: a11a7485e04d4deb31e9497476bb198d675bc68f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432983"
---
# <a name="setatrefeval-function"></a>SETATREFEVAL 関数

SETATREF _関数の set_expression_ パラメーターで使用して、SETATREFの参照パラメーターに割り当てる前に、set_expressionを評価する必要があるかどうかを示します。 
  
## <a name="syntax"></a>構文

SETATREFEVAL(** *expr* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expr_ <br/> |必須  <br/> |**さまざま** <br/> | SETATREF 関数が別のセルにリダイレクトするときに _set_expression式。_  <br/> |
   
## <a name="remarks"></a>注釈

SETATREF *関数の set_expression* パラメーターを参照セルに割り当てると、Microsoft Visio set_expressionは既定でセルに式として書き込みます。 *ただし、set_expression* パラメーターの一部が SETATREFEVAL 関数によってラップされている場合、Visio は式を評価し、SETATREFEVAL 関数を結果に置き換え、SETATREF 式を解決します。 
  
## <a name="example"></a>例

例については、[SETATREF](setatref-function.md) 関数を参照してください。 
  

