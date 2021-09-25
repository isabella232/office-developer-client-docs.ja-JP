---
title: MAPI プライマリ ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8787a873-6752-4b17-8ea3-8fed793e1371
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dd0ffa1d8c9d2b8b8a65fd8434fc382f6ee77547
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610238"
---
# <a name="mapi-primary-identity"></a>MAPI プライマリ ID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ほとんどの MAPI セッションには、セッションのプライマリ ID を提供する特定のサービス プロバイダーがあります。 通常、これはアドレス帳プロバイダーで、メッセージング ユーザー オブジェクトまたは配布リストのいずれかを通じて ID を提供します。 実際、MAPI では、アドレス帳プロバイダーを含むメッセージ サービスがプライマリ ID に対してそのオブジェクトの 1 つを使用する必要があります。 メッセージ サービスに属するサービス プロバイダーがプライマリ ID を提供する場合、メッセージ サービス内の他のすべてのサービス プロバイダーは、この ID を共有します。
  
MAPISVC。INF 構成ファイルには、メッセージ サービスとサービス プロバイダー レベルの両方の ID に関連するエントリがあります。 メッセージ サービス セクションには、サービスがプライマリ ID を提供できるかどうかを示すエントリが含まれる必要があります。サービス プロバイダー セクションには、プロバイダーが ID を指定できる場合にのみ、同様のエントリが含まれます。
  
次の表に、MAPISVC のメッセージ サービスとサービス プロバイダーのセクションに表示されるエントリの一覧を示します。INF ファイル。
  
|**プライマリ ID サプライヤー**|**PR_RESOURCE_FLAGS設定**|
|:-----|:-----|
|メッセージ サービス  <br/> | `SERVICE_PRIMARY_IDENTITY` <br/> |
|メッセージ サービスではない  <br/> | `SERVICE_NO_PRIMARY_IDENTITY` <br/> |
|サービス プロバイダー  <br/> | `STATUS_PRIMARY_IDENTITY` <br/> |
   
複数のメッセージ サービスがセッションのプライマリ ID を提供する機能を宣言することができますが、これを行うメッセージ サービスは 1 つしか選択されません。 この選択は次の場合に発生します。
  
- プロファイルが作成された場合。
    
- クライアントが **IMsgServiceAdmin::SetPrimaryIdentity** を呼び出して、特定のメッセージ サービスをセッション ID のプロバイダーとして明示的に確立する場合。 詳細については、次の情報を参照してください。 [「IMsgServiceAdmin::SetPrimaryIdentity」を参照してください](imsgserviceadmin-setprimaryidentity.md)。
    
プロファイルが作成されると、MAPI は **、PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティに STATUS_PRIMARY_IDENTITY フラグが設定されたプロバイダーを含む構成する最初のメッセージ サービスを指定して、プライマリ ID を指定します。 指定されたメッセージ サービス内で、このリソース フラグセットを使用して構成される最初のプロバイダーが、サービスの ID を提供するように選択されます。 指定STATUS_PRIMARY_IDENTITY内の他のすべてのプロバイダーと、プロファイル内の他のメッセージ サービスに対して、このフラグがクリアされます。 プライマリ ID を提供するプロバイダーがプロファイルから削除されると、MAPI は、ID を提供できる構成する次のプロバイダーに役割を割り当てる。 これは、MAPISVC.INF のプロバイダーのセクションのエントリの  `PR_RESOURCE_FLAGS=STATUS_PRIMARY_IDENTITY` 外観によって決まります。 
  
クライアントがメッセージ サービスの **IMsgServiceAdmin::SetPrimaryIdentity** メソッドを呼び出す場合、ターゲット サービス内のサービス プロバイダーの MAPIUID を指定します。 詳細については [、「MAPIUID」を参照してください](mapiuid.md)。 **MAPIUID** によって表されるサービス プロバイダーは、メッセージ サービスとセッションのプライマリ ID を提供するために割り当て、サービス内の他のすべてのプロバイダーは、この ID を共有します。 
  
プライマリ ID の提供を担当するメッセージ サービスのすべてのプロバイダーは、次のプロパティを含む状態テーブルの行を更新します。
  
|**プライマリ ID プロパティ**|**設定値**|
|:-----|:-----|
|**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))  <br/> |プライマリ ID を指定するオブジェクトの表示名。  <br/> |
|**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))  <br/> |プライマリ ID を指定するオブジェクトの検索キー。  <br/> |
|**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))  <br/> |プライマリ ID を指定するオブジェクトのエントリ識別子。  <br/> |
   
 **プライマリ ID を指定するオブジェクトのエントリ識別子を取得するには**
  
- **IMAPISession::QueryIdentity メソッドを呼び出** します。 詳細については [、「IMAPISession::QueryIdentity」を参照してください](imapisession-queryidentity.md)。 **QueryIdentity** は **、PR_RESOURCE_FLAGS** 列の値 STATUS_PRIMARY_IDENTITY を含む行の状態テーブルを検索し、対応する **PR_IDENTITY_ENTRYID** をプライマリ ID のエントリ識別子として返します。 
    

