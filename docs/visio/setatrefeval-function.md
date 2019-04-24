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
description: SETATREF 関数の set_expression パラメーターで使用され、SETATREF の reference パラメーターに割り当てる前に set_expression を評価する必要があることを示します。
ms.openlocfilehash: a11a7485e04d4deb31e9497476bb198d675bc68f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326160"
---
# <a name="setatrefeval-function"></a>SETATREFEVAL 関数

SETATREF 関数の_set_expression_パラメーターで使用され、SETATREF の_reference_パラメーターに割り当てる前に_set_expression_を評価する必要があることを示します。 
  
## <a name="syntax"></a>構文

SETATREFEVAL (* * *expr* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expr_ <br/> |必須  <br/> |**さまざま** <br/> | SETATREF 関数が_set_expression_を別のセルにリダイレクトするときに評価される式を指定します。  <br/> |
   
## <a name="remarks"></a>解説

SETATREF 関数の*set_expression*パラメーターを参照先のセルに代入すると、Microsoft Visio は既定でそのセルに*set_expression*を式として書き込みます。 ただし、 *set_expression*パラメーターのいずれかの部分が SETATREFEVAL 関数によってラップされている場合、Visio は式を評価し、SETATREFEVAL 関数をその結果に置き換えて SETATREF 式を解決します。 
  
## <a name="example"></a>例

例については、[SETATREF](setatref-function.md) 関数を参照してください。 
  

