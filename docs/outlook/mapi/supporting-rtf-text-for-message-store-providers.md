---
title: メッセージ ストア プロバイダーの rtf 形式のテキストをサポートしています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d7d64c8a7d4df4898502f4574ca879c736547b37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804070"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a>メッセージ ストア プロバイダーの rtf 形式のテキストをサポートしています。

  
  
**適用されます**: Outlook 
  
一部のクライアント アプリケーションは、メッセージでリッチ テキスト形式 (RTF) のテキストを使用するようにします。 メッセージは、メッセージ内の rtf 形式のテキストをサポートするためにプロバイダーのニーズを保存する場合 ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティだけでなく、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のプロパティを処理する必要があります。 主に、つまり、両方のプロパティを格納する**PR_BODY には** **PR_RTF_COMPRESSED**内のテキストのプレーン テキスト版が含まれていることを確認します。 [](rtfsync.md)関数は、この目的のために役立ちます。 
  
2 つのフラグ メッセージ ストア オブジェクトの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティで設定可能なメッセージ ストア プロバイダー **PR_BODY**と**PR_ の点から何を期待できることをクライアントに通知します。RTF_COMPRESSED**メッセージ ・ ストア内のメッセージのプロパティです。 STORE_RTF_OK フラグは、ことストアから生成できます**PR_BODY**プロパティの値、 **PR_RTF_COMPRESSED**プロパティ、動的にクライアントが明示的に同期する際の負担を軽減するを示します。 STORE_UNCOMPRESSED_RTF フラグは、メッセージ ストア プロバイダーが**PR_RTF_COMPRESSED**の非圧縮データをサポートできることを示します。
  
Rtf 形式のテキストをサポートしていないメッセージ ストア プロバイダーは rtf 形式のテキストをサポートしているクライアント アプリケーションと適切に相互運用するために**PR_BODY**プロパティが変更されたときに**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) のプロパティを削除する必要があります。. 
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

