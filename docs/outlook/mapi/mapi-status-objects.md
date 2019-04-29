---
title: MAPI 状態オブジェクト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 816d1b7c9c0b8c5a80a2351580ce3224fccf0b14
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406746"
---
# <a name="mapi-status-objects"></a>MAPI 状態オブジェクト

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Status オブジェクトは、MAPI リソースに関する情報を報告します。 たとえば、サービスプロバイダー、MAPI の送受信プロセス、またはアドレス帳などです。
  
status オブジェクトは、現在のプロファイル内の各サービスプロバイダーに関する情報を提供します。 mapi は、サブシステム、mapi の送受信プロセス、およびアドレス帳の状態オブジェクトの実装を担当します。 サブシステム状態オブジェクトは、グローバル情報を提供します。 統合されたアドレス帳の status オブジェクトは、現在動作しているすべてのアドレス帳プロバイダーの状態を提供します。
  
すべての status オブジェクトは状態テーブルに含まれています。このテーブルは、セッションのすべてのステータス情報をクライアントに提供する MAPI で保持されます。 詳細については、「 [Status Tables](status-tables.md)」を参照してください。 クライアントは、テーブルまたはサービスプロバイダーの場合は、そのログオンオブジェクトを通じて、特定の状態オブジェクトにアクセスできます。 たとえば、アドレス帳プロバイダーの状態オブジェクトにアクセスするために、クライアントは**IABLogon:: openstatusentry**を呼び出すことができます。 詳細については、「 [IABLogon:: openstatusentry](iablogon-openstatusentry.md)」を参照してください。
  
クライアントは、status オブジェクトを使用して次のことを行えます。
  
- セッションの状態について説明します。
    
- サービスプロバイダーを監視します。
    
- メッセージ送信を制御します。
    
- リソースの構成と状態を表示または変更します。
    
すべての status オブジェクトは、 **imapistatus**インターフェイスを実装します。 詳細については、「 [imapistatus: imapistatus](imapistatusimapiprop.md)」を参照してください。 ただし、すべてのステータスオブジェクトがすべての**imapistatus**メソッドを完全にサポートするわけではありません。 status オブジェクトでサポートされているメソッドにはバリエーションがあるため、クライアントは、使用する前に、特定の状態オブジェクトについて知る必要があります。 状態オブジェクトは、それぞれの機能に関する情報を次の3つのプロパティに公開するために必要です。 
  
 **PR_RESOURCE_METHODS**([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) 
  
 **PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 
  
 **PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) 
  
状態オブジェクトの実装の詳細については、「 [status オブジェクトの実装](status-object-implementation.md)」を参照してください。 status オブジェクトの使用の詳細については、「 [status Table and status Objects](status-table-and-status-objects.md)」を参照してください。
  

