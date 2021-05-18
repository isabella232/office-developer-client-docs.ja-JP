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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 29d392eba530126e06a672c10044c5b4df0618c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406088"
---
# <a name="spropertyrestriction"></a>SPropertyRestriction

**適用対象**: Outlook 2013 | Outlook 2016 
  
定数とプロパティの値を一致するために使用されるプロパティ制限について説明します。
  
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
  
> 検索で使用される関係演算子。 指定できる値は次のとおりです。
    
  - RELOP_GE: 比較は、大きいまたは等しい最初の値に基づいて行います。
        
  - RELOP_GT: 比較は、より大きい最初の値に基づいて行います。
        
  - RELOP_LE: 比較は、より小さいか等しい最初の値に基づいて行います。
        
  - RELOP_LT: 比較は、より小さい最初の値に基づいて行います。
        
  - RELOP_NE: 比較は、等しくない値に基づいて行います。
        
  - RELOP_RE: 比較は LIKE (正規表現) の値に基づいて行います。
        
  - RELOP_EQ: 比較は、等しい値に基づいて行います。
    
**ulPropTag**
  
> 比較するプロパティを識別するプロパティ タグ。 
    
**lpProp**
  
> 比較で使用される定数値を含む [SPropValue](spropvalue.md) 構造体へのポインター。 
    
## <a name="remarks"></a>注釈

**SPropertyRestriction** 構造体には 2 つのプロパティ タグがあります。 1 つは **ulPropTag** メンバーに、もう 1 つは lpProp によって指される **SPropValue 構造体の ulPropTag** メンバー **に含されます**。  MAPI には、プロパティ識別子フィールドとプロパティの種類フィールドの両方が必要です。 **SPropertyRestriction の ulPropTag** は一致するプロパティであり **、SPropertyRestriction** の **lpProp** ポインターは **、lpProp** union のメンバー値の解釈方法を示します。    2 つのプロパティの種類が一致する必要があります。それ以外の場合は [、IMAPITable::Restrict](imapitable-restrict.md) または [IMAPITable::FindRow](imapitable-findrow.md)の呼び出しで制限が使用される場合、エラー値 MAPI_E_TOO_COMPLEX が返されます。 
  
比較順序は  _(プロパティ値) (関係演算子) (定数値) です_。
  
プロパティ制限が **IMAPITable::Restrict** または **IMAPITable::FindRow** に渡され、ターゲット プロパティが存在しない場合、制限の結果は未定義になります。 プロパティ制限と EXIST 制限を結合する **AND** 制限を作成することで、呼び出し元は正確な結果を保証できます。 [SExistRestriction](sexistrestriction.md)構造体を使用して **、EXIST** 制限と [SAndRestriction](sandrestriction.md)構造体を定義して AND 制限 **を定義** します。 
  
複数値のプロパティ タグは、テーブルを実装するサービス プロバイダーがそれらをサポートしている場合、プロパティ制限で使用できます。 サポートされている場合、複数値プロパティ タグは、単一値プロパティ タグを使用できる任意の場所で使用できます。 
  
複数値のプロパティ タグは、次のメソッドで使用できます。
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::GetProps](imapiprop-getprops.md)
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [IMAPITable::Restrict](imapitable-restrict.md)
    
> [!IMPORTANT]
> 2 つのプロパティ タグが一致しない場合の大きなケースは、複数値のプロパティを制限する場合です。 この場合、次の値を true に設定する必要があります。 > **SPropertyRestriction** の **ulPropTag** のプロパティ型に複数値プロパティ型ビット フラグ MV_FLAG (0x1000) が含まれている場合 **、SPropValue** の **ulPropTag** のプロパティ型は、前者から MV_FLAG ビット フラグを差し引いたもの、つまり逆になります。 > たとえば、プロパティ 0x8012101f のプロパティ タグを持つカテゴリ 、つまり PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012) などの複数値のカスタム文字列プロパティの使用を制限するには、対応する **SPropertyRestriction** が次のように表示されます。 >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> **SPropValue** の **ulPropTag** のプロパティの種類に MV_FLAG ビット フラグが含まれている場合、返される可能性が高MAPI_E_TOO_COMPLEX。 
  
**SPropertyRestriction** 構造の詳細については、「制限について [」を参照してください](about-restrictions.md)。 
  
## <a name="see-also"></a>関連項目

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)
- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [IMAPITable::FindRow](imapitable-findrow.md)
- [IMAPITable::Restrict](imapitable-restrict.md)
- [MAPI の構造](mapi-structures.md)

