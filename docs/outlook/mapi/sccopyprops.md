---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1afd922459be2ec4bbbd27a61fdf6fcb425548c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411009"
---
# <a name="sccopyprops"></a>ScCopyProps

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[spropvalue](spropvalue.md)構造体の配列によって定義されたプロパティを新しい宛先にコピーします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
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
  
> 順番コピーするプロパティの数を指定します。 
    
 _rgprop_
  
> 順番コピーするプロパティを定義する[spropvalue](spropvalue.md)構造体の配列へのポインター。 _rgprop_パラメーターは、配列の先頭をポイントする必要はありませんが、配列内のいずれかの**spropvalue**構造体の先頭を指す必要があります。 
    
 _pvdst_
  
> 順番この関数がプロパティをコピーするメモリ内の初期位置へのポインター。 
    
 _設計_
  
> 読み上げ(オプション) _pvdst_パラメーターによって示されるメモリブロックのサイズ (バイト単位) を指すポインターです。 
    
## <a name="return-value"></a>戻り値

S_OK
  
> プロパティが正常にコピーされました。
    
MAPI_E_INVALID_PARAMETER
  
> 不明なプロパティの種類が検出されました。
    
## <a name="remarks"></a>注釈

新しい配列とそのデータは、1つの割り当てで作成されたバッファーに存在し、 [ScRelocProps](screlocprops.md)関数を使用して、個々の[spropvalue](spropvalue.md)構造内のポインターを調整できます。 この調整の前に、ポインターが有効になります。 
  
 **sccopyprops**は、コピーされたプロパティ配列の元のプロパティの順序を保持します。 
  
_pcb_パラメーターはオプションです。NULL でない場合は、 _pvdst_パラメーターに格納されているバイト数に設定されます。 
  
## <a name="see-also"></a>関連項目



[ScDupPropset](scduppropset.md)

