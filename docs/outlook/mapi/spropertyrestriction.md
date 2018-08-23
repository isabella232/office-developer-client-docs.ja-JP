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
ms.openlocfilehash: f59b0041f271010e56dda2f73d2248f133bc1325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803978"
---
# <a name="spropertyrestriction"></a>SPropertyRestriction

**適用対象**: Outlook 
  
プロパティの値を持つ定数を一致させるために使用されるプロパティの制限について説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
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
  
> 検索に使用される関係演算子です。 使用可能な値は次のとおりです。
    
  - RELOP_GE: 比較を行うベースの最初の値が大きいか等しい。
        
  - RELOP_GT: 比較を行うベースの最初の値が大きい。
        
  - RELOP_LE: 比較を行うに基づいて最初の値が同等またはそれ以下にします。
        
  - RELOP_LT: 比較を行うベースの最初の値が小さい方です。
        
  - RELOP_NE: 比較を行うベースの値が等しくないです。
        
  - RELOP_RE: 比較を (正規表現) の値などを基に行われます。
        
  - RELOP_EQ: 比較で行われるベースの値に等しい。
    
**ulPropTag**
  
> プロパティ タグを比較するプロパティを識別します。 
    
**lpProp**
  
> 比較で使用される定数値を含む[SPropValue](spropvalue.md)構造体へのポインター。 
    
## <a name="remarks"></a>注釈

**SPropertyRestriction**構造体では、2 つのプロパティ タグがあります。 1 **ulPropTag**のメンバーで、 **lpProp**が指す**SPropValue**構造体の**ulPropTag**メンバーには、他のです。 MAPI には、プロパティの識別子フィールドとプロパティの種類] フィールドの両方が必要です。 **SPropertyRestriction**で**ulPropTag**では、対応するプロパティと**SPropValue**の**ulPropTag**の型に**SPropertyRestriction**の**lpProp**のポインターを示す方法のメンバーの値、**lpProp**共用体が解釈されます。 2 つのプロパティの型が一致する必要がありますが、そのエラー値の制限は、 [IMAPITable::Restrict](imapitable-restrict.md)または[IMAPITable::FindRow](imapitable-findrow.md)への呼び出しで使用すると MAPI_E_TOO_COMPLEX が返されます。 
  
比較の順序は、 _(プロパティの値) (関係演算子) (定数)_。
  
プロパティの制限が**IMAPITable::Restrict**または**IMAPITable::FindRow**に渡され、ターゲット プロパティが存在しない、制限の結果は定義されていません。 **既存**の制限のプロパティの制限を結合して**** の制限を作成すると、呼び出し元を正確な結果保証することができます。 [SExistRestriction](sexistrestriction.md)構造体を使用すると、**既存**の制限、**および**制限を定義するのには、 [SAndRestriction](sandrestriction.md)構造体を定義します。 
  
複数値を持つプロパティ タグは、テーブルを実装するサービス プロバイダーによってサポートされる場合、プロパティ制限で使用できます。 サポートされている場合は、複数値を持つプロパティ タグも使えます単一値プロパティ タグを使用できます。 
  
複数値を持つプロパティ タグは、次の方法で使用できます。
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::GetProps](imapiprop-getprops.md)
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [IMAPITable::Restrict](imapitable-restrict.md)
    
> [!IMPORTANT]
> 注目すべき場合は、2 つのプロパティ タグが一致しない場合は、複数値プロパティに制限する場合です。 このケースでは、次の満たす必要があります。 > **SPropValue**の**ulPropTag**のプロパティの型が以前の MV_-に一致する必要があります**SPropertyRestriction**の**ulPropTag**のプロパティの型には、複数値プロパティの型のビット フラグの MV_FLAG (0x1000) が含まれている場合、フラグのビット フラグのうち、その逆行列は、です。 > の例では、0x8012101f、PROP_TAG は、このプロパティのプロパティ タグを使用して、カテゴリなどの複数の値のカスタム文字列プロパティを使用して制限するのには (MV_FLAG | PT_UNICODE、0x8012))、対応する**SPropertyRestriction**のようになります次のとおりです。 >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> **SPropValue**の**ulPropTag**のプロパティの型に MV_FLAG ビット フラグが含まれている可能性があります戻り値が MAPI_E_TOO_COMPLEX に注意してください。 
  
**SPropertyRestriction**構造体の詳細については、[制限の詳細](about-restrictions.md)を参照してください。 
  
## <a name="see-also"></a>関連項目

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)
- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [IMAPITable::FindRow](imapitable-findrow.md)
- [IMAPITable::Restrict](imapitable-restrict.md)
- [MAPI の構造](mapi-structures.md)

