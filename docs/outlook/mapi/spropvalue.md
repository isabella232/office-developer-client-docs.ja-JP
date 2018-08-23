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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f378bdd473410b846328cbe1f911eba9401f88cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804003"
---
# <a name="spropvalue"></a>SPropValue

  
  
**適用対象**: Outlook 
  
MAPI プロパティをについて説明します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|関連するマクロ:  <br/> |[CHANGE_PROP_TYPE](change_prop_type.md)、 [MVI_PROP](mvi_prop.md)、 [PROP_ID](prop_id.md)、 [PROP_TAG](prop_tag.md)、 [PROP_TYPE](prop_type.md) <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a>Members

 **ulPropTag**
  
> プロパティのプロパティ タグです。 プロパティ タグは、プロパティの一意の識別子の上位 16 ビットと下位の 16 ビットのプロパティの型で構成される 32 ビットの符号なし整数です。
    
 **dwAlignPad**
  
> MAPI のために予約使用しません。 
    
 **値**
  
> 共用体データの値の特定の値をプロパティの型によって決まります。 次の表は、各プロパティの種類、使用する共用体のメンバーとその関連するデータ型の一覧です。
    
|**プロパティの種類**|**値**|**値のデータ型**|
|:-----|:-----|:-----|
|PT_I2 または PT_SHORT  <br/> |**i** <br/> |短い int  <br/> |
|PT_I4 または PT_LONG を (符号付き)  <br/> |**l** <br/> |長  <br/> |
|PT_I4 または PT_LONG の (符号なし)  <br/> |**ul** <br/> |ULONG  <br/> |
|PT_R4 または PT_FLOAT  <br/> |**flt** <br/> |浮動小数点数  <br/> |
|PT_R8 または PT_DOUBLE  <br/> |**複列** <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |**b** <br/> |符号なし短整数  <br/> |
|PT_CURRENCY  <br/> |**cur** <br/> |[CURRENCY](currency.md) <br/> |
|PT_APPTIME  <br/> |**で** <br/> |double  <br/> |
|PT_SYSTIME  <br/> |**ft** <br/> |[FILETIME](filetime.md) <br/> |
|PT_STRING8  <br/> |**lpszA** <br/> |LPSTR  <br/> |
|PT_BINARY  <br/> |**箱** <br/> |バイト [配列]  <br/> |
|PT_UNICODE  <br/> |**lpszW** <br/> |LPWSTR  <br/> |
|PT_CLSID  <br/> |**lpguid** <br/> |LPGUID  <br/> |
|PT_I8 または PT_LONGLONG  <br/> |**li** <br/> |**LARGE_INTEGER** <br/> |
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
|PT_NULL または PT_OBJECT  <br/> |**x** <br/> |長  <br/> |
|PT_PTR  <br/> |**lpv** <br/> |VOID\*  <br/> |
   
## <a name="remarks"></a>注釈

**UlPropTag**メンバーは、2 つの部分で構成されています。 
  
- 上位 16 ビットの識別子です。
    
- 下位 16 ビットのタイプです。
    
識別子は、特定の範囲内の数値です。 MAPI は、プロパティの使用および保守の責任者を記述する識別子の範囲を定義します。 MAPI では、Mapitags.h ヘッダー ファイルでサポートされているプロパティ タグのそれぞれの制約を定義します。
  
型は、プロパティの値の形式を示します。 MAPI では、Mapidefs.h ヘッダー ファイルでサポートされているプロパティの型のそれぞれの定数を定義します。 
  
識別子とプロパティの型のプロパティの有効な範囲の一覧については、[プロパティの識別子と型](property-identifiers-and-types.md)の付録を参照してください。 
  
**DwAlignPad**メンバーは、8 バイトの値を 8 バイトのアライメントが必要なコンピューターに確実に適切なアライメントを作成する、スペースとして使用されます。 このようなコンピューター上のコードを記述する開発者は、8 バイト境界に**SPropValue**の配列を割り当てるメモリ割り当てルーチンを使用してください。 
  
詳細については、 [MAPI プロパティの種類の概要](mapi-property-type-overview.md)と、 [MAPI プロパティの更新](updating-mapi-properties.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[MAPI の構造](mapi-structures.md)

