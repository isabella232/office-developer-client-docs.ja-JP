---
title: FPropContainsProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropContainsProp
api_type:
- COM
ms.assetid: 43da5b59-7691-49aa-b83c-753d43bfd8fd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ea56996ad56bb4ce93d103a75eba2c29e6059a87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328043"
---
# <a name="fpropcontainsprop"></a>FPropContainsProp

**適用対象**: Outlook 2013 | Outlook 2016 
  
2つのプロパティ値 (通常は文字列またはバイナリ配列) を比較して、一方に他方が含まれているかどうかを確認します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a>パラメーター

_lpspropvaluedst_
  
> 順番_lpspropバリュー rc_パラメーターで指定された検索文字列を含むことができるプロパティ値を定義する[spropvalue](spropvalue.md)構造体へのポインター。 
    
_lpspropて rc_
  
> 順番**fpropan prop**が、 _lpspropvaluedst_パラメーターで指定されたプロパティ値をシークする、 **spropvalue**構造体へのポインター。 
    
_ulFuzzyLevel_
  
> 順番比較で使用する preciseness のレベルを定義するオプション設定。 

  - **下位16ビット**は、PT_BINARY および PT_STRING8 型のプロパティに適用されます。 次の値のいずれかを正確に設定する必要があります。
      
    - FL_FULLSTRING: _lpspropvalues rc_検索文字列は、 _lpspropvaluedst_で識別されるプロパティ値と等しくなければなりません。
        
    - FL_PREFIX: lpspropvaluesrc の検索文字列は、 _lpspropvaluedst_で識別されるプロパティ値の先頭に配置する必要があります。 __ 2つの値は、 _lpspropvalues rc_で示される検索文字列の長さまで比較する必要があります。 
        
    - FL_SUBSTRING: lpspropvaluesrc の検索文字列は、 _lpspropvaluedst_で識別されるプロパティ値の任意の場所に格納されている必要があります。 __ 
      
  - **上位16ビット**は、PT_STRING8 型のプロパティにのみ適用されます。 これらの値は、次の任意の組み合わせで設定できます。
    
    - FL_IGNORECASE: 比較は大文字と小文字の区別を考慮せずに行う必要があります。 
        
    - FL_IGNORENONSPACE: 比較では、Unicode で定義されたスペーシング文字 (アクセント記号など) を無視する必要があります。 
        
    - FL_LOOSE: 比較では、大文字と小文字の区別を無視して、可能な限り一致を示す必要があります。
    
## <a name="return-value"></a>戻り値

TRUE 
  
> パラメーターはすべて有効で、lpspropvaluesrc の検索文字列は_lpspropvaluedst_プロパティ値に指定されたとおりに含まれています。 __ 
    
FALSE 
  
> 比較対象のプロパティ値が PT_STRING8 または PT_BINARY の型ではないか、プロパティ値が異なる型で__ あるか、lpspropvaluesrc 検索文字列が_lpspropvaluedst_プロパティ値で指定されたとおりに含まれていません。 
    
## <a name="remarks"></a>解説

比較方法は、 [spropvalue](spropvalue.md)プロパティの定義に指定されているプロパティの種類と、 _ulFuzzyLevel_パラメーターで指定されているファジーレベルヒューリスティックによって異なります。 [fpropcompareprop](fpropcompareprop.md)および**fpropの prop**関数を使用して、テーブルの生成に関する制限を準備できます。 
  
プロパティの種類が PT_BINARY の場合、 _ulFuzzyLevel_の上位16ビットは無視されます。 _ulFuzzyLevel_の設定が指定されていない場合、または無効な場合は、完全な文字列の完全一致が実行されます。 プロパティコンテインメントの詳細については、 [scontentrestriction](scontentrestriction.md)構造を参照してください。 
  

