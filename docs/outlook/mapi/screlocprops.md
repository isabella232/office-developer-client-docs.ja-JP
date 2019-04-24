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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c73fb96c9620a90ab0505b394fcb9853d02dcde5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360691"
---
# <a name="screlocprops"></a>ScRelocProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
配列とそのデータが新しい場所にコピーまたは移動された後に、 [spropvalue](spropvalue.md)配列内のポインターを調整します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
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
  
> 順番_rgprop_パラメーターによって参照される、配列内のプロパティの数。 
    
 _rgprop_
  
> 順番ポインターを調整する[spropvalue](spropvalue.md)構造体の配列へのポインター。 
    
 _pvbaseold_
  
> 順番_rgprop_パラメーターによって参照される配列の元のベースアドレスへのポインター。 
    
 _pvBaseNew_
  
> 順番_rgprop_パラメーターによって参照される配列の新しいベースアドレスへのポインター。 
    
 _設計_
  
> [入力]_pvBaseNew_パラメーターで指定された配列のサイズをバイト単位で示すオプションのポインターです。 NULL でない場合、 _pcb_パラメーターは_pvD_パラメータに格納されているバイト数に設定されます。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> ポインターが正常に調整されました。
    
MAPI_E_INVALID_PARAMETER
  
> 1つまたは両方のパラメーターが無効であったか、不明なプロパティの種類が検出されました。
    
## <a name="remarks"></a>解説

**ScRelocProps**関数は、ポインターが調整されているプロパティ値の配列が、 **sccopyprops**関数の呼び出しと同じように、1つの呼び出しで最初に割り当てられたことを前提としています。 クライアントアプリケーションまたはサービスプロバイダーが、メモリのないブロックから構築されたプロパティ値を処理している場合は、 [sccopyprops](sccopyprops.md)を使用してプロパティをコピーする必要があります。 
  
 **ScRelocProps**は、 [spropvalue](spropvalue.md)配列内のポインターの有効性を維持するために使用されます。 このような配列を書き込み、ディスクから読み取る際にポインターの有効性を維持するには、次の操作を行います。 
  
1. 配列とデータをディスクに書き込む前に、 _pvBaseNew_パラメーターを指定した配列の**ScRelocProps**を、たとえば、何らかの標準値ゼロを指定して呼び出します。 
    
2. ディスクから配列とデータを読み取った後、手順1で使用したのと同じ標準値に等しい_pvbaseold_パラメーターを持つ配列で**ScRelocProps**を呼び出します。 配列とデータは、1つの割り当てで作成されたバッファーに読み込む必要があります。 
    
3. **ScRelocProps**の_pcb_パラメーターはオプションです。 
    
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ScCountProps](sccountprops.md)
  
[ScDupPropset](scduppropset.md)
  
[ScRelocNotifications](screlocnotifications.md)

