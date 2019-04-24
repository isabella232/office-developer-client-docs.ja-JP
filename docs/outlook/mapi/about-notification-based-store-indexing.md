---
title: 通知ベースのストアインデックス作成について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3dd551dd0c1ea229381e5dd01c5cf6fa04790c30
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322135"
---
# <a name="about-notification-based-store-indexing"></a>通知ベースのストアインデックス作成について

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
mapi ストアプロバイダーでは、mapi プロトコルハンドラーがストア内のメッセージをクロールしてインデックスを作成するか、インデックス付けするメッセージがある場合に、ストアがインデクサーに通知を送信するかどうかを指定できます。 後者は通知ベースのインデックス作成と呼ばれ、通知ベースのインデックスをサポートするストアは pusher ストアと呼ばれます。
  
通知ベースのインデックス処理をサポートするストアプロバイダーは、 **[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** プロパティの**STORE_PUSHER_OK**フラグを設定します。 MAPI プロトコルハンドラーまたはクライアントは、 **PR_STORE_SUPPORT_MASK**プロパティを取得してストアの特性を決定できます。 
  
添付ファイル、フォルダー、またはメッセージがインデックス化されるたびに、ストアプロバイダーは、インデックスを作成するオブジェクトを識別する MAPI Uniform resource Locator (URL) を生成し、それをインデクサーに送信します。 この mapi URL は Unicode でエンコードされ、mapi プロトコルハンドラーに対して一意にオブジェクトを識別する必要があります。 mapi url の詳細については、「[通知ベースのインデックス作成の mapi url につい](about-mapi-urls-for-notification-based-indexing.md)て」を参照してください。
  
pusher ストアでシャットダウンが発生する前に、インデクサーは常にすべてのインデックスを作成することはできないため、pusher ストアは、プッシュする必要のあるものを保持する必要があります。 ストアプロバイダーは、インデックスを必要とするオブジェクトについての通知を送信するときに、通知構造の**uleventtype**メンバーで通知**[](notification.md)** タイプ**fnevIndexing**を指定します。 **NOTIFICATION** 構造の **info** メンバーには、**[EXTENDED_NOTIFICATION](extended_notification.md)** 構造が含まれます。 ストアプロバイダーは、 **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** プロパティでプロセスを識別します。 また、 [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)構造体のプロセスを識別し、この情報を**EXTENDED_NOTIFICATION**構造の**p傾斜 entparameters**メンバーの一部として渡します。 プロセスがシャットダウンまたはクラッシュした場合、MAPI プロトコルハンドラーはすぐにそのことを検出し、pusher ストアのインデックス作成を停止できます。 
  
## <a name="see-also"></a>関連項目



[ストア API について](about-the-store-api.md)
  
[MAPI 定数](mapi-constants.md)

