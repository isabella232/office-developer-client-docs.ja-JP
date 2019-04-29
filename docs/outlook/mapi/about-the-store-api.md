---
title: ストア API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 166a8e60-e09d-7473-b61b-35d78a863192
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: fb9b0a4c8ac1a2f41a0fddcd746dba5fc4bae1a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405556"
---
# <a name="about-the-store-api"></a>ストア API について

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
store API は、ストアプロバイダーにさまざまなストア機能を提供します。 これにより、次の日、データ型、プロパティ、およびインターフェイスが提供されます。
  
定義
  
- [Store API の定数](mapi-constants.md)
    
データ型:
  
- **[INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)**
    
- **[MSCAP_SELECTOR](mscap_selector.md)**
    
名前付きプロパティ:
  
- **[ArchiveSourceSupportMask](archivesourcesupportmask.md)**
    
- **[CrawlSourceSupportMask](crawlsourcesupportmask.md)**
    
- **[サーバーフォルダーのサイズを表示する](display-server-folder-sizes-property.md)**
    
- **[会議の更新オプションを非表示にする](hide-meeting-update-option-property.md)**
    
- **[ストアの種類をプライベートにする](make-store-type-private-property.md)**
    
- **[NoFolderScan](nofolderscan.md)**
    
> [!NOTE]
> これらの名前付きプロパティによって提供される機能を必要としないストアプロバイダーは、単にそれらを無視して、 **imapiprop**インターフェイスでサポートを実装することはできません。 これらのプロパティは、microsoft outlook 2003 Service Pack 1 以降で提供されるため、以前のバージョンの microsoft outlook でストアに追加しても効果はありません。 存在しない場合、または値が**false**の場合は無視されます。 
  
プロパティ:
  
- **[PR_ADDITIONAL_REN_ENTRYIDS](pidtagadditionalrenentryids-canonical-property.md)**
    
- **[PR_PROVIDER_ITEMID](pidtagprovideritemid-canonical-property.md)**
    
- **[PR_PROVIDER_PARENT_ITEMID](pidtagproviderparentitemid-canonical-property.md)**
    
- **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)**
    
インターフェイス
  
- **[IFolderSupport](ifoldersupportiunknown.md)**
    
- **[imscapabilities](imscapabilitiesiunknown.md)**
    
- **[IProxyStoreObject](iproxystoreobject.md)**
    
## <a name="registering-stores-for-indexing"></a>インデックス作成のためのストアの登録

MAPI プロトコルハンドラーは、検索用にインデックスが必要なストアの Windows レジストリをチェックします。 インデックスを作成するストアプロバイダーは、Windows レジストリに登録する必要があります。 outlook 2013 または outlook 2010 でのインデックス作成のためのストアプロバイダーの登録の詳細については、「[インデックス作成のためのストア登録につい](about-registering-stores-for-indexing.md)て」を参照してください。
  
## <a name="indexing-stores"></a>インデックス作成ストア

mapi ストアプロバイダーでは、mapi プロトコルハンドラーでストア内のメッセージのクロールとインデックス作成を行うことができます。また、インデックスを作成するメッセージがある場合にのみ、インデクサーに通知を送信することもできます。 通知ベースのインデックス作成の詳細については、「[通知ベースのストアインデックス作成につい](about-notification-based-store-indexing.md)て」を参照してください。
  

