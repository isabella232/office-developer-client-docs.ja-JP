---
title: ストア インデックスNotification-Basedについて
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2d00b0b65639786a561830ed50f555b17519aba9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592761"
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

