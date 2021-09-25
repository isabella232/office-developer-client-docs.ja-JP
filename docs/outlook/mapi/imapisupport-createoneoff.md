---
title: IMAPISupportCreateOneOff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.CreateOneOff
api_type:
- COM
ms.assetid: ee57d6e0-9de0-4427-97ce-371c1c01f3de
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6d65a0103e86b89aa051c41a1597d0b2208aa33e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596142"
---
# <a name="imapisupportcreateoneoff"></a>IMAPISupport::CreateOneOff

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1 回のアドレスのエントリ識別子を作成します。
  
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
  
> [in]受信者 [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)**プロパティPR_DISPLAY_NAME表示** 名へのポインター。 _lpszName パラメーター_ には NULL を指定できます。 
    
 _lpszAdrType_
  
> [in]受信者のアドレスの種類 (FAX、SMTP、X500 など) へのポインター。 _lpszAdrType パラメーター_ を NULL にすることはできません。 
    
 _lpszAddress_
  
> [in]受信者のメッセージング アドレスへのポインター。 _lpszAddress パラメーター_ は NULL にすることはできません。 
    
 _ulFlags_
  
> [in]1 回の受信者に影響を与えるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_SEND_NO_RICH_INFO 
  
> 受信者は、書式設定されたメッセージ コンテンツを処理できません。 このMAPI_SEND_NO_RICH_INFO設定されている場合、MAPI は受信者のPR_SEND_RICH_INFO **(** [PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) プロパティを FALSE に設定します。 このMAPI_SEND_NO_RICH_INFO設定されていない場合  _、LPszAddress_ が指す受信者のメッセージング アドレスがインターネット アドレスと解釈されない限り、MAPI はこのプロパティを TRUE に設定します。 この場合、MAPI は、この値 **PR_SEND_RICH_INFO** FALSE に設定します。 
    
MAPI_UNICODE 
  
> 表示名、アドレスの種類、およびアドレスは Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、これらの文字列は ANSI 形式です。
    
 _lpcbEntryID_
  
> [out]  _lppEntryID_ パラメーターが指すエントリ識別子内のバイト数へのポインター。 
    
 _lppEntryID_
  
> [out]1 回の受信者のエントリ識別子へのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 1 回のエントリ識別子が正常に作成されました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::CreateOneOff** メソッドは、すべてのサービス プロバイダー サポート オブジェクトに実装されます。 サービス プロバイダーは **CreateOneOff** を呼び出して、1 回の受信者 (現在読み込まれているアドレス帳プロバイダーのコンテナーに属していない受信者) のエントリ識別子を作成します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**CreateOneOff** によって返されるエントリ識別子の使用が完了したら [、MAPIFreeBuffer](mapifreebuffer.md)関数を使用してエントリ識別子に割り当てられたメモリを解放します。 
  
## <a name="notes-to-transport-providers"></a>トランスポート プロバイダーへのメモ

トランスポート ニュートラル カプセル化形式 (TNEF) をサポートし **、PR_SEND_RICH_INFO** プロパティの値を使用して、メッセージを転送するときに TNEF を使用するかどうかを決定します。 TNEF をサポートしていない、または要求された場合にこの形式でメッセージを送信しない場合は、カスタム MAPI プロパティを必要とするフォーム ベースのクライアントまたはクライアントに問題が発生する可能性があります。 これは、TNEF は通常、カスタム メッセージ クラスのカスタム プロパティを送信するために使用されるためです。 
  
## <a name="see-also"></a>関連項目



[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagDisplayName 標準プロパティ](pidtagdisplayname-canonical-property.md)
  
[PidTagSendRichInfo 標準プロパティ](pidtagsendrichinfo-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

