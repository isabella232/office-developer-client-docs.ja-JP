---
title: SPropValue
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropValue
api_type:
- COM
ms.assetid: faf795a2-84db-432d-a05f-082f25a5cab5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c7f4e8835831af6277cef134bf3961e9928cba33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433529"
---
# <a name="spropvalue"></a>SPropValue

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI プロパティについて説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[CHANGE_PROP_TYPE](change_prop_type.md)、 [MVI_PROP](mvi_prop.md)、 [PROP_ID](prop_id.md)、 [PROP_TAG](prop_tag.md)、 [PROP_TYPE](prop_type.md) <br/> |
   
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
  
> プロパティのプロパティタグ。 property タグは、上位16ビットのプロパティの一意の識別子と、下位16ビットのプロパティの型で構成される、32ビットの符号なし整数です。
    
 **dwAlignPad**
  
> MAPI 用に予約済み。を使用しないでください。 
    
 **値**
  
> データ値の和集合。プロパティの型によって指定される特定の値。 次の表に、使用する必要がある結合のメンバーと、関連付けられたデータ型について、各プロパティの種類の一覧を示します。
    
|**プロパティの種類**|**値**|**値のデータ型**|
|:-----|:-----|:-----|
|PT_I2 または PT_SHORT  <br/> |**i** <br/> |short int  <br/> |
|PT_I4 または PT_LONG (署名済み)  <br/> |**l** <br/> |LONG  <br/> |
|PT_I4 または PT_LONG (署名なし)  <br/> |**ul** <br/> |ULONG  <br/> |
|PT_R4 または PT_FLOAT  <br/> |**flt** <br/> |浮動小数点数  <br/> |
|PT_R8 または PT_DOUBLE  <br/> |**click** <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |**b** <br/> |符号なし short int  <br/> |
|PT_CURRENCY  <br/> |**.cur** <br/> |[CURRENCY](currency.md) <br/> |
|PT_APPTIME  <br/> |**下部** <br/> |double  <br/> |
|PT_SYSTIME  <br/> |**cm** <br/> |[FILETIME](filetime.md) <br/> |
|PT_STRING8  <br/> |**lpszA** <br/> |LPSTR  <br/> |
|PT_BINARY  <br/> |**在庫** <br/> |BYTE [配列]  <br/> |
|PT_UNICODE  <br/> |**lpszw** <br/> |LPWSTR  <br/> |
|PT_CLSID  <br/> |**lpguid** <br/> |lpguid  <br/> |
|PT_I8 または PT_LONGLONG  <br/> |**&** <br/> |**LARGE_INTEGER** <br/> |
|PT_MV_I2  <br/> |**mvi** <br/> |[SShortArray](sshortarray.md) <br/> |
|PT_MV_LONG  <br/> |**mvi** <br/> |[SLongArray](slongarray.md) <br/> |
|PT_MV_R4  <br/> |**MVflt** <br/> |[SRealArray](srealarray.md) <br/> |
|PT_MV_DOUBLE  <br/> |**MVdbl** <br/> |[SDoubleArray](sdoublearray.md) <br/> |
|PT_MV_CURRENCY  <br/> |**MVcur** <br/> |[SCurrencyArray](scurrencyarray.md) <br/> |
|PT_MV_APPTIME  <br/> |**mvat** <br/> |[SAppTimeArray](sapptimearray.md) <br/> |
|PT_MV_SYSTIME  <br/> |**MVft** <br/> |[SDateTimeArray](sdatetimearray.md) <br/> |
|PT_MV_BINARY  <br/> |**mvbin** <br/> |[SBinaryArray](sbinaryarray.md) <br/> |
|PT_MV_STRING8  <br/> |**MVszA** <br/> |[SLPSTRArray](slpstrarray.md) <br/> |
|PT_MV_UNICODE  <br/> |**MVszW** <br/> |[SWStringArray](swstringarray.md) <br/> |
|PT_MV_CLSID  <br/> |**MVguid** <br/> |[SGuidArray](sguidarray.md) <br/> |
|PT_MV_I8  <br/> |**MVli** <br/> |[SLargeIntegerArray](slargeintegerarray.md) <br/> |
|PT_ERROR  <br/> |**err** <br/> |[SCODE](scode.md) <br/> |
|PT_NULL または PT_OBJECT  <br/> |**x** <br/> |LONG  <br/> |
|PT_PTR  <br/> |**lpv** <br/> |VOID\*  <br/> |
   
## <a name="remarks"></a>注釈

**ulPropTag**メンバーは、次の2つの部分で構成されます。 
  
- 上位16ビットの識別子。
    
- ローオーダー16ビットの型。
    
識別子は、特定の範囲内の数値です。 MAPI は、識別子の範囲を定義して、プロパティがどのように使用され、保持する責任者を示します。 MAPI は、Mapitags ヘッダーファイルでサポートされている各プロパティタグに対する制約を定義します。
  
この型は、プロパティの値の形式を示します。 MAPI は、mapidefs.h ヘッダーファイルでサポートされている各プロパティの種類に対して定数を定義します。 
  
識別子およびプロパティの種類の有効なプロパティ範囲の完全な一覧については、「付録」の「[プロパティの識別子と種類](property-identifiers-and-types.md)」を参照してください。 
  
**dwAlignPad**メンバーは、8バイト値の8バイト配置を必要とするコンピューターで適切に配置されるように、パディングとして使用されます。 このようなコンピューターでコードを記述する開発者は、8バイト境界に**spropvalue**配列を割り当てるメモリ割り当てルーチンを使用する必要があります。 
  
詳細については、「 [mapi プロパティの種類の概要](mapi-property-type-overview.md)」および「 [mapi プロパティの更新](updating-mapi-properties.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目



[MAPI の構造](mapi-structures.md)

