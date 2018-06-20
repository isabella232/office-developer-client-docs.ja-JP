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
ms.openlocfilehash: ea7696e7628939466730b9c054a706a7a9fa264e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805136"
---
# <a name="cy-function"></a>CY 関数

通貨値を返します。
  
## <a name="syntax"></a>構文

CY (* **値** *、* * *cyID* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |省略可能  <br/> |**数値または文字列** <br/> |数値または通貨固有の書式設定を含む文字列です。 指定しない場合、通貨型の値はシステムの地域と言語の設定の通貨スタイルに従って書式設定されます。  <br/> |
| _cyid を指定_ <br/> |省略可能  <br/> |**番号** <br/> |数値通貨 ID、または ISO 4217 の省略形の 3 文字の引用符で囲まれた文字列です。  <br/> |
   
## <a name="remarks"></a>備考

別の通貨を指定するには、有効な_cyid を指定_する必要があります。 一覧については、[通貨定数について](about-currency-constants.md)参照してください。
  
_値_は、通貨の種類と互換性がない場合、または「非数」などの無効な引数が指定されて、#value!! エラーが返されます。 _値_が 922,337,203,685,477.5807 またはより少ない-922,337,203,685,477.5808、#value! より大きい場合は! エラーが返されます。 
  
精度 3.6 兆など、単位の小数点を含む非常に大きな通貨の値を向上させるには、_値_の文字列引数を使用します。
  
無効な_cyID_を指定するには、エラーが返されます。 
  
## <a name="example-1"></a>例 1

ユーザーの [地域と言語] 設定で米国ドルが指定されている場合:
  
CY(999998.993)
  
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
  

