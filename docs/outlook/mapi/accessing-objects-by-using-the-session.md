---
title: セッションを使用してオブジェクトにアクセスする
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ecada707-2960-41ec-be7e-619cad257c57
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a76397b74642aedf9ad5c9704735d869f61db7e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410540"
---
# <a name="accessing-objects-by-using-the-session"></a>セッションを使用してオブジェクトにアクセスする

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[MAPILogonEx](mapilogonex.md)の呼び出しから受け取ったセッションポインターを使用して、さまざまなオブジェクトにアクセスできます。 次の表に、さまざまなオブジェクトへのアクセスに使用されるメソッドを示します。 
  
|**Object**|**Session メソッド**|
|:-----|:-----|
|プロファイルセクション  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|メッセージストア  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|アドレス帳  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|メッセージサービスの管理オブジェクト  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|フォルダー、メッセージ、アドレス帳コンテナー、配布リスト、またはメッセージングユーザー  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
**openentry**メソッドと有効なエントリ識別子を使用すると、任意のアドレス帳またはメッセージストアプロバイダーオブジェクトを開くことができます。 **imapisession**メソッドに加えて、MAPI には、他にも**openentry**メソッドがあります。 **openentry**は、次のオブジェクトに実装されています。 
  
|**Object**|**メソッド**|
|:-----|:-----|
|アドレス帳プロバイダーのログオンオブジェクト  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md) <br/> |
|アドレス帳  <br/> |[IAddrBook::OpenEntry](iaddrbook-openentry.md) <br/> |
|アドレス帳コンテナー  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Session  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
|メッセージストア  <br/> |[IMsgStore::OpenEntry](imsgstore-openentry.md) <br/> |
|メッセージストアプロバイダーのログオンオブジェクト  <br/> |[IMSLogon::OpenEntry](imslogon-openentry.md) <br/> |
|フォルダー  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|サポートオブジェクト  <br/> |[IMAPISupport::OpenEntry](imapisupport-openentry.md) <br/> |
   
一部の**openentry**メソッドは、 **imapisession:: openentry**のように、開くオブジェクトのエントリ識別子を必要とします。その他のメソッドを使用すると、NULL を指定できます。 NULL エントリ識別子は、オブジェクトに応じて異なる方法で解釈されます。 たとえば、NULL エントリ識別子を持つ**IAddrBook:: openentry**を呼び出すと、MAPI はアドレス帳のルートコンテナーを開きます。 メッセージストアの**openentry**メソッドは同じように動作します。メッセージストアのルートフォルダーを開きます。 **IMAPIContainer:: openentry**は、フォルダーとアドレス帳コンテナーの両方で実装されている場合があります。実装に応じて、MAPI_E_INVALID_PARAMETER またはルートコンテナーが返される場合があります。 
  
エントリ識別子に NULL 値を使用しないことに加えて、セッションの**openentry**メソッドは、そのジョブがオブジェクトを開かないため、他の**openentry**メソッドとは異なります。 代わりに、エントリ id を調べて、適切なサービスプロバイダーによって実装されている別の**openentry**メソッドに呼び出しを転送します。 たとえば、メッセージのエントリ識別子を含む**imapisession:: openentry**を呼び出すと、MAPI はメッセージを処理するメッセージストアの**IMSLogon:: openentry**メソッドを呼び出します。 
  
クライアントは、セッションを使用してオブジェクトを開くだけでなく、それらを使用してオブジェクトを比較します。 [imapisession:: compareentryids](imapisession-compareentryids.md)メソッドは、エントリ識別子を比較してオブジェクトを比較します。 エントリ識別子に含まれている[MAPIUID](mapiuid.md)構造が同じサービスプロバイダーに属している場合、MAPI はそのプロバイダーに呼び出しを転送します。 **compareentryids**は、2つのエントリ識別子が一致しない場合にエラー値を返します。 このメソッドは、任意の種類のオブジェクトに属するエントリ識別子を比較できますが、 **compareentryids**は、メッセージストアやアドレス帳コンテナーなどの上位レベルのオブジェクトに最適です。 下位レベルのオブジェクトを比較するには、オブジェクトの検索キー (**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))) またはレコードキー (**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))) を直接比較します。 
  
**openentry**と同様に、 **compareentryids**は複数のオブジェクトで実装されています。 開かれるか、または比較されるオブジェクトについての情報量に応じて、どの**openentry**および**compareentryid**メソッドを使用するかを選択します。 呼び出すインターフェイスメソッドを決定する際には、次のガイドラインを使用します。 
  
- ターゲットオブジェクトに関する情報がない場合は、 [imapisession:: openentry](imapisession-openentry.md)または[imapisession:: compareentryids](imapisession-compareentryids.md)を呼び出します。 この方法を使用すると、任意のオブジェクトにアクセスできますが、3つのうち最も低速です。
    
- ターゲットオブジェクトがフォルダーなどではなく、アドレス帳のエントリであることがわかっている場合は、 [IAddrBook:: openentry](iaddrbook-openentry.md)または[IAddrBook:: compareentryids](iaddrbook-compareentryids.md)メソッドを呼び出します。 **IAddrBook:: openentry**は、ターゲットオブジェクトとして NULL が指定されている場合に、アドレス帳のルートコンテナーを開きます。 この方法を使用すると、アドレス帳オブジェクトへのアクセスが可能になり、 **imapisession**を使用するよりも高速になりますが、 **IMAPIContainer**を使用するよりも時間がかかります。
    
- 使用されているエントリ識別子が短い用語エントリ識別子である場合、または対象のオブジェクトが特定のアドレス帳のコンテナーまたはフォルダーに属していることがわかっている場合は、 [IMAPIContainer:: openentry](imapicontainer-openentry.md)メソッドを呼び出します。 この方法では、最速のパフォーマンスが得られますが、特定のコンテナーまたはフォルダー内のオブジェクトへのアクセスのみが可能になります。 
    

