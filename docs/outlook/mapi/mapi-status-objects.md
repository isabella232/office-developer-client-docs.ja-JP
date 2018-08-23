---
title: MAPI オブジェクトのステータス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 38310619-1b1d-4934-8533-d0612676c0b0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 69a4d25fc6a7abec68c94cc947e5944322d230a6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594951"
---
# <a name="mapi-status-objects"></a>MAPI オブジェクトのステータス

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
状態オブジェクトは、MAPI リソースに関する情報をレポートします。 などのサービス プロバイダー、MAPI 送信/受信プロセス、またはアドレス帳に。
  
状態オブジェクトが現在のプロファイルで個々 のサービス プロバイダーに関する情報を指定することがあります。 MAPI は、サブシステム、MAPI 送信/受信プロセス、およびアドレス帳のステータスのオブジェクトを実装する必要があります。 サブシステムの状態オブジェクトは、グローバルな情報を提供します。 統合アドレス帳のステータスのオブジェクトには、動作しているすべてのアドレス帳プロバイダーの状態が用意されています。
  
状態テーブルのすべてのセッションの状態情報をクライアントに提供する MAPI によって保持されるテーブルでは、ステータスのすべてのオブジェクトが含まれます。 詳細については、[ステータス ・ テーブル](status-tables.md)を参照してください。 テーブルまたは、サービス プロバイダーに、そのログオン オブジェクトをクライアントは、特定のステータスのオブジェクトにアクセスできます。 たとえば、アドレス帳プロバイダーの状態のオブジェクトにアクセスするに、クライアントは**IABLogon::OpenStatusEntry**を呼び出すことができます。 詳細については、 [IABLogon::OpenStatusEntry](iablogon-openstatusentry.md)を参照してください。
  
クライアントは、オブジェクトの状態を使用できます。
  
- セッションの状態について説明します。
    
- サービス プロバイダーを監視します。
    
- メッセージの転送を制御します。
    
- 表示またはリソースの構成とステータスを変更します。
    
ステータスのすべてのオブジェクトは、 **IMAPIStatus**インターフェイスを実装します。 詳細についてを参照してください[IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)。 ただし、すべての状態のオブジェクトは完全に**IMAPIStatus**のすべてのメソッドをサポートします。 ステータス オブジェクトでサポートされているメソッドのバリエーションがあるため、クライアントを使用できるようにする前に、特定のステータスのオブジェクトについて説明する必要があります。 状態オブジェクトは、次の 3 つのプロパティでその機能についての情報を公開する必要があります。 
  
 **PR_RESOURCE_METHODS**([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) 
  
 **PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md)) 
  
 **PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) 
  
状態オブジェクトを実装する方法の詳細については、[状態オブジェクトの実装](status-object-implementation.md)を参照してください。 ステータス オブジェクトの使い方の詳細については、[状態テーブルおよび状態オブジェクト](status-table-and-status-objects.md)を参照してください。
  

