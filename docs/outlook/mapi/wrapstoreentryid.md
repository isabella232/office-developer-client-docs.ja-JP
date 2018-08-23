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
ms.openlocfilehash: 45263396e69852a9ae17ff6fce284663bdf2fb07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585137"
---
# <a name="wrapstoreentryid"></a>WrapStoreEntryID

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージング システムがメッセージ ストアの内部のエントリの識別子をより使用可能なエントリ id に変換します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
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

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]フラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> 文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。 
    
 _szDLLName_
  
> [in]メッセージ ストア プロバイダーの DLL の名前。 
    
 _cbOrigEntry_
  
> [in]メッセージ ・ ストアの元のエントリ id のバイト単位のサイズです。 
    
 _lpOrigEntry_
  
> [in]元のエントリ id が含まれている[エントリ ID](entryid.md)の構造体へのポインター。 
    
 _lpcbWrappedEntry_
  
> [out]バイト単位で、新しいエントリ id のサイズへのポインター。 
    
 _lppWrappedEntry_
  
> [out]新しいエントリの識別子を含む**エントリ ID**の構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

メッセージ ストアのオブジェクトは、そのメッセージ ・ ストアのサービス プロバイダーの coresident にのみ意味を持つエントリの内部識別子を保持します。 その他のメッセージング コンポーネントでは、MAPI には、ラップされたメッセージ ・ ストアに属していると認識可能な内部のエントリ id のバージョンが用意されています。 Coresident サービス ・ プロバイダーは常に指定する元のラップが解除されたメッセージ ストアのエントリ id です。クライアント アプリケーションは、常にでは、その使用可能な任意の場所のメッセージング ドメインと他のドメインに、ラップされたバージョンを指定してする必要があります。 
  
サービス プロバイダーは、 **WrapStoreEntryID**関数または**WrapStoreEntryID**関数を呼び出し、 [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md)メソッドのいずれかを使用して、メッセージ ストアのエントリの識別子を折り返すことができます。 プロバイダーはメッセージ ストアの**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) を公開するときのエントリ id をラップする必要がありますプロパティまたは書き込みを行うことと、[プロファイル] セクションに**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) を公開するときにプロパティです。 [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)の呼び出しに応答する場合、MAPI は、メッセージ ストアのエントリの識別子をラップします。 
  
クライアント アプリケーションでは、MAPI にラップされたメッセージ ストアのエントリの識別子を渡しますと、の呼び出しでは、 [IMAPISession::OpenEntry](imapisession-openentry.md) MAPI のラップを解除のエントリ id [IMSProvider::Logon](imsprovider-logon.md)や[などのプロバイダーのメソッドを呼び出すために使用する前にIMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md)。 
  

