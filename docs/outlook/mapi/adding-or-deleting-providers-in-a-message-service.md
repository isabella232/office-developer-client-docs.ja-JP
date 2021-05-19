---
title: メッセージ サービスでのプロバイダーの追加または削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44bb4d34-ca96-4d5a-93fe-85e09bd7971d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ed5ea8bdfcbdaaa6b6abd81a39f0e8df50d3b314
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433424"
---
# <a name="adding-or-deleting-providers-in-a-message-service"></a>メッセージ サービスでのプロバイダーの追加または削除

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ サービスでサービス プロバイダーを追加または削除するには [、IProviderAdmin : IUnknown インターフェイスを使用](iprovideradminiunknown.md) します。 [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md)を呼び出すことによって **、IProviderAdmin** ポインターを取得できます。 [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)を介してアクセス可能なプロバイダー テーブルには、メッセージ サービスに現在インストールされているサービス プロバイダーに関する情報が一覧表示されます。 クライアントとサービス プロバイダーは、プロバイダー テーブルを使用して、プロバイダー DLL ファイルの名前 ( **たとえば、MAPIUID、** 表示名、プロバイダーの種類、およびメッセージ サービスに関する情報) にアクセスできます。 詳細については、「プロバイダー テーブル [」を参照してください](provider-tables.md)。
  
 **メッセージ サービスでサービス プロバイダーを追加または削除するには**
  
1. **AdminServices メソッドを呼び出** して、メッセージ サービス管理オブジェクトにアクセスします。 
    
2. メッセージ [サービス テーブルにアクセスするには、IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) を呼び出します。 
    
3. 変更するメッセージ サービスの名前を持つ **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) または **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) と一致する [SPropertyRestriction](spropertyrestriction.md)構造体を使用してプロパティ制限を構築します。 
    
4. メッセージ サービス テーブルの [IMAPITable::FindRow](imapitable-findrow.md) メソッドを呼び出して、対象のメッセージ サービスを表すテーブル内の行を検索します。 
    
5. [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md)を呼び出して **、IProviderAdmin ポインターを取得** します。 メッセージ サービス **テーブルPR_SERVICE_UID** から 、lpUID パラメーターとして [PidTagServiceUid] 列を _渡_ します。[](pidtagserviceuid-canonical-property.md) 
    
6. [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)を呼び出して、プロバイダー テーブルにアクセスします。 
    
7. **追加** または削除するサービス プロバイダーの名前を持つ PR_DISPLAY_NAME ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) または **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) と一致する SPropertyRestriction 構造体を使用してプロパティ制限を構築します。 
    
8. プロバイダー テーブルの [IMAPITable::FindRow](imapitable-findrow.md) メソッドを呼び出して、対象のサービス プロバイダーを表すテーブル内の行を検索します。 
    
9. [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md)を呼び出して、プロバイダーまたは[IProviderAdmin::D eleteProvider](iprovideradmin-deleteprovider.md)を追加して、メッセージ サービスから削除します。 **CreateProvider の場合** は、プロバイダーの **PR_DISPLAY_NAMEを**_lpszProvider パラメーターとして渡_ します。 どちらのメソッドでも、プロバイダーのプロパティPR_SERVICE_UID  _lpUID パラメーターとして渡_ します。 サービス プロバイダーが追加または削除された後、新しいセッションが作成されるまで変更は表示されません。 
    
サービス プロバイダー (特にメッセージ ストア プロバイダー) をプロファイルに追加するもう 1 つの方法は、プロバイダーのエントリ識別子を作成する方法です。 エントリ識別子を作成するには、その形式に関する知識が必要なので、この手法を使用できるのは、サービス プロバイダーがエントリ識別子形式をパブリックにしている場合のみです。 
  
新しく作成されたエントリ識別子を使用して、クライアントは [IMAPISession::OpenMsgStore を呼び出します](imapisession-openmsgstore.md)。 MAPI は、サービス プロバイダーのプロファイルにプロファイル セクションを自動的に作成しますが、メッセージ サービスには追加されません。 
  
一部のメッセージ サービスでは、この種類の動的変更を許可しない場合があります。サポートされるかどうかは、メッセージ サービスによって決定されます。 サポートされる場合とサポートされない可能性があるもう 1 つの機能は、メッセージ サービスのプライベート プロファイル セクションに直接アクセスする機能です。 使用しているメッセージ サービスがこのようなアクセスを許可している場合は、MAPISVC.INF のプライベート セクションを表す GUID が発行されます。  この GUID を[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md)への呼び出しで渡して、プロファイル セクションにアクセスできます。  
  

