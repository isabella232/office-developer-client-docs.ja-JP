---
title: 一時エントリ id
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 741d21ae-f14a-4b7f-80aa-91d0f0ff3f34
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1335de3c1decf6c594f0148fbbf055061d7ce7e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801670"
---
# <a name="one-off-entry-identifiers"></a>一時エントリ id
  
**適用対象**: Outlook 
  
一時エントリ id は、 **IAddrBook::CreateOneOff**メソッドでは、MAPI とゲートウェイ ・ コンポーネントなど、MAPI サブシステムへのアクセス権を持たないコンポーネントによって作成されます。 �ڍׂɂ��ẮA [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)��Q�Ƃ��Ă��������B 一時エントリ id の形式を次の図に示します。
  
**一時エントリ識別子の形式**
  
![一時エントリの識別子の形式](media/amapi_69.gif "一時エントリの識別子の形式")
  
最初のフィールドは、カスタム受信者を表すものとしてのエントリ id を識別する特殊な[MAPIUID](mapiuid.md)構造です。 この**MAPIUID**の構造体は、定数 MAPI_ONE_OFF_UID を設定しなければなりません。 MAPI_ONE_OFF_UID は、MAPIDEFS ヘッダー ファイルで定義されます。H. 
  
バージョンとフラグ フィールドには、Intel のバイト順の 16 ビット ワードです。 バージョン フィールドはゼロに設定する必要があります。 フラグ フィールドは、次の値に設定できます。
  
MAPI_ONE_OFF_NO_RICH_INFO
  
MAPI_ONE_OFF_UNICODE
  
受信者が表示されなくなりますメッセージの内容で、トランスポート ニュートラル カプセル化形式 (TNEF) 場合、MAPI_ONE_OFF_NO_RICH_INFO フラグが設定されています。 MAPI_SEND_NO_RICH_INFO は、 [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)メソッドに渡されるとき、このフラグが設定されています。 
  
表示名と電子メール アドレスが Unicode 文字列である場合、MAPI_ONE_OFF_UNICODE フラグが設定されています。 MAPI_UNICODE が**IAddrBook::CreateOneOff**に渡された場合、このフラグが設定されています。 **CreateOneOff**に MAPI_UNICODE フラグが渡されない、MAPI では、ワークステーションの現在の ANSI 文字セットでは、表示名と電子メール アドレスの文字列を想定しています。 ANSI 文字列は、一般にエントリの識別子のコード ページがエンコードされていませんので、別の文字セットを使用してプラットフォーム間で送信されるメッセージでは動作しません。 この潜在的な互換性の問題を防ぐには、多くのアドレスの種類は、複数の文字セットに共通の文字だけに制限されます。 ただし、文字セットとプラットフォームの互換性を確保するのにはクライアントする必要があります Unicode を使用、メッセージ内の文字の文字列です。
  
表示名は、受信者の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティを**IAddrBook::CreateOneOff**に渡される_lpszName_パラメーターに対応する null で終わる文字列です。 明らかな場合、MAPI_ONE_OFF_UNICODE フラグが設定されたと ANSI の場合、文字セット、ユニコードです。 
  
アドレスの種類は、受信者の**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) のプロパティを**IAddrBook::CreateOneOff**に渡される_lpszAdrType_パラメーターに対応する null で終わる文字列です。 
  
電子メール アドレスは、受信者の**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) のプロパティを**IAddrBook::CreateOneOff**に渡される_lpszAddress_パラメーターに対応する null で終わる文字列です。 
  
> [!NOTE]
> 1 回限りのエントリの識別子構造体です。バイトの上に示されるとおりに梱包し、エントリの識別子の長さは、電子メール アドレスの末尾の null 文字を超える任意のバイト数を含めないようにします。 
  
クライアントと一時エントリ id を手動で作成したアドレス帳プロバイダーは、 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) と**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) のプロパティの値を生成する必要もあります。 レコード キーは、エントリの識別子と同じです。 検索キーは、次の順序で次のフィールドを連結することにより形成する必要があります。
  
1. アドレスの種類、文字の大文字に変換します。
    
2. コロン (:)。
    
3. 電子メールのアドレスは、大文字に変換されます。
    
4. 終端の null 文字です。
    
文字セット変換する必要がありますを完了できません、検索キーを生成するとき。
  

