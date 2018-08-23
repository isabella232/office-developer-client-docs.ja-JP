---
title: IAddrBookCreateOneOff
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
ms.openlocfilehash: ddb87af4b14be6d728bcceddb4d958ba49229ad4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579040"
---
# <a name="iaddrbookcreateoneoff"></a>IAddrBook::CreateOneOff

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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
  
> [in]受信者の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティの値へのポインター。 _LpszName_パラメーターは、NULL にすることができます。 
    
 _lpszAdrType_
  
> [in]FAX または SMTP など、受信者のアドレスの種類へのポインター。 _LpszAdrType_パラメーターは、NULL にすることはできません。 
    
 _lpszAddress_
  
> [in]受信者のアドレスへのポインター。 _LpszAddress_パラメーターは、NULL にすることはできません。 
    
 _ulFlags_
  
> [in]1 回限りの受信者に影響を与えるフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_SEND_NO_RICH_INFO 
  
> 受信者には、コンテンツの書式設定されたメッセージを処理できません。 MAPI_SEND_NO_RICH_INFO を設定すると、MAPI では受信者の**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) のプロパティを FALSE に設定します。 MAPI_SEND_NO_RICH_INFO が設定されていない場合は、MAPI は_lpszAddress_で指定された受信者のメッセージのアドレスがインターネット アドレスを解釈しない限り、TRUE にこのプロパティを設定します。 この例では、MAPI は、 **PR_SEND_RICH_INFO**を FALSE に設定します。 
    
MAPI_UNICODE 
  
> 表示名、アドレスの種類、およびアドレスは、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式でこれらの文字列です。
    
 _lpcbEntryID_
  
> [out]_LppEntryID_パラメーターで指定されたエントリの識別子のバイト数へのポインター。 
    
 _lppEntryID_
  
> [out]1 回限りの受信者のエントリの識別子へのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 一時エントリ id が正常に作成されました。
    
## <a name="remarks"></a>注釈

クライアントが 1 回限りの受信者のエントリ id を作成する**CreateOneOff**メソッドを呼び出して、現在読み込まれているアドレス帳プロバイダーのいずれかから任意のコンテナーに属していない受信者です。 一時受信者は、セッションのすべての種類のアクティブなアドレス帳のプロバイダーの 1 つによってサポートされているアドレスを持つことができます。 
  
一時受信者は通常、特定のアドレスの種類のテンプレートを使用して作成されます。 アドレスの種類をサポートしているアドレス帳プロバイダーには、テンプレートが用意されています。 クライアント アプリケーションのユーザーは、テンプレートに関連する情報を入力します。
  
MAPI では、表示名、アドレスの種類、および**CreateOneOff**のアドレス パラメーターの文字の Unicode 文字列をサポートしています。
  
MAPI_SEND_NO_RICH_INFO フラグは、書式付きのテキストをリッチ テキスト形式 (RTF) では各メッセージと送信かどうかを制御します。 トランスポート ニュートラル カプセル化形式 (TNEF): 書式設定されたテキスト形式の送信に使用される-は、受信者が、 **PR_SEND_RICH_INFO**プロパティを設定する方法に関係なく、ほとんどのトランスポート プロバイダーによって送信されます。 個人間のメッセージを処理するクライアントのメッセージングの問題ではありません。 ただし、通常は TNEF を送信するカスタム メッセージ クラス用のカスタム プロパティを使用、それをサポートしていないことがありますフォーム ベースのクライアントまたはユーザー設定の MAPI プロパティを必要とするクライアントの問題。 詳細については、 [TNEF をメッセージの送信](sending-messages-with-tnef.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|Mapiabfunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI では、 **CreateOneOff**メソッドを使用して、任意のアドレス帳に含まれていないアドレスのエントリ ID を作成します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

