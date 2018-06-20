---
title: MAPI のプライマリ Id
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8787a873-6752-4b17-8ea3-8fed793e1371
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: bd6fe1298a38733cb9d4916a931138c616e110bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801416"
---
# <a name="mapi-primary-identity"></a>MAPI のプライマリ Id

  
  
**適用されます**: Outlook 
  
ほとんどの MAPI セッションには、セッションのプライマリ id を提供する特定のサービス プロバイダーがあります。 通常、そのメッセージ オブジェクトをユーザーまたは配布リストのいずれかを通じて id を提供する、アドレス帳プロバイダーです。 実際には、MAPI では、アドレス帳プロバイダーは、メッセージ サービスを使用して、そのオブジェクトのいずれかのプライマリ id のお勧めします。 メッセージ サービスが属するサービス ・ プロバイダーには、プライマリ id が用意されて、すべての他のサービス プロバイダーは、メッセージ サービスでこの id を共有します。
  
MAPISVC。INF の構成ファイルには、メッセージ サービスとサービス プロバイダーのレベルの両方で id に関連するエントリがあります。 メッセージ サービスのセクションでは、サービスがプライマリ id; を提供できるかどうかを示すエントリを含める必要があります。サービス プロバイダー セクションには、プロバイダー id を指定できる場合にのみのようなエントリが含まれます。
  
メッセージ サービスと、MAPISVC のサービスのプロバイダー セクションに表示されるエントリを次の表に一覧します。INF ファイルです。
  
|**プライマリ id サプライヤー**|**PR_RESOURCE_FLAGS の設定**|
|:-----|:-----|
|メッセージ サービス  <br/> | `SERVICE_PRIMARY_IDENTITY` <br/> |
|メッセージ サービスではなく  <br/> | `SERVICE_NO_PRIMARY_IDENTITY` <br/> |
|サービス プロバイダー  <br/> | `STATUS_PRIMARY_IDENTITY` <br/> |
   
複数のメッセージ サービスは、セッションのプライマリ id を提供する機能を宣言できます、これを行う 1 つのメッセージ サービスが選択されます。 このオプションを選択に発生することができます。
  
- プロファイルの作成時。
    
- クライアントが明示的にセッション id のプロバイダーとして、特定のメッセージ サービスを確立するために**IMsgServiceAdmin::SetPrimaryIdentity**を呼び出すとします。 詳細については。 [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)を参照してください。
    
MAPI がメッセージする最初のサービスを構成するプライマリ id を指定するのには、 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) のプロパティの設定 STATUS_PRIMARY_IDENTITY フラグを使用してプロバイダーを含むを指定するプロファイルが作成されると、. 指定されたメッセージ サービス内でサービスの id を提供するこのリソース フラグを設定して構成する最初のプロバイダーが選択されます。 指定されたサービスおよびその他のメッセージのサービス プロファイルにその他のすべてのプロバイダーは、STATUS_PRIMARY_IDENTITY フラグがクリアされます。 いつでもプライマリ id を提供するプロバイダーをプロファイルから削除する場合、MAPI には、識別情報を提供できるように構成するのには次のプロバイダーにロールが割り当てられます。 外観によって決定される、 `PR_RESOURCE_FLAGS=STATUS_PRIMARY_IDENTITY` MAPISVC.INF のプロバイダーのセクション内のエントリです。 
  
クライアントは、メッセージ サービスの**IMsgServiceAdmin::SetPrimaryIdentity**メソッドを呼び出す、ときに、対象となるサービス内のサービス ・ プロバイダーの MAPIUID を指定します。 詳細については、 [MAPIUID](mapiuid.md)を参照してください。 メッセージ サービスとのセッションでは、プライマリ id を提供する**MAPIUID**によって表されるサービスのプロバイダーが割り当てられているし、この id を共有するすべてのサービスで他のプロバイダーです。 
  
プライマリ id を指定することを担当するメッセージ サービスのすべてのプロバイダーでは、次のプロパティを含める状態テーブル内の行を更新します。
  
|**プライマリ id のプロパティ**|**設定値**|
|:-----|:-----|
|**PR_IDENTITY_DISPLAY**([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))  <br/> |プライマリ id を提供するオブジェクトの名前を表示します。  <br/> |
|**PR_IDENTITY_SEARCH_KEY**([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))  <br/> |プライマリ id を提供するオブジェクトのキーを検索します。  <br/> |
|**PR_IDENTITY_ENTRYID**([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))  <br/> |プライマリ id を提供するオブジェクトのエントリ id です。  <br/> |
   
 **プライマリ id を提供するオブジェクトのエントリ id を取得するには**
  
- **IMAPISession::QueryIdentity**メソッドを呼び出します。 詳細については、 [IMAPISession::QueryIdentity](imapisession-queryidentity.md)を参照してください。 **QueryIdentity** 、 **PR_RESOURCE_FLAGS**列の値 STATUS_PRIMARY_IDENTITY が含まれていますし、エントリの識別子として、主に対応する**PR_IDENTITY_ENTRYID**を返します行の状態テーブルを検索します。id です。 
    

