---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9f4b69c62f78805e93f28db73691830515997fa3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586790"
---
# <a name="sccopyprops"></a>ScCopyProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[SPropValue](spropvalue.md)構造体の配列で定義されたプロパティを新しい宛先にコピーします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>パラメーター

 _cprop_
  
> [in]コピーするプロパティの数。 
    
 _rgprop_
  
> [in]コピーするプロパティを [定義する SPropValue](spropvalue.md) 構造体の配列へのポインター。 _rgprop パラメーター_ は、配列の先頭を指す必要はないが、配列内の **SPropValue** 構造体の 1 つの先頭を指している必要があります。 
    
 _pvDst_
  
> [in]この関数がプロパティをコピーするメモリ内の初期位置へのポインター。 
    
 _pcb_
  
> [out]  _pvDst_ パラメーターが指すメモリ ブロックのサイズ (バイト単位) へのオプションのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> プロパティが正常にコピーされました。
    
MAPI_E_INVALID_PARAMETER
  
> 不明なプロパティの種類が検出されました。
    
## <a name="remarks"></a>注釈

新しい配列とそのデータは、1 つの割り当てで作成されたバッファー内に存在し [、ScRelocProps](screlocprops.md) 関数を使用して、個々の [SPropValue](spropvalue.md) 構造体のポインターを調整できます。 この調整の前に、ポインターは有効です。 
  
 **ScCopyProps は** 、コピーされたプロパティ配列の元のプロパティの順序を維持します。 
  
_pcb パラメーター_ は省略可能です。NULL 以外の場合は _、pvDst_ パラメーターに格納されているバイト数に設定されます。 
  
## <a name="see-also"></a>関連項目



[ScDupPropset](scduppropset.md)

