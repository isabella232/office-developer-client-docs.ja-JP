---
title: セッションを使用したオブジェクトへのアクセス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ecada707-2960-41ec-be7e-619cad257c57
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: da0ee486979d02f70f24fed2e6e63a5ce5277564
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556981"
---
# <a name="accessing-objects-by-using-the-session"></a>セッションを使用したオブジェクトへのアクセス

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[MAPILogonEx](mapilogonex.md)への呼び出しから受け取るセッション ポインターを使用すると、さまざまなオブジェクトにアクセスできます。 次の表に、さまざまなオブジェクトにアクセスするために使用されるメソッドを示します。 
  
|**Object**|**Session メソッド**|
|:-----|:-----|
|[プロファイル] セクション  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|メッセージ ストア  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|アドレス帳  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|メッセージ サービス管理オブジェクト  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|フォルダー、メッセージ、アドレス帳コンテナー、配布リスト、またはメッセージング ユーザー  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
**OpenEntry メソッドと有効** なエントリ識別子を使用すると、任意のアドレス帳またはメッセージ ストア プロバイダー オブジェクトを開きます。 **IMAPISession** メソッドに加えて、MAPI には **他にも OpenEntry メソッド** があります。 **OpenEntry は** 、次のオブジェクトに実装されます。 
  
|**Object**|**メソッド**|
|:-----|:-----|
|アドレス帳プロバイダーのログオン オブジェクト  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md) <br/> |
|アドレス帳  <br/> |[IAddrBook::OpenEntry](iaddrbook-openentry.md) <br/> |
|アドレス帳コンテナー  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Session  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
|メッセージ ストア  <br/> |[IMsgStore::OpenEntry](imsgstore-openentry.md) <br/> |
|メッセージ ストア プロバイダーのログオン オブジェクト  <br/> |[IMSLogon::OpenEntry](imslogon-openentry.md) <br/> |
|フォルダー  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|サポート オブジェクト  <br/> |[IMAPISupport::OpenEntry](imapisupport-openentry.md) <br/> |
   
**一部の OpenEntry** メソッドでは **、IMAPISession::OpenEntry** と同様に、オブジェクトのエントリ識別子を開く必要があります。その他のメソッドでは、NULL を指定できます。 NULL エントリ識別子は、オブジェクトによって異なる方法で解釈されます。 たとえば、NULL エントリ識別子を使用して **IAddrBook::OpenEntry** を呼び出す場合、MAPI はアドレス帳のルート コンテナーを開きます。 メッセージ ストアの **OpenEntry メソッドも** 同様に動作します。メッセージ ストアのルート フォルダーが開きます。 **IMAPIContainer::OpenEntry** は、フォルダーコンテナーとアドレス帳コンテナーの両方によって実装され、実装者によっては MAPI_E_INVALID_PARAMETER またはルート コンテナーを返す場合があります。 
  
エントリ識別子の NULL 値を許可しないだけでなく、セッションの **OpenEntry** メソッドは、そのジョブがオブジェクトを開かないので、他の **OpenEntry** メソッドとは異なります。 代わりに、エントリ識別子を調べて、適切なサービス プロバイダーによって実装された別の **OpenEntry** メソッドに呼び出しを転送します。 たとえば、メッセージのエントリ識別子を使用して **IMAPISession::OpenEntry** を呼び出す場合、MAPI はメッセージを担当するメッセージ ストアの **IMSLogon::OpenEntry** メソッドを呼び出します。 
  
セッションを使用してオブジェクトを開くだけでなく、クライアントはセッションを使用してオブジェクトを比較します。 [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md)メソッドは、エントリ識別子を比較してオブジェクトを比較します。 エントリ識別子 [に含まれる MAPIUID](mapiuid.md) 構造体が同じサービス プロバイダーに属している場合、MAPI は呼び出しをそのプロバイダーに転送します。 **CompareEntryIDs は** 、2 つのエントリ識別子が一致しない場合にエラー値を返します。 このメソッドは、任意の種類のオブジェクトに属するエントリ識別子を比較することができますが **、CompareEntryIDs** は、メッセージ ストアやアドレス帳コンテナーなどの上位レベルのオブジェクトに最適です。 下位レベルのオブジェクトを比較するには、オブジェクトの検索キー **(PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))) またはレコード キー (**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))) を直接比較します。 
  
**OpenEntry と同様** に **、CompareEntryIDs は複数** のオブジェクトによって実装されます。 開くオブジェクトまたは比較するオブジェクトに関する情報の量に応じて、使用する **OpenEntry** メソッドと **CompareEntryID** メソッドを選択します。 呼び出すインターフェイス メソッドを決定する場合は、次のガイドラインを使用します。 
  
- ターゲット オブジェクトに関する情報がない場合は [、IMAPISession::OpenEntry](imapisession-openentry.md) または [IMAPISession::CompareEntryIDs を呼び出します](imapisession-compareentryids.md)。 この方法では、任意のオブジェクトにアクセスできますが、3 つのオブジェクトの中で最も低速です。
    
- ターゲット オブジェクトがフォルダーではなくアドレス帳エントリである場合は [、IAddrBook::OpenEntry](iaddrbook-openentry.md) メソッドまたは [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) メソッドを呼び出します。 **IAddrBook::OpenEntry は** 、ターゲット オブジェクトとして NULL を指定すると、アドレス帳のルート コンテナーを開きます。 この方法では、任意のアドレス帳オブジェクトへのアクセスが可能で **、IMAPISession** を使用するよりも高速ですが **、IMAPIContainer** を使用するよりも遅くなります。
    
- 使用するエントリ識別子が短期的なエントリ識別子である場合、またはターゲット オブジェクトが特定のアドレス帳コンテナーまたはフォルダーに属している場合は [、IMAPIContainer::OpenEntry](imapicontainer-openentry.md) メソッドを呼び出します。 この方法では、パフォーマンスは最も高速になりますが、特定のコンテナーまたはフォルダー内のオブジェクトにのみアクセスできます。 
    

