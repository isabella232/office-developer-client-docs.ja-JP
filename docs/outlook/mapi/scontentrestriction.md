---
title: SContentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SContentRestriction
api_type:
- COM
ms.assetid: 784c8a5a-493e-48e6-8784-ba8122c76e3d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 87be6df27a3e6729cb514118438521d76a66b30c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339838"
---
# <a name="scontentrestriction"></a>SContentRestriction
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
コンテンツ制限について説明します。これは、テーブルビューを、検索文字列と一致するコンテンツを持つ列を含む行だけに制限するために使用されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a>Members

**ulFuzzyLevel**
  
> 一致するかどうかを確認するときにコンテンツ制限に適用する preciseness レベルを定義するオプション設定。
    
   **ulFuzzyLevel**メンバーの**下位16ビット**は、PT_BINARY および PT_STRING8 型のプロパティに適用され、次のいずれかの値に設定する必要があります。 
    
   - FL_FULLSTRING: 一致するには、 **lpprop**検索文字列が**ulPropTag**で識別されるプロパティに含まれている必要があります。
        
   - FL_PREFIX: 一致するには、 **ulPropTag**で識別されるプロパティの先頭に**lpprop**検索文字列を指定する必要があります。 2つの文字列は、 **lpprop**で示される検索文字列の長さまで比較する必要があります。 
        
   - FL_SUBSTRING: 一致するには、 **lpprop**検索文字列が**ulPropTag**で識別されるプロパティの任意の場所に含まれている必要があります。 
        
   **ulFuzzyLevel**メンバーの**上位16ビット**は、PT_STRING8 型のプロパティにのみ適用され、任意の組み合わせで次の値に設定できます。 
        
   - FL_IGNORECASE: 比較は、大文字と小文字を区別せずに行う必要があります。 
        
   - FL_IGNORENONSPACE: 比較では、Unicode で定義されたスペース以外の文字 (分音記号など) を無視する必要があります。 
        
   - FL_LOOSE: 比較によって、大文字と小文字を区別せずに、可能な限り一致が得られます。 
    
**ulPropTag**
  
> 検索文字列の出現をチェックする文字列プロパティを識別するプロパティタグ。 
    
**lpprop**
  
> 検索文字列として使用する文字列値を含むプロパティ値構造体へのポインター。
    
## <a name="remarks"></a>解説

**scontentrestriction**構造体には、 **ulPropTag**メンバーと、 **lpprop**でポイントされている**scontentrestriction**構造の**ulPropTag**メンバー内の2つのプロパティタグがあります。 両方のタグで、MAPI は property type フィールドのみを必要とし、[プロパティ識別子] フィールドは無視されます。 ただし、2つのプロパティの型が一致している必要があります。または、制限が[imapitable:: Restrict](imapitable-restrict.md)または[imapitable:: FindRow](imapitable-findrow.md)の呼び出しで使用されている場合は、エラー値 MAPI_E_TOO_COMPLEX が返されます。 
  
FL_FULLSTRING、FL_PREFIX、および FL_SUBSTRING の値は相互に排他的です。 設定できるのは1つだけで、そのうちの1つを設定する必要があります。 これらの意味は固定されており、プロバイダーは定義されたとおりに実装する必要があります。 プロバイダーは、これらの値をサポートできない場合は MAPI_E_TOO_COMPLEX を返します。 
  
FL_IGNORECASE、FL_IGNORENONSPACE、および FL_LOOSE の値は独立しています。 ゼロから3つまでのすべての場所を設定できます。 これらの定義はガイドラインとしてのみ提供されており、プロバイダーは各フラグの固有の意味を自由に実装することができます。 プロバイダーは、指定されたフラグの実装がない場合は、エラー表示を返さないようにする必要があります。 
  
プロパティが存在しない場合、プロパティに対して適用されるコンテンツ制限の結果は未定義です。 クライアントでこのような制限に対して適切に定義された動作が必要であり、そのプロパティが存在するかどうかが不明な場合は、そのプロパティが存在するかどうかは、テーブルの必須列ではないので、コンテンツ制限を既存の制限で結合するための**と**制限を作成する必要があります。 [sexistrestriction](sexistrestriction.md)構造を使用して、**と**制限を定義するための、存在制限と[SAndRestriction](sandrestriction.md)構造を定義します。 
  
**scontentrestriction**構造と一般的な制限の詳細については、「[制限につい](about-restrictions.md)て」を参照してください。
  
## <a name="see-also"></a>関連項目

- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [MAPI の構造](mapi-structures.md)

