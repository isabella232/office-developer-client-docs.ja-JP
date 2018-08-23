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
description: SETATREF 関数の式のパラメーターで使用すると、SETATREF 参照パラメーターに割り当てる前にその式を評価するかを指定します。
ms.openlocfilehash: 0826ef9ca91e180576c0b2611452758b238736a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806366"
---
# <a name="setatrefeval-function"></a>SETATREFEVAL 関数

SETATREF 関数の_式_のパラメーターで使用すると、SETATREF_参照_パラメーターに割り当てる前にその_式_を評価するかを指定します。 
  
## <a name="syntax"></a>構文

SETATREFEVAL (* * *expr* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expr_ <br/> |必須  <br/> |**多様** <br/> | SETATREF 関数は、_セット式_を別のセルにリダイレクトするときに評価される式を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

SETATREF 関数の*式*のパラメーターを参照先のセルに代入すると、Microsoft Visio に書き込みます*セット式*セル式としてデフォルトで。 ただし、*セット式*のパラメーターの任意の部分は、SETATREFEVAL 関数によってラップされたが、Visio は式を評価し、SETATREF 式を解決する前にその結果で SETATREFEVAL 関数を置き換えます。 
  
## <a name="example"></a>例

例については、[SETATREF](setatref-function.md) 関数を参照してください。 
  

