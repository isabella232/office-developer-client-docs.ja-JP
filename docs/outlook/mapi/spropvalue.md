---
title: SPropValue
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SPropValue
api_type:
- COM
ms.assetid: faf795a2-84db-432d-a05f-082f25a5cab5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f0b26c5d0ef2906945becbfe4dd121d10831ca05
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566529"
---
# <a name="spropvalue"></a>SPropValue

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI プロパティについて説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[CHANGE_PROP_TYPE](change_prop_type.md)、 [MVI_PROP](mvi_prop.md) [、](prop_id.md)PROP_ID [、](prop_tag.md)PROP_TAG [、](prop_type.md) PROP_TYPE <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a>メンバー

 **ulPropTag**
  
> プロパティのプロパティ タグ。 プロパティ タグは、高次 16 ビットのプロパティの一意識別子と、低次 16 ビットのプロパティの型で構成される 32 ビットの符号なし整数です。
    
 **dwAlignPad**
  
> MAPI 用に予約されています。使用しない。 
    
 **値**
  
> データ値の共用体、プロパティの種類によって決まる特定の値。 次の表に、各プロパティの種類、使用する共用体のメンバー、および関連するデータ型を示します。
    
|**プロパティの種類**|**値**|**Value のデータ型**|
|:-----|:-----|:-----|
|PT_I2またはPT_SHORT  <br/> |**i** <br/> |short int  <br/> |
|PT_I4またはPT_LONG (署名済み)  <br/> |**l** <br/> |LONG  <br/> |
|PT_I4またはPT_LONG (符号なし)  <br/> |**ul** <br/> |ULONG  <br/> |
|PT_R4またはPT_FLOAT  <br/> |**flt** <br/> |浮動小数点数  <br/> |
|PT_R8またはPT_DOUBLE  <br/> |**dbl** <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |**b** <br/> |符号なし short int  <br/> |
|PT_CURRENCY  <br/> |**cur** <br/> |[CURRENCY](currency.md) <br/> |
|PT_APPTIME  <br/> |**at** <br/> |double  <br/> |
|PT_SYSTIME  <br/> |**ft** <br/> |[FILETIME](filetime.md) <br/> |
|PT_STRING8  <br/> |**lpszA** <br/> |LPSTR  <br/> |
|PT_BINARY  <br/> |**bin** <br/> |BYTE [配列]  <br/> |
|PT_UNICODE  <br/> |**lpszW** <br/> |LPWSTR  <br/> |
|PT_CLSID  <br/> |**lpguid** <br/> |LPGUID  <br/> |
|PT_I8またはPT_LONGLONG  <br/> |**li** <br/> |**LARGE_INTEGER** <br/> |
|PT_MV_I2  <br/> |**MVi** <br/> |[SShortArray](sshortarray.md) <br/> |
|PT_MV_LONG  <br/> |**MVI** <br/> |[SLongArray](slongarray.md) <br/> |
|PT_MV_R4  <br/> |**MVflt** <br/> |[SRealArray](srealarray.md) <br/> |
|PT_MV_DOUBLE  <br/> |**MVdbl** <br/> |[SDoubleArray](sdoublearray.md) <br/> |
|PT_MV_CURRENCY  <br/> |**MVcur** <br/> |[SCurrencyArray](scurrencyarray.md) <br/> |
|PT_MV_APPTIME  <br/> |**MVat** <br/> |[SAppTimeArray](sapptimearray.md) <br/> |
|PT_MV_SYSTIME  <br/> |**MVft** <br/> |[SDateTimeArray](sdatetimearray.md) <br/> |
|PT_MV_BINARY  <br/> |**MVbin** <br/> |[SBinaryArray](sbinaryarray.md) <br/> |
|PT_MV_STRING8  <br/> |**MVszA** <br/> |[SLPSTRArray](slpstrarray.md) <br/> |
|PT_MV_UNICODE  <br/> |**MVszW** <br/> |[SWStringArray](swstringarray.md) <br/> |
|PT_MV_CLSID  <br/> |**MVguid** <br/> |[SGuidArray](sguidarray.md) <br/> |
|PT_MV_I8  <br/> |**MVli** <br/> |[SLargeIntegerArray](slargeintegerarray.md) <br/> |
|PT_ERROR  <br/> |**err** <br/> |[SCODE](scode.md) <br/> |
|PT_NULLまたはPT_OBJECT  <br/> |**x** <br/> |LONG  <br/> |
|PT_PTR  <br/> |**lpv** <br/> |VOID \*  <br/> |
   
## <a name="remarks"></a>注釈

**ulPropTag メンバー** は、次の 2 つの部分で構成されます。 
  
- 高次 16 ビットの識別子。
    
- 低次 16 ビットの型。
    
識別子は、特定の範囲内の数値です。 MAPI では、プロパティの使用および管理の責任者を示す識別子の範囲を定義します。 MAPI は、Mapitags.h ヘッダー ファイルでサポートする各プロパティ タグの制約を定義します。
  
型は、プロパティの値の形式を示します。 MAPI は、Mapidefs.h ヘッダー ファイルでサポートする各プロパティの種類の定数を定義します。 
  
識別子とプロパティ型の有効なプロパティ範囲の完全な一覧については、付録「プロパティ識別子と型」 [を参照](property-identifiers-and-types.md) してください。 
  
**dwAlignPad メンバー** は、8 バイト値に対して 8 バイトの配置を必要とするコンピューター上で適切な配置を行うパディングとして使用されます。 このようなコンピューターでコードを記述する開発者は、8 バイト境界に **SPropValue** 配列を割り当てるメモリ割り当てルーチンを使用する必要があります。 
  
詳細については、「MAPI プロパティの [種類の概要」および「MAPI](mapi-property-type-overview.md) [プロパティの更新」を参照してください](updating-mapi-properties.md)。 
  
## <a name="see-also"></a>関連項目



[MAPI の構造](mapi-structures.md)

