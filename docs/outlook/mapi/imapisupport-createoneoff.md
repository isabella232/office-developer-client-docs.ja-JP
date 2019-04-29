---
title: imapisupportcreateoneoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CreateOneOff
api_type:
- COM
ms.assetid: ee57d6e0-9de0-4427-97ce-371c1c01f3de
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9571d51e01c2d58d9b8a9a913ba2c210ae0bd44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411996"
---
# <a name="imapisupportcreateoneoff"></a>IMAPISupport::CreateOneOff

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1回限りのアドレスのエントリ id を作成します。
  
```cpp
HRESULT CreateOneOff(
  LPSTR lpszName,
  LPSTR lpszAdrType,
  LPSTR lpszAddress,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>パラメーター

 _lpszname_
  
> 順番**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティの受信者の表示名へのポインター。 _lpszname_パラメーターには NULL を指定できます。 
    
 _lpszadrtype_
  
> 順番受信者のアドレスの種類 (FAX、SMTP、または X500 など) へのポインター。 _lpszadrtype_パラメーターを NULL にすることはできません。 
    
 _lpszaddress_
  
> 順番受信者のメッセージアドレスへのポインター。 _lpszaddress_パラメーターを NULL にすることはできません。 
    
 _ulFlags_
  
> 順番1回限りの受信者に影響を与えるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_SEND_NO_RICH_INFO 
  
> 受信者は、書式設定されたメッセージコンテンツを処理できません。 MAPI_SEND_NO_RICH_INFO が設定されている場合、MAPI は受信者の**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) プロパティを FALSE に設定します。 MAPI_SEND_NO_RICH_INFO が設定されていない場合、MAPI は、 _lpszaddress_が指す受信者のメッセージアドレスがインターネットアドレスであると解釈されない限り、このプロパティを TRUE に設定します。 この場合、MAPI は**PR_SEND_RICH_INFO**を FALSE に設定します。 
    
MAPI_UNICODE 
  
> 表示名、アドレスの種類、アドレスは、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、これらの文字列は ANSI 形式になります。
    
 _lpcbEntryID_
  
> 読み上げ_lppentryid_パラメーターによって示されるエントリ識別子のバイト数へのポインター。 
    
 _lppentryid_
  
> 読み上げ1回限りの受信者のエントリ識別子へのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 1回限りのエントリ識別子が正常に作成されました。
    
## <a name="remarks"></a>注釈

**imapisupport:: createoneoff**メソッドは、すべてのサービスプロバイダーサポートオブジェクトに実装されています。 サービスプロバイダーは、 **createoneoff**を呼び出して、1回限りの受信者 (現在読み込まれているアドレス帳プロバイダーのいずれかのコンテナーに属さない受信者) のエントリ識別子を作成します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**createoneoff**で返されるエントリ識別子の使用が終了したら、 [MAPIFreeBuffer](mapifreebuffer.md)関数を使用して、エントリ識別子に割り当てられているメモリを解放します。 
  
## <a name="notes-to-transport-providers"></a>トランスポートプロバイダーへのメモ

トランスポートニュートラルカプセル化形式 (TNEF) をサポートし、 **PR_SEND_RICH_INFO**プロパティの値を使用して、メッセージを転送するときに TNEF を使用するかどうかを決定します。 TNEF をサポートしていない場合、または要求されたときにこの形式でメッセージを送信しない場合は、フォームベースのクライアントまたはカスタム MAPI プロパティを必要とするクライアントで問題になる可能性があります。 これは、通常、カスタムメッセージクラスのカスタムプロパティを送信するために TNEF が使用されるためです。 
  
## <a name="see-also"></a>関連項目



[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagDisplayName 標準プロパティ](pidtagdisplayname-canonical-property.md)
  
[PidTagSendRichInfo 標準プロパティ](pidtagsendrichinfo-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

