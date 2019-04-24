---
title: WrapStoreEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WrapStoreEntryID
api_type:
- HeaderDef
ms.assetid: b20107e3-5e23-4cde-9cd6-670c914ea70a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e797a80cf8659baa7ca935f94b3ab65c200530a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325670"
---
# <a name="wrapstoreentryid"></a>WrapStoreEntryID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアの内部エントリ識別子を、メッセージングシステムによって使用可能なエントリ id に変換します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
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
  
> 順番フラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 文字列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。 
    
 _szDLLName_
  
> 順番メッセージストアプロバイダー DLL の名前。 
    
 _cbOrigEntry_
  
> 順番メッセージストアの元のエントリ識別子のサイズ (バイト単位)。 
    
 _lporigentry_
  
> 順番元のエントリ識別子を含む[ENTRYID](entryid.md)構造体へのポインター。 
    
 _lpcbWrappedEntry_
  
> 読み上げ新しいエントリ識別子のサイズ (バイト単位) へのポインター。 
    
 _lppWrappedEntry_
  
> 読み上げ新しいエントリ識別子を含む**ENTRYID**構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>解説

メッセージストアオブジェクトは、そのメッセージストアとのサービスプロバイダ coresident にのみ意味がある内部エントリ識別子を保持します。 その他のメッセージングコンポーネントの場合、MAPI は、メッセージストアに属しているものとして認識できるようにするために、ラップされたバージョンの内部エントリ識別子を提供します。 coresident サービスプロバイダーには、必ず、元のラップされていないメッセージストアエントリ識別子を指定する必要があります。クライアントアプリケーションには常にラップされたバージョンが指定されている必要があります。これは、メッセージングドメインとその他のドメイン内の任意の場所で使用できます。 
  
サービスプロバイダーは、 **WrapStoreEntryID**関数または[imapisupport:: WrapStoreEntryID](imapisupport-wrapstoreentryid.md)メソッドのいずれかを使用して、メッセージストアエントリ識別子をラップできます。このメソッドは、 **WrapStoreEntryID**関数を呼び出します。 プロバイダーは、メッセージストアの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) プロパティを公開するか、プロファイルセクションに書き込むとき、および**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) を公開するときに、エントリ識別子をラップする必要があります。プロパティ. MAPI は、 [imapisession:: openmsgstore](imapisession-openmsgstore.md)呼び出しに応答するときに、メッセージストアエントリ識別子をラップします。 
  
クライアントアプリケーションが、ラップされたメッセージストアエントリ識別子を mapi に渡すと ( [imapisession:: openentry](imapisession-openentry.md)呼び出しなど)、mapi は、 [IMSProvider:: Logon](imsprovider-logon.md) [などのプロバイダーメソッドを呼び出す前に、エントリ識別子をラップします。IMSProvider:: comparestoreids](imsprovider-comparestoreids.md)。 
  

