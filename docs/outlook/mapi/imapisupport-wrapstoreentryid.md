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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341287"
---
# <a name="imapisupportwrapstoreentryid"></a>IMAPISupport::WrapStoreEntryID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアの内部エントリ識別子を MAPI 標準形式のエントリ id に変換します。
  
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
  
> 順番_lporigentry_パラメーターによって指摘されたエントリ識別子のバイト数。 
    
 _lporigentry_
  
> 順番メッセージストアのプライベートエントリ識別子へのポインター。
    
 _lpcbWrappedEntry_
  
> 読み上げ_lppWrappedEntry_パラメーターによって示されるエントリ識別子のバイト数へのポインター。 
    
 _lppWrappedEntry_
  
> 読み上げラップされたエントリ識別子へのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> エントリ識別子が正常にラップされました。
    
## <a name="remarks"></a>解説

**imapisupport:: WrapStoreEntryID**メソッドは、すべてのサービスプロバイダーサポートオブジェクトに実装されています。 サービスプロバイダーは**WrapStoreEntryID**を使用して、ストアの内部エントリ識別子をラップするメッセージストアのエントリ識別子を MAPI で生成します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

クライアントがメッセージストアの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) プロパティを取得し、メッセージストアがプライベート形式のエントリ識別子を使用する場合は、WrapStoreEntryID を呼び出します。 **** を指定し、 _lppWrappedEntry_パラメーターで指定されたエントリ識別子を返します。 
  
[IMSProvider:: Logon](imsprovider-logon.md)および[IMSLogon:: compareentryids](imslogon-compareentryids.md)メソッドの呼び出しは、常にストアの秘密エントリ識別子を取得します。ラップされたバージョンは、クライアントアプリケーションと MAPI 間でのみ使用されます。 
  
エントリ識別子の使用が終了したら、 [MAPIFreeBuffer](mapifreebuffer.md)関数を使用して、 _lppWrappedEntry_パラメーターで指定されたエントリ識別子のメモリを解放します。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

