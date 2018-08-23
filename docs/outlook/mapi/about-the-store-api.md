---
title: ストア API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: d72df30eab5fde4288b5feba1d7045da05117bde
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579376"
---
# <a name="about-the-store-api"></a>ストア API について

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
保存の API では、プロバイダーを格納するその他のストアの機能を提供します。 次の定義、データ型、プロパティ、およびインターフェイスを提供します。
  
定義
  
- [ストア API の定数](mapi-constants.md)
    
データ型:
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
名前付きプロパティ。
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[サーバーのフォルダーのサイズを表示します。](display-server-folder-sizes-property.md)**
    
- **[会議の更新] オプションを非表示にします。](hide-meeting-update-option-property.md)**
    
- **[ストアの種類のプライベート](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> これらの名前付きプロパティによって提供される機能のいずれかを必要としないストアのプロバイダーでは、単純に無視でき、 **IMAPIProp**インターフェイスのサポートを実装することができます。 これらのプロパティを提供するには、Microsoft Outlook 2003 Service Pack 1 で始まる、ためには、Microsoft Outlook の以前のバージョン ストアに追加することも効果がありません。 存在しない場合、またはその値が**false**の場合、無視されます。 
  
プロパティ:
  
- **[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**
    
- **[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**
    
- **[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**
    
- **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**
    
インターフェイス
  
- **[IFolderSupport](ifoldersupportiunknown.md)**
    
- **[IMSCapabilities](imscapabilitiesiunknown.md)**
    
- **[IProxyStoreObject](iproxystoreobject.md)**
    
## <a name="registering-stores-for-indexing"></a>インデックス作成のためのストアを登録します。

MAPI プロトコル ハンドラーでは、検索用のストアにインデックスを作成するための Windows レジストリをチェックします。 インデックスを作成するストア プロバイダーは、Windows レジストリに登録しなければなりません。 2013 の Outlook または Outlook 2010 のインデックス作成のためのストア プロバイダーの登録の詳細については、[ストアの登録について](about-registering-stores-for-indexing.md)を参照してください。
  
## <a name="indexing-stores"></a>ストアのインデックスを作成します。

MAPI ストア プロバイダーは、クロールとインデックスのストアにメッセージを MAPI プロトコル ハンドラーを許可するか、インデックスを作成するメッセージがある場合にのみ、インデクサーに対して通知を送信することできます。 通知に基づくインデックス作成の詳細については、 [About Notification-Based ストアのインデックス作成](about-notification-based-store-indexing.md)を参照してください。
  

