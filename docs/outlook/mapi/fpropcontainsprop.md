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
ms.openlocfilehash: b08d3af8c61d8ced31e822bb787d49ad90b4df54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571676"
---
# <a name="fpropcontainsprop"></a>FPropContainsProp

**適用されます**: Outlook 2013 |Outlook 2016 
  
文字列またはバイナリ配列は、1 つが含まれている他の一般的に、2 つのプロパティ値を比較します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a>パラメーター

_lpSPropValueDst_
  
> [in]_LpSPropValueSrc_パラメーターで指定された検索文字列を含む可能性があるプロパティの値を定義する[SPropValue](spropvalue.md)構造体へのポインター。 
    
_lpSPropValueSrc_
  
> [in]_LpSPropValueDst_パラメーターで指定されたプロパティの値で**FPropContainsProp**を検索する検索文字列を定義する**SPropValue**構造体へのポインター。 
    
_ulFuzzyLevel_
  
> [in]オプションの設定 preciseness のレベルを定義する、比較で使用します。 

  - **下位 16 ビット**は、PT_BINARY と PT_STRING8 型のプロパティに適用されます。 次の値の 1 つだけを設定する必要があります。
      
    - FL_FULLSTRING: _lpSPropValueSrc_の検索文字列を_lpSPropValueDst_で識別されるプロパティの値と同じにする必要があります。
        
    - FL_PREFIX: _lpSPropValueSrc_の検索文字列は、 _lpSPropValueDst_によって識別されるプロパティの値の先頭にあります。 _LpSPropValueSrc_によって示される検索文字列の長さの分だけ、2 つの値を比較する必要があります。 
        
    - FL_SUBSTRING: _lpSPropValueSrc_の検索文字列に含まれなければならない任意の場所_lpSPropValueDst_によって識別されるプロパティの値。 
      
  - **上位 16 ビット**は PT_STRING8 の種類のプロパティにのみ適用されます。 任意の組み合わせで次の値に設定できます。
    
    - FL_IGNORECASE: 大文字と小文字を考慮せず、比較を行ってください。 
        
    - FL_IGNORENONSPACE: 比較は、アクセント記号などの非スペーシング文字の Unicode で定義されているを無視してください。 
        
    - FL_LOOSE: 比較が一致する限り、大文字と小文字を示す必要がありますと小文字を区別し、非スペーシング文字。
    
## <a name="return-value"></a>戻り値

TRUE 
  
> パラメーターはすべて有効ですし、 _lpSPropValueSrc_の検索文字列が含まれている_lpSPropValueDst_プロパティの値で指定しました。 
    
FALSE 
  
> PT_STRING8 または PT_BINARY 型は比較対象のプロパティ値、プロパティ値は、さまざまな種類のまたは_lpSPropValueSrc_の検索文字列が含まれていない_lpSPropValueDst_のプロパティの値で指定しました。 
    
## <a name="remarks"></a>注釈

比較メソッドは、 [SPropValue](spropvalue.md)プロパティの定義で指定されたプロパティの型および_ulFuzzyLevel_パラメーターで指定したあいまいレベル ヒューリスティックによって異なります。 テーブルを生成するための制限を準備するのには、 [FPropCompareProp](fpropcompareprop.md)と**FPropContainsProp**関数を使用できます。 
  
PT_BINARY プロパティの型では、 _ulFuzzyLevel_の上位 16 ビットは無視されます。 _UlFuzzyLevel_の設定が存在しないか無効な場合、完全な文字列の完全一致が実行されます。 プロパティの包含構造の詳細については、 [SContentRestriction](scontentrestriction.md)構造体を参照してください。 
  

