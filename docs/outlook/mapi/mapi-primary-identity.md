---
title: MAPI プライマリ id
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8787a873-6752-4b17-8ea3-8fed793e1371
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5bf88de280b012c54d4caaac6bdfe877f476ac37
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404723"
---
# <a name="mapi-primary-identity"></a>MAPI プライマリ id

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ほとんどの MAPI セッションには、セッションのプライマリ id を提供する特定のサービスプロバイダーがあります。 通常、アドレス帳プロバイダーは、メッセージングユーザーオブジェクトまたは配布リストのいずれかを使用して id を提供します。 実際に、MAPI では、アドレス帳プロバイダーを含むメッセージサービスがプライマリ id に対してオブジェクトの1つを使用することをお勧めします。 メッセージサービスに属するサービスプロバイダーがプライマリ id を提供すると、メッセージサービス内の他のすべてのサービスプロバイダーがこの id を共有します。
  
mapisvc.inf。INF 構成ファイルには、メッセージサービスとサービスプロバイダーレベルの両方で id に関連するエントリがあります。 メッセージサービスセクションには、サービスがプライマリ id を提供できるかどうかを示すエントリを含める必要があります。サービスプロバイダーのセクションには、プロバイダーが id を提供できる場合にのみ、同様のエントリが含まれます。
  
次の表に、mapisvc.inf のメッセージサービスおよびサービスプロバイダーのセクションに表示されるエントリを示します。INF ファイル
  
|**プライマリ id サプライヤー**|**PR_RESOURCE_FLAGS 設定**|
|:-----|:-----|
|メッセージサービス  <br/> | `SERVICE_PRIMARY_IDENTITY` <br/> |
|メッセージサービスではありません  <br/> | `SERVICE_NO_PRIMARY_IDENTITY` <br/> |
|サービスプロバイダー  <br/> | `STATUS_PRIMARY_IDENTITY` <br/> |
   
複数のメッセージサービスは、セッションのプライマリ id を提供する機能を宣言できますが、そのために選択されているメッセージサービスは1つだけです。 次の選択が可能です。
  
- プロファイルが作成されたとき。
    
- クライアントが**IMsgServiceAdmin:: setprimaryidentity**を呼び出して、特定のメッセージサービスをセッション id のプロバイダーとして明示的に確立するとき。 を参照してください。 「 [IMsgServiceAdmin:: setprimaryidentity](imsgserviceadmin-setprimaryidentity.md)」を参照してください。
    
プロファイルが作成されると、MAPI は、STATUS_PRIMARY_IDENTITY フラグを**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) プロパティに設定してプライマリ id を指定したプロバイダーを含む、構成する最初のメッセージサービスを指定します。. 指定したメッセージサービス内で、このリソースフラグセットを使用して構成する最初のプロバイダーが、サービスの id を提供するために選択されます。 STATUS_PRIMARY_IDENTITY フラグは、指定されたサービス内の他のすべてのプロバイダーと、プロファイル内の他のメッセージサービスに対してクリアされます。 プライマリ id を提供するプロバイダーがプロファイルから削除されるたびに、MAPI は、id を提供できる次のプロバイダーに役割を割り当てます。 これは、mapisvc.inf のプロバイダーのセクション`PR_RESOURCE_FLAGS=STATUS_PRIMARY_IDENTITY`にあるエントリの外観によって決まります。 
  
クライアントは、message service の**IMsgServiceAdmin:: setprimaryidentity**メソッドを呼び出すときに、ターゲットサービス内のサービスプロバイダーの MAPIUID を指定します。 詳細については、「 [MAPIUID](mapiuid.md)」を参照してください。 **MAPIUID**によって表されるサービスプロバイダーは、メッセージサービスとセッションのプライマリ id を指定するために割り当てられ、サービス内の他のすべてのプロバイダーがこの id を共有します。 
  
プライマリ id の指定を担当するメッセージサービスのすべてのプロバイダーは、次のプロパティを含むように状態テーブルの行を更新します。
  
|**プライマリ id プロパティ**|**設定値**|
|:-----|:-----|
|**PR_IDENTITY_DISPLAY**([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))  <br/> |プライマリ id を提供するオブジェクトの表示名。  <br/> |
|**PR_IDENTITY_SEARCH_KEY**([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))  <br/> |プライマリ id を提供するオブジェクトの検索キー。  <br/> |
|**PR_IDENTITY_ENTRYID**([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))  <br/> |プライマリ id を提供するオブジェクトのエントリ識別子。  <br/> |
   
 **プライマリ id を提供するオブジェクトのエントリ識別子を取得するには**
  
- **imapisession:: queryidentity**メソッドを呼び出します。 詳細については、「 [imapisession:: queryidentity](imapisession-queryidentity.md)」を参照してください。 **queryidentity**は、 **PR_RESOURCE_FLAGS**列の値 STATUS_PRIMARY_IDENTITY が含まれている行の状態テーブルを検索し、プライマリのエントリ識別子として対応する**PR_IDENTITY_ENTRYID**を返します。独自性. 
    

