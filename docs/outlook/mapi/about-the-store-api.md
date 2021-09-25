---
title: ストア API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: deba8ea99e53d3bc20267d4beb92952af14adfaa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592747"
---
# <a name="about-the-store-api"></a>ストア API について

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ストア API は、プロバイダーを格納するためのさまざまなストア機能を提供します。 次の定義、データ型、プロパティ、およびインターフェイスを提供します。
  
定義:
  
- [ストア API の定数](mapi-constants.md)
    
データ型:
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
名前付きプロパティ:
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[サーバー フォルダーのサイズの表示](display-server-folder-sizes-property.md)**
    
- **[会議の更新オプションを非表示にする](hide-meeting-update-option-property.md)**
    
- **[ストアの種類をプライベートにする](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> これらの名前付きプロパティによって提供される機能を必要としないストア プロバイダーは、それらを無視するだけで **、IMAPIProp** インターフェイスでのサポートを実装しません。 これらのプロパティは、Microsoft Outlook 2003 Service Pack 1 から提供されるので、以前のバージョンの Microsoft Outlook のストアに追加する効果はありません。 存在しない場合、または値が false の場合は無視 **されます**。 
  
プロパティ:
  
- **[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**
    
- **[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**
    
- **[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**
    
- **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**
    
インターフェイス
  
- **[IFolderSupport](ifoldersupportiunknown.md)**
    
- **[IMSCapabilities](imscapabilitiesiunknown.md)**
    
- **[IProxyStoreObject](iproxystoreobject.md)**
    
## <a name="registering-stores-for-indexing"></a>インデックス作成用のストアの登録

MAPI プロトコル ハンドラーは、検索Windowsインデックスを作成する必要があるストアのレジストリをチェックします。 インデックスを作成するストア プロバイダーは、レジストリに登録Windows必要があります。 Outlook 2013 または Outlook 2010 でのインデックス作成用のストア プロバイダーの登録の詳細については、「About [Registering Stores for Indexing](about-registering-stores-for-indexing.md)」を参照してください。
  
## <a name="indexing-stores"></a>Indexing Stores

MAPI ストア プロバイダーは、MAPI プロトコル ハンドラーがストア内のメッセージのクロールとインデックス作成を許可するか、インデックスを作成するメッセージがある場合にのみインデクサーに通知を送信できます。 通知ベースのインデックス作成の詳細については、「概要 [- ストア インデックスNotification-Basedを参照してください](about-notification-based-store-indexing.md)。
  

