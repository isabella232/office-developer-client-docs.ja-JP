---
title: SContentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SContentRestriction
api_type:
- COM
ms.assetid: 784c8a5a-493e-48e6-8784-ba8122c76e3d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c007d2ea61810aa93685a2d91836afdc4209d623
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624280"
---
# <a name="scontentrestriction"></a>SContentRestriction
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブル ビューを、検索文字列に一致するコンテンツを含む列を含む行にのみ制限するために使用されるコンテンツ制限について説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a>メンバー

**ulFuzzyLevel**
  
> 一致を確認するときにコンテンツ制限が適用する精度のレベルを定義するオプション設定。
    
   **ulFuzzyLevel** メンバーの下位 **16** ビットは、PT_BINARY および PT_STRING8 型のプロパティに適用され、次のいずれかの値に設定する必要があります。 
    
   - FL_FULLSTRING: 一致するには **、lpProp** 検索文字列が ulPropTag で識別されるプロパティに含 **まれている必要があります**。
        
   - FL_PREFIX : 一致するには **、ulPropTag** で識別されるプロパティの最初に lpProp 検索文字列が **表示されている必要があります**。 2 つの文字列は、lpProp で示される検索文字列の長さまでのみ比較 **する必要があります**。 
        
   - FL_SUBSTRING: 一致するには **、lpProp** 検索文字列が ulPropTag で識別されるプロパティの任意の場所に **含まれている必要があります**。 
        
   **ulFuzzyLevel** メンバーの上位 **16** ビットは、PT_STRING8 型のプロパティにのみ適用され、任意の組み合わせで次の値に設定できます。 
        
   - FL_IGNORECASE: ケースを考慮せずに比較を行う必要があります。 
        
   - FL_IGNORENONSPACE: この比較では、二等分記号などの Unicode で定義された非間隔文字は無視する必要があります。 
        
   - FL_LOOSE: 大文字と小文字を無視して、可能な限り一致する比較を行う必要があります。 
    
**ulPropTag**
  
> 検索文字列の出現をチェックする文字列プロパティを識別するプロパティ タグ。 
    
**lpProp**
  
> 検索文字列として使用する文字列値を含むプロパティ値構造体へのポインター。
    
## <a name="remarks"></a>注釈

**SContentRestriction** 構造体には **、1 つは ulPropTag** メンバー、もう 1 つは **lpProp** によって指される **SPropValue** 構造体の **ulPropTag** メンバーの 2 つのプロパティ タグがあります。 どちらのタグでも、MAPI はプロパティの種類フィールドのみを必要とし、プロパティ識別子フィールドを無視します。 ただし、2 つのプロパティの種類が一致する必要があります。それ以外の場合は [、IMAPITable::Restrict](imapitable-restrict.md) または [IMAPITable::FindRow](imapitable-findrow.md)の呼び出しで制限が使用される場合、エラー値 MAPI_E_TOO_COMPLEX が返されます。 
  
値はFL_FULLSTRING、FL_PREFIX、およびFL_SUBSTRING排他的です。 設定できるのは 1 つのみであり、そのうちの 1 つを設定する必要があります。 その意味は固定され、プロバイダーは定義されたとおりに実装する必要があります。 プロバイダーは、これらの値MAPI_E_TOO_COMPLEXサポートできない場合は、この値を返す必要があります。 
  
値はFL_IGNORECASE、FL_IGNORENONSPACE、およびFL_LOOSE独立しています。 ゼロから 3 つすべての任意の場所に設定できます。 これらの定義はガイドラインとしてのみ提供され、プロバイダーは各フラグの固有の意味を自由に実装できます。 指定したフラグが実装されていない場合、プロバイダーはエラーの表示を返す必要はありません。 
  
プロパティに対してコンテンツ制限が適用された結果は、プロパティが存在しない場合は未定義です。 クライアントがこのような制限に対して十分に定義された動作を必要とし、プロパティが存在するかどうかが分からない場合、プロパティがテーブルの必須列ではない場合は、存在制限を使用してコンテンツ制限に参加する **AND** 制限を作成する必要があります。 [SExistRestriction](sexistrestriction.md)構造体を使用して、存在制限と [SAndRestriction](sandrestriction.md)構造体を定義して AND 制限 **を定義** します。 
  
**SContentRestriction** 構造と制限全般の詳細については、「制限について」[を参照してください](about-restrictions.md)。
  
## <a name="see-also"></a>関連項目

- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [MAPI の構造](mapi-structures.md)

