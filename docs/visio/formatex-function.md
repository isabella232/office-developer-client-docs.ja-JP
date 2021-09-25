---
title: FORMATEX 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251590
ms.localizationpriority: medium
ms.assetid: d375c971-fee2-baa3-dc4f-a26018e70e8a
description: dstUnit で記述された形式に従って書式設定された文字列として、srcUnit で評価された式の結果を返します。
ms.openlocfilehash: 4572c609ddb6a2a60cf34517531495705752ec7a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554769"
---
# <a name="formatex-function"></a>FORMATEX 関数

dstUnit で記述された形式に従って書式設定された文字列として、srcUnit で評価された式の結果を返します。
  
## <a name="syntax"></a>構文

FORMATEX(** *式* **," ** *format* ** ",[ ** *srcUnit* ** ],[ ** *dstUnit* ** ],[ ** *langID* ** ][, ** *calID* ** ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須  <br/> |**String** <br/> |定数、演算子、関数、およびシェイプシートのセルに対する参照を組み合わせたもので、結果が値となる式です。  <br/> |
| _format_ <br/> |必須  <br/> |**String** <br/> |文字列の書式設定に使用する図の書式設定。図の書式設定の詳細については、「[図の書式設定](about-format-pictures.md)」を参照してください。<br/> |
| _srcUnit_ <br/> |省略可能  <br/> |**String** <br/> | 式を評価するために使用する単位 (in、cm など) です。  <br/> |
| _dstUnit_ <br/> |省略可能  <br/> |**String** <br/> |式の結果に使用する単位 (in、cm など) です。  <br/> |
| _langID_ <br/> |オプション  <br/> |**数値** <br/> |Microsoft Office system の日付/時間形式の書式設定に使用する言語です。  <br/> |
| _calID_ <br/> |オプション  <br/> |**数値** <br/> |Microsoft Office system の日付/時間形式を書式設定するときのカレンダーです。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

式の種類および図の書式設定で指定されている形式に応じて、返される文字列の書式が決まります。この書式は式の種類に適したものでなければなりません。
  
3 + 4 などのように、種類が指定されていない式の結果を計算するには、srcUnit 引数を使用します。3 ft + 8 ft などのように、式の結果の種類が明示されている場合は、srcUnit は無視されます。
  
書式設定された結果に使用する単位を指定するには、dstUnit 引数を使用します。dstUnit を指定しないと、式の結果の単位が使用されます。
  
式の結果と書式設定で指定されている形式が異なる場合、書式設定に構文エラーがある場合、または srcUnit や dstUnit として渡された単位が認識されない場合、エラーを返します。
  
## <a name="example"></a>例

FORMATEX(5.5, "0.00 u", "cm", "ft") 
  
0.18 フィートを返します。 
  

