---
title: アドレス帳エントリを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6ebd6009700742e9b1159bc95ff0496c423e512c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326328"
---
# <a name="opening-address-book-entries"></a>アドレス帳エントリを開く

**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントまたはプロバイダーが、いずれかのオブジェクトを開くことを要求した場合、MAPI はプロバイダーの[IABLogon:: openentry](iablogon-openentry.md)メソッドを呼び出します。 MAPI は、エントリ識別子の[MAPIUID](mapiuid.md)部分を調べ、それを呼び出し**** **でプロバイダーが登録した MAPIUID に一致させることによって、ターゲットオブジェクトを表すエントリ識別子がプロバイダーに属していると判断します。imapisupport:: setprovideruid**。 その後、MAPI が**openentry**メソッドを呼び出します。 プロバイダーは、対応するオブジェクト (コンテナー、配布リスト、またはメッセージングユーザー) を取得することによって応答する必要があります。 
  
NULL エントリ識別子は、アドレス帳プロバイダーのルートコンテナーを開く要求を示します。 クライアントは、ルートコンテナーを開いて、階層テーブルとその受信者にアクセスします。 1回限りの受信者を作成するためのテンプレートのみを提供するアドレス帳プロバイダーは、ルートコンテナーの**openentry**呼び出しをサポートしていません。 
  
### <a name="to-implement-iablogonopenentry"></a>IABLogon:: openentry を実装するには
  
1. 入力識別子がプロバイダーがサポートしている有効な識別子であることを確認してください。 有効なエントリ識別子でない場合は、MAPI_E_INVALID_ENTRYID を返します。 
    
2. _ulflags_パラメーターを使用して渡されたフラグを確認します。 MAPI が MAPI_MODIFY で渡され、プロバイダーがそのオブジェクトの変更を許可していない場合は、エラーが発生し、MAPI_E_ACCESS_DENIED エラー値が返されます。 
    
3. _lpinterface_パラメーターで要求されたインターフェイスが、プロバイダーが開くように求められたオブジェクトの種類に対して有効であることを確認します。 無効なパラメーターが渡された場合は、fail を返し、MAPI_E_INTERFACE_NOT_SUPPORTED エラーの値を返します。 
    
4. _cbEntryID_パラメーターが0の場合、これはプロバイダーのルートコンテナーを開くための要求です。 ルートコンテナーを作成し、その**IABContainer**インターフェイス実装へのポインターを返します。 
    
5. プロバイダーが複数のログオンオブジェクトを実装しており、それぞれに**MAPIUID**登録されている場合は、エントリ識別子に含まれる**MAPIUID**と適切なログオンオブジェクトをマップします。 
    
6. エントリ識別子が表すオブジェクトの種類を決定します。これは、プロバイダーに属するメッセージングユーザー、配布リスト、またはコンテナーで、または、 _lpulObjectType_に対して適切な値を設定できるように、1回限りのメッセージングユーザーまたは配布リストに属しています。parameter. 
    
7. 適切な型のオブジェクトを作成し、次の基本的なプロパティを設定します。
    
    - **PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    - **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))
    - **PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    - **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
8. エントリ識別子の情報から**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) と**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) を計算します。
    
9. オブジェクトのインターフェイス実装へのポインターを返します。 
    

