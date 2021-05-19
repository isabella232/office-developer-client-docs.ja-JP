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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ea56996ad56bb4ce93d103a75eba2c29e6059a87
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432633"
---
# <a name="fpropcontainsprop"></a>FPropContainsProp

**適用対象**: Outlook 2013 | Outlook 2016 
  
2 つのプロパティ値 (通常は文字列またはバイナリ配列) を比較して、もう 1 つのプロパティ値にもう一方が含まれているか確認します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a>パラメーター

_lpSPropValueDst_
  
> [in]_lpSPropValueSrc_ パラメーターが指す検索文字列を含む可能性があるプロパティ値を定義する [SPropValue](spropvalue.md)構造体へのポインター。 
    
_lpSPropValueSrc_
  
> [in]_lpSPropValueDst_ パラメーターが指すプロパティ値で **FPropContainsProp** がシークしている検索文字列を定義する **SPropValue** 構造体へのポインター。 
    
_ulFuzzyLevel_
  
> [in]比較で使用する精度のレベルを定義するオプション設定。 

  - 下位 **16 ビットは、** 種類と種類のプロパティに適用PT_BINARYおよびPT_STRING8。 これらは、次のいずれかの値に設定する必要があります。
      
    - FL_FULLSTRING:  _lpSPropValueSrc_ 検索文字列は  _、lpSPropValueDst_ で識別されるプロパティ値と等しくする必要があります。
        
    - FL_PREFIX:  _lpSPropValueSrc_ 検索文字列は  _、lpSPropValueDst_ で識別されるプロパティ値の先頭に表示する必要があります。 2 つの値は  _、lpSPropValueSrc_ で示される検索文字列の長さまでのみ比較する必要があります。 
        
    - FL_SUBSTRING:  _lpSPropValueSrc_ 検索文字列は  _、lpSPropValueDst_ で識別されるプロパティ値の任意の場所に含まれている必要があります。 
      
  - 上位 **16 ビットは、** データ型のプロパティにのみPT_STRING8。 これらは、任意の組み合わせで次の値に設定できます。
    
    - FL_IGNORECASE: 大文字と小文字の区別を考慮せずに比較を行う必要があります。 
        
    - FL_IGNORENONSPACE: この比較では、Unicode で定義された非太平洋文字 (等値記号など) は無視する必要があります。 
        
    - FL_LOOSE: 大文字と小文字の区別と非スパック文字を無視して、可能な限り一致を示す必要があります。
    
## <a name="return-value"></a>戻り値

TRUE 
  
> パラメーターはすべて有効で  _、lpSPropValueSrc_ 検索文字列は  _lpSPropValueDst_ プロパティの値で指定されている通り含まれています。 
    
FALSE 
  
> 比較されるプロパティの値は、PT_STRING8 または PT_BINARY 型ではないか、プロパティ値が異なる型か  _、lpSPropValueSrc_ 検索文字列が  _lpSPropValueDst_ プロパティ値で指定された値に含めされていません。 
    
## <a name="remarks"></a>注釈

比較メソッドは [、SPropValue](spropvalue.md) プロパティ定義で指定されたプロパティの種類と  _、ulFuzzyLevel_ パラメーターで提供されるファジー レベルのヒューリスティックによって異なります。 [FPropCompareProp](fpropcompareprop.md)関数と **FPropContainsProp** 関数を使用して、テーブルを生成するための制限を準備できます。 
  
_ulFuzzyLevel_ の上位 16 ビットは、プロパティの種類が指定PT_BINARY。 _ulFuzzyLevel の設定が_ 見つからないか無効な場合は、完全文字列の完全一致が実行されます。 プロパティの格納の詳細については [、「SContentRestriction 構造体」を参照](scontentrestriction.md) してください。 
  

