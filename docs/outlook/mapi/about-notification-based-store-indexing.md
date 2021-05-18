---
title: ストア インデックスNotification-Basedについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3dd551dd0c1ea229381e5dd01c5cf6fa04790c30
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409175"
---
# <a name="about-notification-based-store-indexing"></a>ストア インデックスNotification-Basedについて

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI ストア プロバイダーは、MAPI プロトコル ハンドラーがストア内のメッセージをクロールしてインデックスを作成するかどうか、またはインデックスを作成するメッセージがあるときにストアがインデクサーに通知を送信するかどうかを指定できます。 後者は通知ベースのインデックス作成と呼び、通知ベースのインデックス作成をサポートするストアはプッシュストアと呼ばれる。
  
通知ベースのインデックス作成をサポートするストア プロバイダーは、STORE_PUSHER_OK **プロパティに** PR_STORE_SUPPORT_MASK **[します。](pidtagstoresupportmask-canonical-property.md)** MAPI プロトコル ハンドラーまたはクライアントは、ストアの特性を **PR_STORE_SUPPORT_MASKプロパティを** 取得できます。 
  
インデックスを作成する添付ファイル、フォルダー、またはメッセージがある場合、ストア プロバイダーは、インデックスを作成するオブジェクトを識別する MAPI Uniform Resource Locator (URL) を生成し、インデクサーに送信します。 この MAPI URL は Unicode でエンコードされ、MAPI プロトコル ハンドラーに対してオブジェクトを一意に識別する必要があります。 MAPI URL の詳細については、「MAPI URL [for Notification-Basedを参照してください](about-mapi-urls-for-notification-based-indexing.md)。
  
プッシュ ストアでシャットダウンが発生する前に、インデクサーが常にすべてをインデックス付けできるとは限りないので、プッシュする必要がある項目をプシュター ストアで保持する必要があります。 ストア プロバイダーは、インデックスを作成する必要があるオブジェクトに関する通知を送信すると **[、NOTIFICATION](notification.md)** 構造体の **ulEventType** メンバーで通知の種類 **fnevIndexing** を指定します。 **NOTIFICATION** 構造の **info** メンバーには、**[EXTENDED_NOTIFICATION](extended_notification.md)** 構造が含まれます。 ストア プロバイダーは、PR_SEARCH_OWNER_ID プロパティ **[内のプロセスを識別](pidtagsearchownerid-canonical-property.md)** します。 また、INDEX_SEARCH_PUSHER_PROCESS 構造内のプロセス [](index_search_pusher_process.md)を識別し、この情報を EXTENDED_NOTIFICATION 構造体の **pbEventParameters** **メンバーの一部として渡** します。 プロセスがシャットダウンまたはクラッシュした場合、MAPI プロトコル ハンドラーは直ちにそれを検出し、プッカー ストアのインデックス作成を停止できます。 
  
## <a name="see-also"></a>関連項目



[ストア API について](about-the-store-api.md)
  
[MAPI 定数](mapi-constants.md)

