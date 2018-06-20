---
title: ストアの通知に基づくインデックスの作成について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b3685890-117c-9acc-e19f-cf22a349a088
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 338ae3c3c8d8b4037ab0c7b46916e45cf5a8ded2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799601"
---
# <a name="about-notification-based-store-indexing"></a>ストアの通知に基づくインデックスの作成について

  
  
**適用されます**: Outlook 
  
MAPI ストア プロバイダーは、ストアでの MAPI プロトコル ハンドラーのクロールとインデックスのメッセージかどうか、またはかどうか、ストアに通知を送信、インデクサー インデックスを作成するメッセージがある場合に指定できます。 後者し、呼ばれ通知ベースのインデックス作成、通知ベースのインデックス作成をサポートしているストアは、プッシュ型ストアとして、知られています。
  
**[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** プロパティのインデックス設定の通知に基づく**STORE_PUSHER_OK**フラグをサポートしているストア プロバイダーです。 MAPI プロトコル ハンドラー、またはクライアントは、ストアの特性を決定する**PR_STORE_SUPPORT_MASK**プロパティを取得できます。 
  
添付ファイル、フォルダー、またはインデックスを作成するメッセージがある場合、ストア プロバイダーは、MAPI (URL) オブジェクトを識別するインデックスを作成するを生成し、インデクサーに送信します。 この MAPI URL は Unicode でエンコードされてされ、MAPI プロトコル ハンドラー オブジェクトを一意に識別する必要があります。 MAPI Url の詳細については、[通知ベースのインデックス作成用に MAPI Url について](about-mapi-urls-for-notification-based-indexing.md)を参照してください。
  
インデクサー常にインデックスを作成できませんすべてのプッシュ型ストアのシャット ダウンが発生する前に、ためプッシュ型ストアがプッシュする必要のあるを保持する必要があります。 ストア プロバイダーは、インデックスを作成する必要のあるオブジェクトに通知を送信するときは、**[通知](notification.md)** の構造体の**ulEventType**メンバーに通知の種類の**fnevIndexing**を指定します。 **通知**の構造体のメンバー**情報**には、 **[EXTENDED_NOTIFICATION](extended_notification.md)** 構造体が含まれています。 ストア プロバイダーは、 **[PR_SEARCH_OWNER_ID](pidtagsearchownerid-canonical-property.md)** プロパティにはそのプロセスを識別します。 また、 [INDEX_SEARCH_PUSHER_PROCESS](index_search_pusher_process.md)構造で、プロセスを識別し、 **pbEventParameters** 、 **EXTENDED_NOTIFICATION**構造体のメンバーの一部としてこの情報を渡します。 プロセスがシャット ダウンまたはクラッシュした場合、MAPI プロトコル ハンドラーはすぐに検出して、プッシュ型ストアのインデックス作成を停止することになります。 
  
## <a name="see-also"></a>関連項目



[ストア API について](about-the-store-api.md)
  
[MAPI �萔](mapi-constants.md)

