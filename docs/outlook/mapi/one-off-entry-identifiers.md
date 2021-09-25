---
title: 一時エントリ識別子
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 741d21ae-f14a-4b7f-80aa-91d0f0ff3f34
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: befb72506ee8b31628b10567996a92db6de3f89b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584012"
---
# <a name="one-off-entry-identifiers"></a>一時エントリ識別子
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1 回限りエントリ識別子は **、IAddrBook::CreateOneOff** メソッドで MAPI によって作成され、ゲートウェイ コンポーネントなどの MAPI サブシステムにアクセスできないコンポーネントによって作成されます。 �ڍׂɂ��ẮA [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)��Q�Ƃ��Ă��������B 次の図は、一時エントリ識別子の形式を示しています。
  
**一時エントリ識別子の形式**
  
![一時エントリ識別子の形式](media/amapi_69.gif "一時エントリ識別子の形式")
  
最初のフィールドは、カスタム受信者を表すエントリ識別子を識別する特別な [MAPIUID](mapiuid.md) 構造です。 この **MAPIUID** 構造体は、定数に設定する必要MAPI_ONE_OFF_UID。 MAPI_ONE_OFF_UIDは、ヘッダー ファイル MAPIDEFS.H で定義されます。 
  
バージョンとフラグのフィールドは、Intel のバイト順で 16 ビットの単語です。 バージョン フィールドは 0 に設定する必要があります。 flags フィールドは、次の値に設定できます。
  
MAPI_ONE_OFF_NO_RICH_INFO
  
MAPI_ONE_OFF_UNICODE
  
受信者MAPI_ONE_OFF_NO_RICH_INFOトランスポート ニュートラル カプセル化形式 (TNEF) でメッセージ コンテンツを受信しない場合は、このフラグが設定されます。 このフラグは [、IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) MAPI_SEND_NO_RICH_INFOに渡される場合に設定されます。 
  
表示MAPI_ONE_OFF_UNICODE、電子メール アドレスが Unicode 文字列の場合は、このフラグが設定されます。 このフラグは **、IAddrBook::CreateOneOff にMAPI_UNICODEが渡される場合に設定されます**。 **CreateOneOff** に MAPI_UNICODEフラグが渡されない場合、MAPI は表示名と電子メール アドレス文字列がワークステーションの現在の ANSI 文字セットにあると見なします。 ANSI 文字列は、通常、コード ページがエントリ識別子にエンコードされないので、異なる文字セットを使用してプラットフォーム間で送信されるメッセージではうまく動作しません。 この潜在的な非互換性から保護するために、多くのアドレスの種類は、複数の文字セットで一般的な文字にのみ制限されます。 ただし、文字セットとプラットフォームの互換性を確保するために、クライアントはメッセージ内の文字列に Unicode を使用する必要があります。
  
表示名は、受信者の **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティおよび **IAddrBook::CreateOneOff** に渡される _lpszName_ パラメーターに対応する null で終わる文字列です。 文字セットが Unicode の場合MAPI_ONE_OFF_UNICODEフラグが設定されている場合、ANSI はクリアです。 
  
アドレスの種類は、受信者の **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) プロパティおよび **IAddrBook::CreateOneOff** に渡される _lpszAdrType_ パラメーターに対応する null 終端文字列です。 
  
電子メール アドレスは、受信者の PR_EMAIL_ADDRESS ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) プロパティおよび **IAddrBook::CreateOneOff** に渡される _lpszAddress_ パラメーターに対応する null で終わる文字列です。  
  
> [!NOTE]
> 1 回のエントリ識別子構造にパディングはありません。バイトは上で示したとおりにパックされ、エントリ識別子の長さは、電子メール アドレスの終端の null 文字を超えるバイトを含めることはできません。 
  
一時エントリ識別子を手動で作成するクライアントおよびアドレス帳プロバイダーは **、PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) プロパティと PR_SEARCH_KEY ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティの値を生成する必要があります。  レコード キーはエントリ識別子と同じです。 検索キーは、次のフィールドを次の順序で連結して形成する必要があります。
  
1. 大文字に変換されたアドレスの種類。
    
2. コロン (:)。
    
3. 大文字に変換された電子メール アドレス。
    
4. 終端の null 文字。
    
検索キーを生成するときに、文字セット変換を実行する必要はありません。
  

