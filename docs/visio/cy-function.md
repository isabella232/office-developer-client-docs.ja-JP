---
title: CY 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253223
ms.localizationpriority: medium
ms.assetid: abb27f90-21b4-08cd-6995-9520fbcebd78
description: 通貨の値を返します。
ms.openlocfilehash: a94be94db24d9e9f34acf7289878295d4b35c66d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594665"
---
# <a name="cy-function"></a>CY 関数

通貨の値を返します。
  
## <a name="syntax"></a>構文

CY(** *value* **, ** *cyID* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |オプション  <br/> |**Number または String** <br/> |通貨固有の書式を含む数値または文字列。 指定しない場合、通貨の値は、システムの [地域] および [言語] 設定の通貨スタイルに従って書式設定されます。  <br/> |
| _cyID_ <br/> |オプション  <br/> |**数値** <br/> |ISO 4217 省略形の数値通貨 ID または 3 文字の引用符で囲まれた文字列。  <br/> |
   
## <a name="remarks"></a>注釈

別の通貨を指定するには、有効な cyID を含める  _必要があります_。 通貨の一覧については、「[通貨定数について](about-currency-constants.md)」を参照してください。
  
値  _が_ 指定された通貨の種類と互換性がない場合、または "数値ではない" などの無効な引数が指定されている場合は、#VALUE! エラーを返します。 値  _が_ 922,337,203,685,477.5807 より大きい場合、または -922,337,203,685,477.5808 より小さい場合は、#VALUE! エラーを返します。 
  
3.6 兆など、単位の分数を含む非常に大きな通貨値で精度を高めるには、値に文字列引数を使用  _します_。
  
無効な  _cyID を指定すると、_ エラーが返されます。 
  
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
  

