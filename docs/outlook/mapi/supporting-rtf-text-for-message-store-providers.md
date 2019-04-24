---
title: メッセージストアプロバイダーに RTF テキストをサポートする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: dc1d8a5e237b7b34f3a57e9789e03e2f16237764
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349617"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a>メッセージストアプロバイダーに RTF テキストをサポートする

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
一部のクライアントアプリケーションでは、ユーザーがメッセージでリッチテキスト形式 (RTF) のテキストを使用できます。 メッセージストアプロバイダーがメッセージ内の RTF テキストをサポートする必要がある場合は、 **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティに加えて、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティを処理する必要があります。 主に、これは、両方のプロパティを格納し、 **PR_BODY**が**PR_RTF_COMPRESSED**のテキストのプレーンテキストバージョンを含んでいることを確認することを意味します。 [rtfsync](rtfsync.md)関数は、このために役立ちます。 
  
メッセージストアオブジェクトの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティに設定して、 **PR_BODY**および PR_ に関して、メッセージストアプロバイダーから期待されることをクライアントに通知する2つのフラグがあります。 **** メッセージストア内のメッセージの RTF_COMPRESSED プロパティ。 STORE_RTF_OK フラグは、ストアが**PR_RTF_COMPRESSED**プロパティから**PR_BODY**プロパティの値を動的に生成できることを示します。これにより、クライアントを明示的に同期する負荷が軽減されます。 STORE_UNCOMPRESSED_RTF フラグは、メッセージストアプロバイダーが**PR_RTF_COMPRESSED**内の圧縮されていないデータをサポートできることを示します。
  
rtf テキストをサポートしていないメッセージストアプロバイダーは、rtf テキストをサポートするクライアントアプリケーションと適切に相互運用するために**PR_BODY**プロパティが変更されたときに、 **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) プロパティを削除する必要があります。. 
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

