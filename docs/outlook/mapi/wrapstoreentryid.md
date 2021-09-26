---
title: WrapStoreEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- WrapStoreEntryID
api_type:
- HeaderDef
ms.assetid: b20107e3-5e23-4cde-9cd6-670c914ea70a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ef6286738be70ee3e2d91d32df9635f25df0a6c7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583234"
---
# <a name="wrapstoreentryid"></a>WrapStoreEntryID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストアの内部エントリ識別子を、メッセージング システムで使用できるエントリ識別子に変換します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
WrapStoreEntryID(
  ULONG ulFlags,
  LPSTR szDLLName,
  ULONG cbOrigEntry,
  LPENTRYID lpOrigEntry,
  ULONG * lpcbWrappedEntry,
  LPENTRYID * lppWrappedEntry
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]フラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。 
    
 _szDLLName_
  
> [in]メッセージ ストア プロバイダー DLL の名前。 
    
 _cbOrigEntry_
  
> [in]メッセージ ストアの元のエントリ識別子のサイズ (バイト単位)。 
    
 _lpOrigEntry_
  
> [in]元のエントリ [識別子を](entryid.md) 含む ENTRYID 構造体へのポインター。 
    
 _lpcbWrappedEntry_
  
> [out]新しいエントリ識別子のサイズ (バイト単位) へのポインター。 
    
 _lppWrappedEntry_
  
> [out]新しいエントリ識別子を含 **む ENTRYID** 構造体へのポインターを指すポインター。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

メッセージ ストア オブジェクトは内部エントリ識別子を保持します。これは、そのメッセージ ストアを持つサービス プロバイダーの coresident にとってのみ意味があります。 その他のメッセージング コンポーネントの場合、MAPI は、メッセージ ストアに属すると認識できる、ラップされたバージョンの内部エントリ識別子を提供します。 Coresident サービス プロバイダーには、常に元のラップされていないメッセージ ストア エントリ識別子を指定する必要があります。クライアント アプリケーションには、常にラップされたバージョンを指定する必要があります。その後、メッセージング ドメイン内および他のドメインの任意の場所で使用できます。 
  
サービス プロバイダーは **、WrapStoreEntryID 関数または WRAPStoreEntryID** 関数を呼び出す [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)メソッドを使用して、メッセージ ストアエントリ識別子をラップできます。  プロバイダーは、メッセージ ストア **の PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを公開する場合、またはプロファイル セクションに書き込む場合、および **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) プロパティを公開するときに、エントリ識別子をラップする必要があります。 MAPI は [、IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) 呼び出しに応答するときにメッセージ ストアエントリ識別子をラップします。 
  
クライアント アプリケーションが [、IMAPISession::OpenEntry](imapisession-openentry.md) 呼び出しなど、ラップされたメッセージ ストアエントリ識別子を MAPI に渡す場合、MAPI はエントリ識別子をアンラップしてから、そのエントリ識別子を使用して [IMSProvider::Logon](imsprovider-logon.md) や [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md)などのプロバイダー メソッドを呼び出します。 
  

