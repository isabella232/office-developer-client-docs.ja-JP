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
ms.openlocfilehash: 43703051193ffacec6a54355eeea74edf904f186
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580573"
---
# <a name="scontentrestriction"></a>SContentRestriction
 
**適用されます**: Outlook 2013 |Outlook 2016 
  
検索文字列に一致する内容を持つ列を含む行だけを表形式ビューを制限するために使用されるコンテンツの制限について説明します。 
  
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

## <a name="members"></a>Members

**ulFuzzyLevel**
  
> オプションの設定が一致することを確認するときにコンテンツの制限が設定されている preciseness のレベルを定義します。
    
   **UlFuzzyLevel**メンバーの**下位 16 ビット**は、PT_BINARY と PT_STRING8 プロパティの型に適用し、次の値のいずれかに設定する必要があります。 
    
   - FL_FULLSTRING: 一致するには、 **lpProp**の検索文字列含める必要があります**ulPropTag**によって識別されるプロパティにします。
        
   - FL_PREFIX: 一致するには、 **lpProp**の検索文字列必要があります**ulPropTag**によって識別されるプロパティの先頭にします。 **LpProp**によって示される検索文字列の長さの分だけ、2 つの文字列を比較する必要があります。 
        
   - FL_SUBSTRING: 一致するには、 **lpProp**検索文字列含める必要があります任意の場所**ulPropTag**によって識別されるプロパティにします。 
        
   **UlFuzzyLevel**メンバーの**上位 16 ビット**では、型 PT_STRING8 プロパティにのみ適用され、任意の組み合わせで次の値を設定することができます。 
        
   - FL_IGNORECASE: 大文字と小文字を考慮せず、比較を行ってください。 
        
   - FL_IGNORENONSPACE: 比較は、アクセント記号などの Unicode が定義されている空白でない文字を無視してください。 
        
   - FL_LOOSE: 比較頂いた一致する限り、大文字と小文字、空白でない文字を無視しています。 
    
**ulPropTag**
  
> プロパティ タグが検索文字列の出現箇所をチェックする文字列プロパティを識別します。 
    
**lpProp**
  
> 検索文字列として使用する文字列値を格納するプロパティ値の構造体へのポインター。
    
## <a name="remarks"></a>注釈

**SContentRestriction**構造体には 2 つのプロパティ タグがあります: **lpProp**が指す**ulPropTag**のメンバーと、 **ulPropTag** 、 **SPropValue**構造体のメンバーで、その他のいずれかです。 両方のタグでは、MAPI プロパティの種類のフィールドだけが必要ですでプロパティの識別子フィールドは無視されます。 ただし、2 つのプロパティの型が一致する必要がありますか、またはエラー値の制限は、 [IMAPITable::Restrict](imapitable-restrict.md)または[IMAPITable::FindRow](imapitable-findrow.md)への呼び出しで使用すると MAPI_E_TOO_COMPLEX が返されます。 
  
FL_FULLSTRING、FL_PREFIX、FL_SUBSTRING の値は、相互に排他的です。 それらの 1 つだけを設定することができ、それらのいずれかを設定する必要があります。 その意味は固定で、プロバイダーは定義されているとおりに正確にして実装する必要があります。 プロバイダーは、これらの値をサポートするためにできない場合、MAPI_E_TOO_COMPLEX を返す必要があります。 
  
FL_IGNORECASE、FL_IGNORENONSPACE、FL_LOOSE の値は独立しています。 任意の場所それらのすべての 3 つのゼロからを設定できます。 ガイドラインとしてのみ、その定義が用意されているし、プロバイダーは、各フラグの特定の意味は、独自に実装するために自由です。 プロバイダーでは指定されたフラグの実装が存在しない場合、エラーは返されません。 
  
プロパティが存在しない場合、プロパティに対して設定されたコンテンツの制限の結果は定義されていません。 クライアントは、このような制限について明確に定義された動作が必要で、たとえばプロパティが存在するかどうかでないことが必要なテーブルの列ではありません、既存の制限のあるコンテンツの制限に参加する**と**制限も作成する必要があります。 [SExistRestriction](sexistrestriction.md)構造体を使用すると、既存の制限、**および**制限を定義するのには、 [SAndRestriction](sandrestriction.md)構造体を定義します。 
  
**SContentRestriction**構造体および制限の詳細については一般に、[制限の詳細](about-restrictions.md)を参照してください。
  
## <a name="see-also"></a>関連項目

- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [MAPI の構造](mapi-structures.md)

