---
title: MAPI 状態オブジェクト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2572e7d5d203a53de5c28a5eed0acbf415b81da2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579489"
---
# <a name="mapi-status-objects"></a>MAPI 状態オブジェクト

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Status オブジェクトは、MAPI リソースに関する情報を報告します。 たとえば、サービス プロバイダー、MAPI 送受信プロセス、アドレス帳などです。
  
現在のプロファイルには、個々のサービス プロバイダーに関する情報を提供する状態オブジェクトがあります。 MAPI は、サブシステム、MAPI 送受信プロセス、およびアドレス帳の状態オブジェクトを実装する責任があります。 サブシステムの状態オブジェクトは、グローバル情報を提供します。 統合アドレス帳の status オブジェクトは、現在動作しているすべてのアドレス帳プロバイダーの状態を提供します。
  
すべての status オブジェクトは、セッションのすべての状態情報をクライアントに提供する MAPI によって管理されるテーブルである状態テーブルに含まれます。 詳細については、「Status [Tables」を参照してください](status-tables.md)。 クライアントは、テーブルまたはサービス プロバイダーのログオン オブジェクトを介して、特定の状態オブジェクトにアクセスできます。 たとえば、アドレス帳プロバイダーの状態オブジェクトにアクセスするために、クライアントは **IABLogon::OpenStatusEntry を呼び出します**。 詳細については [、「IABLogon::OpenStatusEntry」を参照してください](iablogon-openstatusentry.md)。
  
クライアントは、状態オブジェクトを使用して、次の操作を実行できます。
  
- セッションの状態について学習します。
    
- サービス プロバイダーを監視します。
    
- メッセージの送信を制御します。
    
- リソースの構成と状態を表示または変更します。
    
すべての status オブジェクトは **、IMAPIStatus インターフェイスを実装** します。 詳細については [、「IMAPIStatus : IMAPIProp 」を参照してください](imapistatusimapiprop.md)。 ただし、すべての状態オブジェクトがすべての **IMAPIStatus メソッドを完全にサポートしているわけではありません** 。 status オブジェクトでサポートされるメソッドにはバリエーションが存在しますので、クライアントは、それを使用する前に、特定の状態オブジェクトについて学習する必要があります。 Status オブジェクトは、次の 3 つのプロパティで機能に関する情報を公開するために必要です。 
  
 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) 
  
 **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 
  
 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) 
  
status オブジェクトの実装の詳細については、「Status [Object Implementation」を参照してください](status-object-implementation.md)。 status オブジェクトの使用の詳細については、「Status [Table and Status Objects」を参照してください](status-table-and-status-objects.md)。
  

