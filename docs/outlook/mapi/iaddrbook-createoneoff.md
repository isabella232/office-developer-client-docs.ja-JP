---
title: iaddrbookcreateoneoff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.CreateOneOff
api_type:
- COM
ms.assetid: bcacfbdf-edff-4810-a985-e6d2c9271901
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 980ac82c6f7fcb5771a6013b3fb033b0bdfd05e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349316"
---
# <a name="iaddrbookcreateoneoff"></a>IAddrBook::CreateOneOff

  
  
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
  
> 順番受信者の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティの値へのポインター。 _lpszname_パラメーターには NULL を指定できます。 
    
 _lpszadrtype_
  
> 順番FAX、SMTP などの受信者のアドレスの種類へのポインター。 _lpszadrtype_パラメーターを NULL にすることはできません。 
    
 _lpszaddress_
  
> 順番受信者のアドレスへのポインター。 _lpszaddress_パラメーターを NULL にすることはできません。 
    
 _ulFlags_
  
> 順番1回限りの受信者に影響を与えるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_SEND_NO_RICH_INFO 
  
> 受信者は、書式設定されたメッセージコンテンツを処理できません。 MAPI_SEND_NO_RICH_INFO が設定されている場合、MAPI は受信者の**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) プロパティを FALSE に設定します。 MAPI_SEND_NO_RICH_INFO が設定されていない場合、MAPI は、 _lpszaddress_が指す受信者のメッセージアドレスがインターネットアドレスであると解釈されない限り、このプロパティを TRUE に設定します。 この場合、MAPI は**PR_SEND_RICH_INFO**を FALSE に設定します。 
    
MAPI_UNICODE 
  
> 表示名、アドレスの種類、アドレスは、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、これらの文字列は ANSI 形式になります。
    
 _lpcbEntryID_
  
> 読み上げ_lppentryid_パラメーターによって指定されたエントリ識別子のバイト数へのポインター。 
    
 _lppentryid_
  
> 読み上げ1回限りの受信者のエントリ識別子へのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 1回限りのエントリ識別子が正常に作成されました。
    
## <a name="remarks"></a>解説

クライアントは**createoneoff**メソッドを呼び出して、1回限りの受信者 (現在読み込まれているアドレス帳プロバイダーのいずれかのコンテナーに属さない受信者) のエントリ id を作成します。 1回限りの受信者は、セッションの active アドレス帳プロバイダーの1つでサポートされている任意の種類のアドレスを持つことができます。 
  
通常、1回限りの受信者は、特定のアドレスの種類に対応したテンプレートを使用して作成されます。 アドレスの種類をサポートするアドレス帳プロバイダーがテンプレートを提供します。 クライアントアプリケーションのユーザーが、テンプレートに関連情報を入力します。
  
MAPI では、表示名、アドレスの種類、および**createoneoff**のアドレスパラメーターに対して Unicode 文字列をサポートしています。
  
MAPI_SEND_NO_RICH_INFO フラグは、リッチテキスト形式 (RTF) の書式付きテキストを各メッセージと共に送信するかどうかを制御します。 トランスポートニュートラルカプセル化形式 (TNEF) (書式付きテキストの送信に使用される形式) は、受信者が**PR_SEND_RICH_INFO**プロパティを設定する方法に関係なく、ほとんどのトランスポートプロバイダーによって送信されます。 これは、個人間メッセージを処理するメッセージングクライアントにとっては問題ではありません。 ただし、TNEF は通常、カスタムメッセージクラスのカスタムプロパティを送信するために使用されるため、サポートしていません。これは、フォームベースのクライアントまたはカスタム MAPI プロパティを必要とするクライアントにとって問題になる可能性があります。 詳細については、「 [TNEF を使用](sending-messages-with-tnef.md)してメッセージを送信する」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|Mapiabfunctions  <br/> |addoneoffaddress  <br/> |mfcmapi は、 **createoneoff**メソッドを使用して、アドレス帳に存在しないアドレスのエントリ ID を作成します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

