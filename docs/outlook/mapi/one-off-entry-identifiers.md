---
title: 一時エントリ識別子
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 741d21ae-f14a-4b7f-80aa-91d0f0ff3f34
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: abe52cb45e13e6713d28fffe379e245e2483bffa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279694"
---
# <a name="one-off-entry-identifiers"></a>一時エントリ識別子
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**IAddrBook:: createoneoff**メソッドと、ゲートウェイコンポーネントなどの mapi サブシステムにアクセスできないコンポーネントによって、1回限りのエントリ識別子が mapi によって作成されます。 �ڍׂɂ��ẮA [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)��Q�Ƃ��Ă��������B 次の図は、1回限りのエントリ識別子の形式を示しています。
  
**一時エントリ識別子の形式**
  
![1 回限りのエントリ識別子形式](media/amapi_69.gif "1 回限りのエントリ識別子形式")
  
最初のフィールドは、カスタム受信者を表すエントリ id を識別する特別な[MAPIUID](mapiuid.md)構造です。 この**MAPIUID**構造は、定数 MAPI_ONE_OFF_UID に設定する必要があります。 MAPI_ONE_OFF_UID は、ヘッダーファイル mapidefs.h で定義されています。H. 
  
version および flags フィールドは、Intel バイトオーダーでの16ビットの単語です。 バージョンフィールドは0に設定する必要があります。 flags フィールドには、次の値を設定できます。
  
MAPI_ONE_OFF_NO_RICH_INFO
  
MAPI_ONE_OFF_UNICODE
  
MAPI_ONE_OFF_NO_RICH_INFO フラグは、受信者がトランスポートニュートラルカプセル化形式 (TNEF) でメッセージコンテンツを受信できないように設定されています。 このフラグは、MAPI_SEND_NO_RICH_INFO が[IAddrBook:: createoneoff](iaddrbook-createoneoff.md)メソッドに渡されたときに設定されます。 
  
表示名と電子メールアドレスが UNICODE 文字列の場合は、MAPI_ONE_OFF_UNICODE フラグが設定されます。 このフラグは、MAPI_UNICODE が**IAddrBook:: createoneoff**に渡されたときに設定されます。 MAPI_UNICODE フラグが**createoneoff**に渡されていない場合、MAPI では、表示名と電子メールアドレスの文字列がワークステーションの現在の ANSI 文字セットに含まれていると見なされます。 ANSI 文字列は、コードページがエントリ識別子でエンコードされていないために、異なる文字セットを使用してプラットフォーム間で送信されるメッセージでは、通常は適切に機能しません。 このような非互換性の問題から保護するために、多くのアドレスの種類は、複数の文字セットで共通の文字に制限されています。 ただし、文字セットとプラットフォームの互換性を確保するために、クライアントはメッセージ内の文字列に Unicode を使用する必要があります。
  
表示名は、受信者の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティ、および**IAddrBook:: createoneoff**に渡された_lpszname_パラメーターに対応する、null で終わる文字列です。 MAPI_ONE_OFF_UNICODE フラグが設定されている場合、文字セットが Unicode で、クリアされている場合は ANSI になります。 
  
アドレスの種類は、受信者の**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) プロパティ、および**IAddrBook:: createoneoff**に渡された_lpszadrtype_パラメーターに対応する、null で終わる文字列です。 
  
電子メールアドレスは、受信者の**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) プロパティ、および**IAddrBook:: createoneoff**に渡された_lpszaddress_パラメーターに対応する、null で終了する文字列です。 
  
> [!NOTE]
> 1回限りのエントリ識別子の構造には、パディングはありません。バイトは上記で示したとおりにパックされ、エントリ識別子の長さには、電子メールアドレスの終端の null 文字を超えるバイトを含めることはできません。 
  
**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) および**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティの値を生成する必要があるのは、1回限りのエントリ識別子を手動で作成するクライアントとアドレス帳プロバイダーです。 record キーは、エントリ識別子と同じです。 検索キーは、次の順序で各フィールドを連結することによって形成する必要があります。
  
1. 住所の種類を大文字に変換します。
    
2. コロン (:)
    
3. 電子メールアドレス。大文字に変換されます。
    
4. 終端の null 文字。
    
検索キーを生成するときに、文字セット変換を行わないでください。
  

