---
title: アドレス帳エントリを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f18ba37549f0ea6ee1a4dfa4028fb71289bae274
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600730"
---
# <a name="opening-address-book-entries"></a>アドレス帳エントリを開く

**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントまたはプロバイダーがオブジェクトの 1 つを開くことを要求した場合、MAPI はプロバイダーの [IABLogon::OpenEntry メソッドを呼び出](iablogon-openentry.md) します。 MAPI は、エントリ識別子の [MAPIUID](mapiuid.md)部分を調べて **、IMAPISupport::SetProviderUID** への呼び出しでプロバイダーが登録した **MAPIUID** に一致することで、ターゲット オブジェクトを表すエントリ識別子がプロバイダーに属すると判断します。 MAPI は **、OpenEntry メソッドを呼び出** します。 プロバイダーは、対応するオブジェクト (コンテナー、配布リスト、またはメッセージング ユーザー) を取得して応答する必要があります。 
  
NULL エントリ識別子は、アドレス帳プロバイダーのルート コンテナーを開く要求を示します。 クライアントはルート コンテナーを開いて、階層テーブルとその受信者にアクセスします。 一時受信者を作成するためのテンプレートのみを提供するアドレス帳プロバイダーは、ルート コンテナーの **OpenEntry** 呼び出しをサポートしていない。 
  
### <a name="to-implement-iablogonopenentry"></a>IABLogon::OpenEntry を実装するには
  
1. エントリ識別子がプロバイダーがサポートする有効な識別子を確認します。 有効なエントリ識別子でない場合は、次の値をMAPI_E_INVALID_ENTRYID。 
    
2. _ulFlags_ パラメーターで渡されるフラグを確認します。 MAPI がアプリケーションで渡MAPI_MODIFYプロバイダーがオブジェクトの変更を許可しない場合は、エラー値をMAPI_E_ACCESS_DENIEDします。 
    
3. _lpInterface_ パラメーターで要求されたインターフェイスが、プロバイダーに開く要求されたオブジェクトの種類に対して有効か確認します。 無効なパラメーターが渡された場合は、エラー値をMAPI_E_INTERFACE_NOT_SUPPORTEDします。 
    
4. _cbEntryID_ パラメーターが 0 の場合、これはプロバイダーのルート コンテナーを開く要求です。 ルート コンテナーを作成し **、IABContainer インターフェイス実装へのポインターを** 返します。 
    
5. プロバイダーが複数のログオン オブジェクトを実装している場合は、それぞれが独自に登録済みの **MAPIUID** を持ち、エントリ識別子に含まれる **MAPIUID** を適切なログオン オブジェクトにマップします。 
    
6. _lpulObjectType_ パラメーターに適切な値を設定できるよう、プロバイダーに属するメッセージング ユーザー、配布リスト、またはコンテナー、または一時メッセージング ユーザーまたは配布リストなど、エントリ識別子が表すオブジェクトの種類を決定します。 
    
7. 適切な種類のオブジェクトを作成し、次の基本プロパティを設定します。
    
    - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    - **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
8. エントリ **PR_EMAIL_ADDRESS** 情報から、PR_EMAIL_ADDRESS **(** [PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) と PR_DISPLAY_NAME ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) を計算します。
    
9. オブジェクトのインターフェイス実装へのポインターを返します。 
    

