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
ms.openlocfilehash: 06590fe55cb02b1abf036156877fd308548436f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803864"
---
# <a name="screlocprops"></a>ScRelocProps

  
  
**適用対象**: Outlook 
  
[SPropValue](spropvalue.md)配列のポインターは、配列とそのデータがコピーまたは新しい場所に移動された後に調整します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
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
  
> [in]_Rgprop_パラメーターが指す配列内のプロパティの数です。 
    
 _rgprop_
  
> [in]ポインターが調整するのには[SPropValue](spropvalue.md)構造体の配列へのポインター。 
    
 _pvBaseOld_
  
> [in]_Rgprop_パラメーターが指す配列の元のベース アドレスへのポインターです。 
    
 _pvBaseNew_
  
> [in]_Rgprop_パラメーターが指す配列の新しいベース アドレスへのポインターです。 
    
 _pcb_
  
> [で [チェック アウト]ポインターを_pvBaseNew_パラメーターで指定された配列のバイト単位のサイズを指します。 設定されていない場合 NULL の場合、 _pcb_のパラメーターは_pvD_パラメーターに格納されるバイトの数です。 
    
## <a name="return-value"></a>�߂�l

S_OK
  
> ポインターが正常に調整されました。
    
MAPI_E_INVALID_PARAMETER
  
> 1 つまたは両方のパラメーターが有効でなかったか、不明なプロパティの種類が発生しました。
    
## <a name="remarks"></a>注釈

**ScRelocProps**関数は、ポインターが調整のプロパティ値の配列が最初に割り当てられたの**ScCopyProps**関数の呼び出しのような 1 つの呼び出しであるという前提で動作します。 切り離されたメモリ ブロックから構築されたプロパティの値では、クライアント アプリケーションまたはサービス プロバイダーが動作している場合は、代わりにプロパティをコピーするのには[ScCopyProps](sccopyprops.md)を使用してください。 
  
 [SPropValue](spropvalue.md)配列内のポインターの有効性を維持するために**ScRelocProps**が使用されます。 ポインターの有効性を保つためにそのような配列を書き込むと、ディスクから読み込むには、次の操作を実行します。 
  
1. アレイとのデータをディスクに書き出す前に、アレイ上のいくつか標準的な値が 0 を指す_pvBaseNew_パラメーターを使用して**ScRelocProps**を呼び出します。 
    
2. アレイとのデータをディスクから読み取り後を呼び出す**ScRelocProps** 、 _pvBaseOld_パラメーターを使用してアレイに手順 1 で使用される同じ標準的な値に等しい。 配列およびデータは、1 つの割り当てで作成されたバッファーに読み取る必要があります。 
    
3. **ScRelocProps** _pcb_のパラメーターはオプションです。 
    
## <a name="see-also"></a>関連項目



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ScCountProps](sccountprops.md)
  
[ScDupPropset](scduppropset.md)
  
[ScRelocNotifications](screlocnotifications.md)

