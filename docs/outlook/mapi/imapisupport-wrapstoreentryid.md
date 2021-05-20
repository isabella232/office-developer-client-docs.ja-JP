---
title: IMAPISupportWrapStoreEntryID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.WrapStoreEntryID
api_type:
- COM
ms.assetid: 923fb879-5f32-4fe2-8920-2ec17002256c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a623ef24f76dae93bfc13e6613e885a120f3278e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430449"
---
# <a name="imapisupportwrapstoreentryid"></a>IMAPISupport::WrapStoreEntryID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストアの内部エントリ識別子を MAPI 標準形式のエントリ識別子に変換します。
  
```cpp
HRESULT WrapStoreEntryID(
ULONG cbOrigEntry,
LPENTRYID lpOrigEntry,
ULONG FAR * lpcbWrappedEntry,
LPENTRYID FAR * lppWrappedEntry
);
```

## <a name="parameters"></a>パラメーター

 _cbOrigEntry_
  
> [in]  _lpOrigEntry_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpOrigEntry_
  
> [in]メッセージ ストアのプライベート エントリ識別子へのポインター。
    
 _lpcbWrappedEntry_
  
> [out]  _lppWrappedEntry_ パラメーターが指すエントリ識別子内のバイト 数へのポインター。 
    
 _lppWrappedEntry_
  
> [out]ラップされたエントリ識別子へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> エントリ識別子が正常にラップされました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::WrapStoreEntryID** メソッドは、すべてのサービス プロバイダー サポート オブジェクトに実装されます。 サービス プロバイダーは **WrapStoreEntryID** を使用して、MAPI がストアの内部エントリ識別子をラップするメッセージ ストアのエントリ識別子を生成します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

クライアントがメッセージ ストアの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して **PR_STORE_ENTRYID** ([PidTagStoreEntryId)](pidtagstoreentryid-canonical-property.md)プロパティを取得し、メッセージ ストアでプライベート形式のエントリ識別子を使用する場合は **、WrapStoreEntryID** を呼び出し  _、lppWrappedEntry_ パラメーターが指すエントリ識別子を返します。 
  
[IMSProvider::Logon](imsprovider-logon.md)メソッドと[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)メソッドの呼び出しは、常にストアのプライベート エントリ識別子を取得します。ラップされたバージョンは、クライアント アプリケーションと MAPI の間でのみ使用されます。 
  
エントリ識別子の使用が完了したら [、MAPIFreeBuffer](mapifreebuffer.md)関数を使用して _、lppWrappedEntry_ パラメーターが指すエントリ識別子のメモリを解放します。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

