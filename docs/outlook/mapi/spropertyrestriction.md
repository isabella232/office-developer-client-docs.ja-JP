---
title: SPropertyRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropertyRestriction
api_type:
- COM
ms.assetid: 2bbf13e9-05b3-4498-8e08-d9e07505190d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 29d392eba530126e06a672c10044c5b4df0618c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357856"
---
# <a name="spropertyrestriction"></a>SPropertyRestriction

**適用対象**: Outlook 2013 | Outlook 2016 
  
定数をプロパティの値と照合するために使用されるプロパティ制限を記述します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a>Members

**relop**
  
> 検索で使用される関係演算子です。 可能な値は次のとおりです。
    
  - RELOP_GE: 比較は、最初の値よりも大きくなるか等しいかに基づいて行われます。
        
  - RELOP_GT: 比較は、より大きな最初の値に基づいて行われます。
        
  - RELOP_LE: 比較は、最初の値よりも小さいか等しいかに基づいて行われます。
        
  - RELOP_LT: 比較は、小さい方の値に基づいて行われます。
        
  - RELOP_NE: 比較は、等しくない値に基づいて行われます。
        
  - RELOP_RE: 比較は、LIKE (正規表現) の値に基づいて行われます。
        
  - RELOP_EQ: 比較は同じ値に基づいて行われます。
    
**ulPropTag**
  
> 比較するプロパティを識別するプロパティタグ。 
    
**lpprop**
  
> 比較で使用される定数値を含む[spropvalue](spropvalue.md)構造体へのポインター。 
    
## <a name="remarks"></a>解説

**spropertyrestriction**構造には、2つのプロパティタグがあります。 一方は**ulPropTag**メンバーで、もう1つは**lpprop**でポイントされた**spropvalue**構造の**ulPropTag**メンバーにあります。 MAPI には、[プロパティ識別子] フィールドと [プロパティの種類] フィールドの両方が必要です。 **spropertyrestriction**の**ulPropTag**は一致するプロパティを示し、 **spropertyrestriction**の**ulPropTag**の種類に対する**spropertyrestriction**の**lpprop**ポインターは、のメンバーの値がどのように表示されるかを示しています。**lpprop**ユニオンが解釈されます。 2つのプロパティの型は一致している必要があります。または、制限が[imapitable:: Restrict](imapitable-restrict.md)または[imapitable:: FindRow](imapitable-findrow.md)の呼び出しで使用されている場合、エラー値 MAPI_E_TOO_COMPLEX が返されます。 
  
比較順序は、 _(プロパティ値) (リレーショナル演算子) (定数値_) です。
  
プロパティ制限が**IMAPITable:: Restrict**または**imapitable:: FindRow**に渡され、target プロパティが存在しない場合、制限の結果は未定義となります。 プロパティ制限に参加する**と**制限が存在し、制限が**存在**することにより、発信者が正確な結果を保証できます。 [sexistrestriction](sexistrestriction.md)構造を使用して、**と**制限を定義するための、**存在**制限と[SAndRestriction](sandrestriction.md)構造を定義します。 
  
テーブルを実装しているサービスプロバイダーがそれらをサポートしている場合は、プロパティ制限で複数値プロパティタグを使用できます。 サポートされている場合は、複数値プロパティタグを使用して、単一値のプロパティタグを任意の場所で使用できます。 
  
複数値プロパティタグは、次の方法で使用できます。
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::GetProps](imapiprop-getprops.md)
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [IMAPITable::Restrict](imapitable-restrict.md)
    
> [!IMPORTANT]
> 複数値のプロパティを制限する場合は、2つのプロパティタグが一致しないようなケースがあります。 この場合は、次の条件を満たす必要があります。 > **spropertyrestriction**の**ulPropTag**のプロパティの種類に、複数値のプロパティの種類のビットフラグ MV_FLAG (0x1000) が含まれている場合、 **spropertyrestriction**の**ulPropTag**のプロパティの型は、以前の MV_ を除いた値と一致する必要があります。フラグビットフラグ (逆)。 > たとえば、プロパティ0x8012101f のプロパティタグを持つカテゴリなど、複数値のカスタム文字列プロパティを使用するように制限するには、PROP_TAG (MV_FLAG | PT_UNICODE, 0x8012) のように、対応する**spropertyrestriction**が表示されます。示し. >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> **spropvalue**の**ulPropTag**のプロパティの種類に MV_FLAG ビットフラグが含まれている場合は、戻り値は MAPI_E_TOO_COMPLEX になる可能性があることに注意してください。 
  
**spropertyrestriction**構造の詳細については、「[制限につい](about-restrictions.md)て」を参照してください。 
  
## <a name="see-also"></a>関連項目

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)
- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [IMAPITable::FindRow](imapitable-findrow.md)
- [IMAPITable::Restrict](imapitable-restrict.md)
- [MAPI の構造](mapi-structures.md)

