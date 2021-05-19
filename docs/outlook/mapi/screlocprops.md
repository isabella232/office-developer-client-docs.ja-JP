---
title: ScRelocProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocProps
api_type:
- COM
ms.assetid: 4aafb254-6074-4a7c-b915-d3d33304ac38
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c73fb96c9620a90ab0505b394fcb9853d02dcde5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421089"
---
# <a name="screlocprops"></a>ScRelocProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
配列とそのデータがコピーまたは新しい場所に移動された後 [、SPropValue](spropvalue.md) 配列内のポインターを調整します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>パラメーター

 _cprop_
  
> [in]  _rgprop_ パラメーターが指す配列内のプロパティの数。 
    
 _rgprop_
  
> [in]ポインターを調整する [SPropValue](spropvalue.md) 構造体の配列へのポインター。 
    
 _pvBaseOld_
  
> [in]  _rgprop_ パラメーターが指す配列の元のベース アドレスへのポインター。 
    
 _pvBaseNew_
  
> [in]  _rgprop_ パラメーターが指す配列の新しいベース アドレスへのポインター。 
    
 _pcb_
  
> [in, out]  _pvBaseNew_ パラメーターで示される配列のサイズ (バイト単位) へのオプションのポインター。 NULL 以外の場合  _、pcb_ パラメーターは pvD パラメーターに格納されているバイト数  _に設定_ されます。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> ポインターが正常に調整されました。
    
MAPI_E_INVALID_PARAMETER
  
> 1 つまたは両方のパラメーターが無効であるか、不明なプロパティの種類が検出されました。
    
## <a name="remarks"></a>注釈

**ScRelocProps** 関数は、ポインターが調整されるプロパティ値配列が **、ScCopyProps** 関数の呼び出しと同様の 1 回の呼び出しで最初に割り当てられたという前提で動作します。 クライアント アプリケーションまたはサービス プロバイダーが、バラバラのメモリ ブロックから構築されたプロパティ値を使用している場合は [、ScCopyProps](sccopyprops.md) を使用して代わりにプロパティをコピーする必要があります。 
  
 **ScRelocProps は**[、SPropValue](spropvalue.md)配列内のポインターの有効性を維持するために使用されます。 このような配列をディスクに書き込んでディスクから読み取る際にポインターの有効性を維持するには、次の操作を実行します。 
  
1. 配列とデータをディスクに書き込む前に、_たとえば、標準_ 値 0 を指す pvBaseNew パラメーターを使用して、配列の **ScRelocProps** を呼び出します。 
    
2. ディスクから配列とデータを読み取った後、手順 1 で使用した標準値と同じ pvBaseOld パラメーターを使用して、配列の **ScRelocProps** を呼び出します。  配列とデータは、1 つの割り当てで作成されたバッファーに読み込む必要があります。 
    
3. **ScRelocProps への pcb パラメーターは** オプションです。  
    
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ScCountProps](sccountprops.md)
  
[ScDupPropset](scduppropset.md)
  
[ScRelocNotifications](screlocnotifications.md)

