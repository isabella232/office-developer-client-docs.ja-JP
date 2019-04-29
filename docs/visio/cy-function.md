---
title: CY 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253223
localization_priority: Normal
ms.assetid: abb27f90-21b4-08cd-6995-9520fbcebd78
description: 通貨値を返します。
ms.openlocfilehash: 65c88d69669e2fa7f708402d9d50dfe035456edb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433557"
---
# <a name="cy-function"></a>CY 関数

通貨値を返します。
  
## <a name="syntax"></a>構文

CY (* **値** *、* * *cyid* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |省略可能  <br/> |**Number または String** <br/> |通貨固有の書式設定を含む数値または文字列。 指定しない場合、通貨の値は、システムの地域と言語の設定の通貨スタイルに従って書式設定されます。  <br/> |
| _cyid_ <br/> |省略可能  <br/> |**数値** <br/> |通貨 ID、または ISO 4217 の省略形を表す3文字の引用符で区切られた文字列。  <br/> |
   
## <a name="remarks"></a>注釈

別の通貨を指定するには、有効な_cyid_を含める必要があります。 通貨の一覧については、「[通貨定数について](about-currency-constants.md)」を参照してください。
  
_value_が指定した通貨の種類と互換性がない場合、または "not not number" などの無効な引数が指定されている場合は、#VALUE します。 エラーを返します。 _値_が922337203685477.5807 より大きい場合、または-922337203685477.5808 未満の場合は、#VALUE します。 エラーを返します。 
  
単位の分数 (3兆6000億など) を含む非常に大きな通貨の値を使用した場合の精度を向上させるには、 _value_に文字列引数を使用します。
  
無効な_cyid_を指定すると、エラーが返されます。 
  
## <a name="example-1"></a>例 1

ユーザーの [地域と言語] 設定で米国ドルが指定されている場合:
  
CY (999998.993)
  
$999,998.99 を返します。
  
## <a name="example-2"></a>例 2

CY(12345678.993, "USD")
  
$12,345,678.99 を返します。
  
## <a name="example-3"></a>例 3

CY(12345678.993, "DEM")
  
12,345,678.99 DEM を返します。
  
## <a name="example-4"></a>例 4

CY(12345678.7832, "XXX")
  
12,345,678.78 を返します。
  

