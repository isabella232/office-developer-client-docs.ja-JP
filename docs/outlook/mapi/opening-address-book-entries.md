---
title: アドレス帳のエントリを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cd86b9cc86f30aac75b732b97208933de4d336e9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566433"
---
# <a name="opening-address-book-entries"></a>アドレス帳のエントリを開く

**適用されます**: Outlook 2013 |Outlook 2016 
  
クライアントまたはプロバイダーが要求されると、オブジェクトの 1 つを開くことを MAPI は、プロバイダーの[IABLogon::OpenEntry](iablogon-openentry.md)メソッドを呼び出します。 MAPI では、ターゲット オブジェクトを表すエントリの識別子が、 [MAPIUID](mapiuid.md)の部分のエントリ id を調べ、**への呼び出しでは、プロバイダーが登録されている**MAPIUID**に一致することによって、プロバイダーに属することを決定します。IMAPISupport::SetProviderUID**。 MAPI は、 **OpenEntry**メソッドを呼び出します。 プロバイダーが対応するオブジェクトを取得することで応答する必要があります: コンテナー、配布リスト、またはメッセージングのユーザーです。 
  
NULL エントリの識別子では、アドレス帳プロバイダーのルート コンテナーを開く要求を示します。 クライアントは、その階層のテーブルとその受信者にアクセスするルート コンテナーを開きます。 のみ 1 回限りの受信者を作成するためのテンプレートを提供するアドレス帳プロバイダーは、ルート コンテナーの**OpenEntry**呼び出しをサポートしていません。 
  
### <a name="to-implement-iablogonopenentry"></a>IABLogon::OpenEntry を実装するには
  
1. エントリの識別子が、プロバイダーがサポートする有効な識別子であることを確認します。 エントリの有効な識別子でない場合は、MAPI_E_INVALID_ENTRYID を返します。 
    
2. _UlFlags_パラメーターに渡されるフラグを確認します。 MAPI_MODIFY MAPI が渡された場合は、プロバイダーでは、そのオブジェクトを変更することはできません、失敗し、MAPI_E_ACCESS_DENIED のエラー値を返します。 
    
3. _LpInterface_パラメーターで要求されたインターフェイスは、プロバイダーは、開くを要求されているオブジェクトの種類に対して有効なことを確認してください。 無効なパラメーターが渡された場合は失敗し、MAPI_E_INTERFACE_NOT_SUPPORTED のエラー値を返します。 
    
4. _CbEntryID_パラメーターが 0 の場合は、これは、プロバイダーのルート コンテナーを開くことを要求します。 ルート コンテナーを作成し、**これにより**インターフェイスの実装へのポインターを返します。 
    
5. プロバイダーは、いくつかのログオン オブジェクトを実装する場合は、それぞれ独自に**MAPIUID**、 **MAPIUID**は、適切なログオン オブジェクトのエントリ id に含まれているマップが登録されています。 
    
6. エントリの識別子を表すオブジェクトの種類を決定する: メッセージ ユーザー、配布リスト、または_lpulObjectType_の適切な値を設定することができるように、プロバイダー、または 1 回限りのメッセージングのユーザーまたは配布リストに属するコンテナーパラメーターです。 
    
7. 適切な型のオブジェクトを作成し、次の基本的なプロパティを設定します。
    
    - **PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    - **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))
    - **PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    - **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
8. エントリ id の情報から、 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) と**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) を計算します。
    
9. オブジェクトのインターフェイスの実装へのポインターを返します。 
    

