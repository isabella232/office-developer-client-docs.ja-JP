---
title: セッションを使用したオブジェクトへのアクセス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ecada707-2960-41ec-be7e-619cad257c57
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: f0696ad4d15274e4af18d2246dd124c1bfee1a2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589407"
---
# <a name="accessing-objects-by-using-the-session"></a>セッションを使用したオブジェクトへのアクセス

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
さまざまなオブジェクトにアクセスするのには、 [MAPILogonEx](mapilogonex.md)呼び出しから受信したセッションのポインターを使用できます。 さまざまなオブジェクトへのアクセスに使用されるメソッドを次の表に一覧します。 
  
|**オブジェクト**|**セッションのメソッド**|
|:-----|:-----|
|プロファイル セクション  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|メッセージ ・ ストア  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|アドレス帳  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|メッセージ サービス管理オブジェクト  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|フォルダー、メッセージ、アドレス帳コンテナー、配布リスト、またはメッセージングのユーザー  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
**OpenEntry**メソッドと有効なエントリの識別子では、アドレス帳またはメッセージ ストア プロバイダー オブジェクトを開くことができます。 他の**OpenEntry**メソッドは MAPI の**IMAPISession**メソッドだけでなくです。 **OpenEntry**は、次のオブジェクトで実装されます。 
  
|**オブジェクト**|**メソッド**|
|:-----|:-----|
|ログオン オブジェクトのアドレス帳プロバイダー  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md) <br/> |
|アドレス帳  <br/> |[IAddrBook::OpenEntry](iaddrbook-openentry.md) <br/> |
|アドレス帳コンテナー  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|セッション  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
|メッセージ ・ ストア  <br/> |[IMsgStore::OpenEntry](imsgstore-openentry.md) <br/> |
|メッセージ ストア プロバイダーのログオン オブジェクト  <br/> |[IMSLogon::OpenEntry](imslogon-openentry.md) <br/> |
|Folder  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|サポート オブジェクト  <br/> |[IMAPISupport::OpenEntry](imapisupport-openentry.md) <br/> |
   
**OpenEntry**メソッドは、 **IMAPISession::OpenEntry**; のように開くには、オブジェクトのエントリ id を必要とします。その他のメソッドを使用すると、NULL を指定できます。 NULL エントリの識別子は、オブジェクトによって異なる方法で解釈されます。 たとえば、NULL のエントリの識別子を使用して**アドレス帳コンテナー**を呼び出すと、MAPI は、アドレス帳のルート コンテナーを開きます。 メッセージ ストアの**OpenEntry**メソッドも同様です。メッセージ ・ ストアのルート フォルダーを開きます。 **IMAPIContainer::OpenEntry**、両方のフォルダーとアドレス帳のコンテナーによって実装されるには、MAPI_E_INVALID_PARAMETER または実装によって、ルート コンテナーを返すことがあります。 
  
他のエントリ id の NULL 値を許可するには、セッションの**OpenEntry**メソッドとは異なります**OpenEntry**メソッドは他のオブジェクトを開くには、そのジョブのためです。 代わりに、エントリ id を検証し、適切なサービス プロバイダーによって実装されている別の**OpenEntry**メソッドの呼び出しを転送します。 などの場合メッセージのエントリ id を持つ**IMAPISession::OpenEntry**を呼び出すと、MAPI **IMSLogon::OpenEntry**メソッド呼び出しメッセージ ストアのメッセージを担当します。 
  
セッションを開くにはオブジェクトを使用する以外クライアントは、それを比較するために使用します。 [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md)メソッドは、それらのエントリの識別子を比較することによってオブジェクトを比較します。 エントリの識別子に含まれる[MAPIUID](mapiuid.md)構造体は、同じサービス プロバイダーに属する、MAPI は、そのプロバイダーへの呼び出しを転送します。 **CompareEntryIDs**は、2 つのエントリの識別子が一致しない場合、エラー値を返します。 このメソッドは、オブジェクトの任意の型に属しているエントリの識別子を比較できます、 **CompareEntryIDs**メッセージ ストアやアドレス帳コンテナーなどのより高レベル オブジェクトに最適に動作します。 下位レベルのオブジェクトを比較するには、直接比較のオブジェクトの検索キー (**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))) またはレコードのキー (**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)))。 
  
**OpenEntry**と同じようには、 **CompareEntryIDs**は、複数のオブジェクトによって実装されます。 **OpenEntry**と**CompareEntryID**を開く、または複数のオブジェクトについてわかっている情報の量に合わせて使用する方法を選択します。 どのインターフェイスのメソッドを呼び出すことを決定する際に、次のガイドラインを使用します。 
  
- 対象オブジェクトに関する情報がいない場合は、 [IMAPISession::OpenEntry](imapisession-openentry.md)または[IMAPISession::CompareEntryIDs](imapisession-compareentryids.md)を呼び出します。 この方法は、任意のオブジェクトへのアクセスを有効が 3 つの最も時間がかかります。
    
- ターゲット オブジェクトは、アドレス帳のエントリではなく、たとえば、フォルダーがわかっている場合は、[アドレス帳コンテナー](iaddrbook-openentry.md)または[IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md)メソッドを呼び出します。 **アドレス帳コンテナー**は、対象のオブジェクトとして NULL を指定した場合、アドレス帳のルート コンテナーを開きます。 この方法は、アドレス帳の任意のオブジェクトへのアクセスを有効にされ、 **IMAPISession**を使用するよりも高速ですが、 **IMAPIContainer**を使用するよりも遅くなります。
    
- 短期的なエントリ id は、エントリ id を使用している場合、またはターゲット オブジェクトを特定のアドレス帳コンテナーまたはフォルダーに属していることがわかっている場合は、 [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)メソッドを呼び出します。 この方法では、最速のパフォーマンスが得られますが、特定のコンテナーまたはフォルダー内のオブジェクトにのみアクセスできます。 
    

