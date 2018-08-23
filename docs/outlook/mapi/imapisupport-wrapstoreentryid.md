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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b3850da2917dbf463590643b9e7ba8420f4ea219
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576058"
---
# <a name="imapisupportwrapstoreentryid"></a>IMAPISupport::WrapStoreEntryID

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI の標準的な形式のエントリ id をメッセージ ・ ストアの内部のエントリの識別子に変換します。
  
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
  
> [in]_LpOrigEntry_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpOrigEntry_
  
> [in]メッセージ ・ ストアのプライベート エントリの識別子へのポインター。
    
 _lpcbWrappedEntry_
  
> [out]_LppWrappedEntry_パラメーターで指定されたエントリの識別子のバイト数へのポインター。 
    
 _lppWrappedEntry_
  
> [out]ラップされたエントリの識別子へのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> エントリ id が正常に折り返されます。
    
## <a name="remarks"></a>注釈

サービス プロバイダーのサポートのすべてのオブジェクトの**IMAPISupport::WrapStoreEntryID**メソッドを実装します。 サービス プロバイダーは、ストアの内部のエントリの識別子をラップするメッセージ ・ ストアのエントリ識別子を生成する MAPI を使用して**WrapStoreEntryID**を使用します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) のプロパティと、メッセージ ストアを取得するためにプライベートの形式で、エントリ id を使用して、クライアントが、メッセージ ・ ストアの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すときは、 **WrapStoreEntryID を呼び出す**し、 _lppWrappedEntry_パラメーターで指定されたエントリの識別子を返します。 
  
[IMSProvider::Logon](imsprovider-logon.md)と[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)メソッドの呼び出しは常にストアのプライベート エントリの識別子を取得します。ラップのバージョンは、クライアント アプリケーションと MAPI の間でのみ使用されます。 
  
エントリの識別子を使用してが完了したら、 [MAPIFreeBuffer](mapifreebuffer.md)関数を使用して、 _lppWrappedEntry_パラメーターで示されるエントリ id 用のメモリを解放します。 
  
## <a name="see-also"></a>関連項目



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[IMSLogon::CompareEntryIDs](imslogon-compareentryids.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

