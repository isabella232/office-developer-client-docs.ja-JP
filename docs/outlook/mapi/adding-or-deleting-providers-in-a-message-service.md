---
title: メッセージ サービスのプロバイダーの追加または削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44bb4d34-ca96-4d5a-93fe-85e09bd7971d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 569c9d8a7ed3f56d88d83ea6fdac4477d39e50a2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569485"
---
# <a name="adding-or-deleting-providers-in-a-message-service"></a>メッセージ サービスのプロバイダーの追加または削除

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ サービスのサービス プロバイダーを追加削除するを使用して、 [IProviderAdmin: IUnknown](iprovideradminiunknown.md)インタ フェースです。 [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md)を呼び出すことによって、 **IProviderAdmin**ポインターを取得できます。 プロバイダー テーブルでは、 [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)からアクセスでは、メッセージ サービスで現在インストールされているサービス プロバイダーに関する情報が表示されます。 クライアントとサービス ・ プロバイダーは、プロバイダー DLL ファイルまたは**MAPIUID**表示名、およびメッセージ サービスに関する情報だけでなくプロバイダーの型の名前にアクセスするのにはプロバイダーのテーブルを使用できます。 詳細については、[プロバイダーのテーブル](provider-tables.md)を参照してください。
  
 **メッセージ サービスのサービス プロバイダーを追加、削除します。**
  
1. メッセージ サービス管理オブジェクトにアクセスする**AdminServices**メソッドを呼び出します。 
    
2. メッセージ サービス テーブルにアクセスするのには[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)を呼び出します。 
    
3. 構築するメッセージ サービスの名前の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) または**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) に一致する[SPropertyRestriction](spropertyrestriction.md)構造体を使用してプロパティの制限変更します。 
    
4. メッセージ サービス テーブルの[IMAPITable::FindRow](imapitable-findrow.md)メソッドを呼び出してメッセージを対象となるサービスを表すテーブルの行を探します。 
    
5. **IProviderAdmin**ポインターを取得するために[IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md)を呼び出します。 メッセージ サービス テーブルの行から**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) の列を_lpUID_パラメーターとして渡します。 
    
6. プロバイダー テーブルにアクセスするのには[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)を呼び出します。 
    
7. ビルドするサービス プロバイダーの名前の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) または**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) に一致する SPropertyRestriction 構造体を使用してプロパティの制限追加または削除します。 
    
8. 対象となるサービス プロバイダーを表すテーブルの行を検索するプロバイダーのテーブルの[IMAPITable::FindRow](imapitable-findrow.md)のメソッドを呼び出します。 
    
9. プロバイダーを追加するのには[IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md)またはメッセージ サービスから削除するのには[IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md)を呼び出します。 **CreateProvider**プロバイダーの**PR_DISPLAY_NAME**プロパティを_lpszProvider_パラメーターとして渡します。 いずれかの方法では、 _lpUID_パラメーターとして、プロバイダーの**PR_SERVICE_UID**プロパティを渡します。 サービス プロバイダーを追加または削除した後、変更は新しいセッションが作成されるまで、見かけ上はできません。 
    
具体的には、メッセージ ストア プロバイダー、サービス ・ プロバイダーをプロファイルに追加するための別の方法では、プロバイダーのエントリ識別子を構築する必要があります。 エントリ識別子を作成するには、形式の知識が必要とするためこの方法のみ使用できます、サービス ・ プロバイダーが行った場合、エントリの識別子の形式公開。 
  
新たに構築されたエントリの識別子、クライアントは[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)を呼び出すことができます。 MAPI は自動的に、サービス プロバイダーには、プロファイルのプロファイル セクションを作成が、メッセージ サービスには追加されません。 
  
メッセージの一部のサービスをこの種類の動的な変更は許可しません。メッセージ サービスがサポートされているかどうか。 サポートされていない可能性があります別の機能は、メッセージ サービスのプライベート プロファイルのセクションに直接アクセスする機能です。 使用しているメッセージ サービスは、このようなアクセスを許可する場合、MAPISVC.INF の秘密のセクションを表す**GUID**が発行されます。 プロファイル セクションにアクセスするのには[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md)の呼び出しでは、この**GUID**を渡すことができます。 
  

