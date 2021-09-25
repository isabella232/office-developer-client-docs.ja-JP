---
title: IAddrBookCreateOneOff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.CreateOneOff
api_type:
- COM
ms.assetid: bcacfbdf-edff-4810-a985-e6d2c9271901
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e5eec965f4a70a5fdec1e9e97cfadc7d26294b78
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596443"
---
# <a name="iaddrbookcreateoneoff"></a>IAddrBook::CreateOneOff

  
  
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
  
> [in]受信者のプロパティ[(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)プロパティPR_DISPLAY_NAMEへのポインター。  _lpszName パラメーター_ には NULL を指定できます。 
    
 _lpszAdrType_
  
> [in]FAX や SMTP などの受信者のアドレスの種類へのポインター。 _lpszAdrType パラメーター_ を NULL にすることはできません。 
    
 _lpszAddress_
  
> [in]受信者のアドレスへのポインター。 _lpszAddress パラメーター_ は NULL にすることはできません。 
    
 _ulFlags_
  
> [in]1 回の受信者に影響を与えるフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_SEND_NO_RICH_INFO 
  
> 受信者は、書式設定されたメッセージ コンテンツを処理できません。 このMAPI_SEND_NO_RICH_INFO設定されている場合、MAPI は受信者のPR_SEND_RICH_INFO **(** [PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) プロパティを FALSE に設定します。 このMAPI_SEND_NO_RICH_INFO設定されていない場合  _、LPszAddress_ が指す受信者のメッセージング アドレスがインターネット アドレスと解釈されない限り、MAPI はこのプロパティを TRUE に設定します。 この場合、MAPI は、この値 **PR_SEND_RICH_INFO** FALSE に設定します。 
    
MAPI_UNICODE 
  
> 表示名、アドレスの種類、およびアドレスは Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、これらの文字列は ANSI 形式です。
    
 _lpcbEntryID_
  
> [out]  _lppEntryID_ パラメーターが指すエントリ識別子内のバイト 数へのポインター。 
    
 _lppEntryID_
  
> [out]1 回の受信者のエントリ識別子へのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 1 回のエントリ識別子が正常に作成されました。
    
## <a name="remarks"></a>注釈

クライアントは **CreateOneOff** メソッドを呼び出して、現在読み込まれているアドレス帳プロバイダーのコンテナーに属していない受信者である 1 回の受信者のエントリ識別子を作成します。 1 回の受信者は、セッションのアクティブなアドレス帳プロバイダーの 1 つでサポートされる任意の種類のアドレスを持つ可能性があります。 
  
一時受信者は、通常、特定のアドレスの種類のテンプレートを使用して作成されます。 アドレスの種類をサポートするアドレス帳プロバイダーは、テンプレートを提供します。 クライアント アプリケーションのユーザーは、関連する情報をテンプレートに入力します。
  
MAPI では、CreateOneOff の表示名、アドレスの種類、およびアドレス パラメーターの Unicode 文字 **文字列がサポートされています**。
  
[MAPI_SEND_NO_RICH_INFO] フラグは、リッチ テキスト形式 (RTF) の書式設定されたテキストを各メッセージと共に送信するかどうかを制御します。 トランスポート ニュートラル カプセル化形式 (TNEF) (書式設定されたテキストの送信に使用される形式) は、受信者が PR_SEND_RICH_INFO プロパティを設定する方法に関係なく、ほとんどのトランスポート **プロバイダーによって送信** されます。 これは、対人メッセージを処理するメッセージング クライアントの問題ではありません。 ただし、TNEF は通常、カスタム メッセージ クラスのカスタム プロパティを送信するために使用するため、サポートしない場合は、カスタム MAPI プロパティを必要とするフォーム ベースのクライアントまたはクライアントに問題が発生する可能性があります。 詳細については [、「TNEF を使用したメッセージの送信」を参照してください](sending-messages-with-tnef.md)。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|Mapiabfunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI は **CreateOneOff** メソッドを使用して、アドレス帳に含めされていないアドレスのエントリ ID を作成します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

