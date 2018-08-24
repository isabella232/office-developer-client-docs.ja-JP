---
title: IMAPISupportCreateOneOff
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1526ed54fd3773856b009c7c3570064f5a66df28
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594944"
---
# <a name="imapisupportcreateoneoff"></a>IMAPISupport::CreateOneOff

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
一時アドレスのエントリ id を作成します。
  
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

 _lpszName_
  
> [in]**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) は、受信者の表示名へのポインター。 _LpszName_パラメーターは、NULL にすることができます。 
    
 _lpszAdrType_
  
> [in]受信者のアドレスの種類 (FAX、SMTP、X500 など) へのポインター。 _LpszAdrType_パラメーターは、NULL にすることはできません。 
    
 _lpszAddress_
  
> [in]受信者のメッセージのアドレスへのポインター。 _LpszAddress_パラメーターは、NULL にすることはできません。 
    
 _ulFlags_
  
> [in]1 回限りの受信者に影響を与えるフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_SEND_NO_RICH_INFO 
  
> 受信者には、コンテンツの書式設定されたメッセージを処理できません。 MAPI_SEND_NO_RICH_INFO を設定すると、MAPI では受信者の**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) のプロパティを FALSE に設定します。 MAPI_SEND_NO_RICH_INFO が設定されていない場合は、MAPI は_lpszAddress_で指定された受信者のメッセージのアドレスがインターネット アドレスを解釈しない限り、TRUE にこのプロパティを設定します。 この例では、MAPI は、 **PR_SEND_RICH_INFO**を FALSE に設定します。 
    
MAPI_UNICODE 
  
> 表示名、アドレスの種類、およびアドレスは、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式でこれらの文字列です。
    
 _lpcbEntryID_
  
> [out]_LppEntryID_パラメーターで指定されたエントリの識別子のバイト数のカウントへのポインター。 
    
 _lppEntryID_
  
> [out]1 回限りの受信者のエントリの識別子へのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 一時エントリ id が正常に作成されました。
    
## <a name="remarks"></a>注釈

サービス プロバイダーのサポートのすべてのオブジェクトの**IMAPISupport::CreateOneOff**メソッドを実装します。 サービス プロバイダーでは、一時受信者 (現在ロードされているアドレス帳プロバイダーのいずれかから任意のコンテナーに属していない受信者) のエントリ id を作成するのには**CreateOneOff**を呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**CreateOneOff**によって返されるエントリの識別子を使用してが完了したら、 [MAPIFreeBuffer](mapifreebuffer.md)関数を使用してエントリの識別子の割り当てられたメモリを解放します。 
  
## <a name="notes-to-transport-providers"></a>トランスポート プロバイダーへのメモ

トランスポート ニュートラル カプセル化形式 (TNEF) をサポートし、 **PR_SEND_RICH_INFO**プロパティの値を使用して、メッセージを転送する場合は、TNEF を使用するかどうかを決定します。 TNEF をサポートしていないまたはしないメッセージを送信する次の形式で要求されたときに、フォーム ベースのクライアントまたはユーザー設定の MAPI プロパティを必要とするクライアントの問題がある場合ができます。 TNEF は、通常、送信するカスタム メッセージ クラス用のカスタム プロパティに使用するためです。 
  
## <a name="see-also"></a>関連項目



[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagDisplayName 標準プロパティ](pidtagdisplayname-canonical-property.md)
  
[PidTagSendRichInfo 標準プロパティ](pidtagsendrichinfo-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

