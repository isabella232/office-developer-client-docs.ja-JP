---
title: メッセージサービスでのプロバイダーの追加または削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44bb4d34-ca96-4d5a-93fe-85e09bd7971d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ed5ea8bdfcbdaaa6b6abd81a39f0e8df50d3b314
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329562"
---
# <a name="adding-or-deleting-providers-in-a-message-service"></a>メッセージサービスでのプロバイダーの追加または削除

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージサービスのサービスプロバイダーを追加または削除するには、 [IProviderAdmin: IUnknown](iprovideradminiunknown.md)インターフェイスを使用します。 **IProviderAdmin**ポインターを取得するには、 [IMsgServiceAdmin:: adminproviders](imsgserviceadmin-adminproviders.md)を呼び出します。 [IProviderAdmin:: getprovidertable](iprovideradmin-getprovidertable.md)を使用してアクセスできるプロバイダテーブルには、現在メッセージサービスにインストールされているサービスプロバイダに関する情報を一覧表示します。 クライアントおよびサービスプロバイダーは、プロバイダテーブルを使用して、プロバイダー DLL ファイルの名前、プロバイダーの**MAPIUID**、表示名、種類、およびメッセージサービスに関する情報にアクセスできます。 詳細については、「[プロバイダテーブル](provider-tables.md)」を参照してください。
  
 **メッセージサービスのサービスプロバイダーを追加または削除するには**
  
1. **adminservices**メソッドを呼び出して、メッセージサービス管理オブジェクトにアクセスします。 
    
2. message service テーブルにアクセスするには、 [IMsgServiceAdmin:: getmsgservicetable](imsgserviceadmin-getmsgservicetable.md)を呼び出します。 
    
3. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) または**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) と一致する[spropertyrestriction](spropertyrestriction.md)構造を使用して、メッセージサービスの名前を持つプロパティ制限を構築します。れ. 
    
4. メッセージサービステーブルの[IMAPITable:: FindRow](imapitable-findrow.md)メソッドを呼び出して、対象のメッセージサービスを表すテーブル内の行を検索します。 
    
5. [IMsgServiceAdmin:: adminproviders](imsgserviceadmin-adminproviders.md)を呼び出して、 **IProviderAdmin**ポインターを取得します。 _lpuid_パラメーターとして、message SERVICE table 行の**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) 列を渡します。 
    
6. プロバイダーテーブルにアクセスするには、 [IProviderAdmin:: getprovidertable](iprovideradmin-getprovidertable.md)を呼び出します。 
    
7. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) または**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) と一致する spropertyrestriction 構造を使用して、プロパティ制限をサービスプロバイダーの名前に作成します。追加または削除されました。 
    
8. プロバイダーテーブルの[IMAPITable:: FindRow](imapitable-findrow.md)メソッドを呼び出して、対象となるサービスプロバイダーを表すテーブル内の行を検索します。 
    
9. [IProviderAdmin:: createprovider](iprovideradmin-createprovider.md)を呼び出して、プロバイダまたは[IProviderAdmin::D eleteprovider](iprovideradmin-deleteprovider.md)を追加し、メッセージサービスから削除します。 **createprovider**の場合は、プロバイダーの**PR_DISPLAY_NAME**プロパティを_lpszprovider_パラメーターとして渡します。 どちらの方法でも、プロバイダーの**PR_SERVICE_UID**プロパティを_lpuid_パラメーターとして渡します。 サービスプロバイダーを追加または削除した後は、新しいセッションが作成されるまで、変更内容は明らかになりません。 
    
サービスプロバイダー、特にメッセージストアプロバイダーをプロファイルに追加するためのもう1つの方法は、プロバイダーのエントリ識別子を構築することです。 エントリ識別子を作成するには、その形式に関する知識が必要ですので、この手法は、サービスプロバイダーがエントリ識別子の形式をパブリックにしている場合にのみ使用できます。 
  
新しく構築されたエントリ識別子を使用すると、クライアントは[imapisession:: openmsgstore](imapisession-openmsgstore.md)を呼び出すことができます。 MAPI は、サービスプロバイダーのプロファイルにプロファイルセクションを自動的に作成しますが、メッセージサービスには追加しません。 
  
一部のメッセージサービスでは、この種の動的変更を許可しません。サポートされているかどうかは、メッセージサービスによってサポートされています。 他にも、サポートされているかどうかは、メッセージサービスのプライベートプロファイルセクションに直接アクセスできる機能です。 使用しているメッセージサービスがこのようなアクセスを許可する場合は、mapisvc.inf のプライベートセクションを表す**GUID**を公開します。 この**GUID**は、 [IProviderAdmin:: openprofile](iprovideradmin-openprofilesection.md)の呼び出しで、プロファイルセクションにアクセスするために渡すことができます。 
  

