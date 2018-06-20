---
title: IMAPISessionEnumAdrTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.EnumAdrTypes
api_type:
- COM
ms.assetid: 9a3702a4-8a6b-4c0c-a90f-02be3a2bfa05
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6bd13eb7180302a5ab770586cf36856ca5a22676
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800679"
---
# <a name="imapisessionenumadrtypes"></a>IMAPISession::EnumAdrTypes

  
  
**適用されます**: Outlook 
  
現在は廃止されています。 セッション内のすべてのトランスポート プロバイダーによって処理可能なアドレスの種類を返します。 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]返されるアドレスの種類の形式を示すフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> Unicode 形式では、アドレスの種類です。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のアドレスの種類です。
    
 _lpcAdrTypes_
  
> [out]_LpppszAdrTypes_パラメーターが指すアドレスの種類の数へのポインターです。 
    
 _lpppszAdrTypes_
  
> [out]アドレスの種類へのポインターの配列へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> アドレスの種類が正常に取得されました。
    
## <a name="remarks"></a>備考

**IMAPISession::EnumAdrTypes**メソッドは、セッション内のすべてのアクティブなトランスポート プロバイダーによって処理可能なアドレスの種類のリストを返します。 現在読み込まれていないトランスポート プロバイダーのアドレスの種類は、一覧には含まれません。 MAPI は、 [IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出すと、1 つまたは複数のアドレスの種類を処理するトランスポート プロバイダーを登録します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_LpppszAdrTypes_パラメーターが指す文字列の配列を解放するのには[MAPIFreeBuffer](mapifreebuffer.md)を呼び出します。 
  
## <a name="see-also"></a>関連項目



[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

