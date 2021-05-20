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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3b2e41c4b1bfc4879717df0c73bbcd45a724ca60
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439290"
---
# <a name="imapisessionenumadrtypes"></a>IMAPISession::EnumAdrTypes

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
非推奨。 セッション内のすべてのトランスポート プロバイダーが処理できるアドレスの種類を返します。 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]返されるアドレスの種類の形式を示すフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> アドレスの種類は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、アドレスの種類は ANSI 形式になります。
    
 _lpcAdrTypes_
  
> [out]  _lpppszAdrTypes_ パラメーターが指すアドレス型の数を指すポインター。 
    
 _lpppszAdrTypes_
  
> [out]アドレス型へのポインターの配列へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> アドレスの種類が正常に取得されました。
    
## <a name="remarks"></a>注釈

**IMAPISession::EnumAdrTypes** メソッドは、セッション内のすべてのアクティブなトランスポート プロバイダーが処理できるアドレスの種類の一覧を返します。 現在読み込まれていないトランスポート プロバイダーのアドレスの種類は、一覧に含まれません。 MAPI が [IXPLogon::AddressTypes](ixplogon-addresstypes.md) メソッドを呼び出す場合、トランスポート プロバイダーは 1 つ以上のアドレスの種類を処理するために登録します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

[MAPIFreeBuffer を呼](mapifreebuffer.md)び出して _、lpppszAdrTypes_ パラメーターが指す文字列配列を解放します。 
  
## <a name="see-also"></a>関連項目



[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

