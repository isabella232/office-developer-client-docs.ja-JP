---
title: メッセージ ストア プロバイダーの RTF テキストのサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: dc1d8a5e237b7b34f3a57e9789e03e2f16237764
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414215"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a>メッセージ ストア プロバイダーの RTF テキストのサポート

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
一部のクライアント アプリケーションでは、ユーザーはメッセージでリッチ テキスト形式 (RTF) テキストを使用できます。 メッセージ ストア プロバイダーがメッセージ内の RTF テキストをサポートする必要がある場合は、PR_BODY ([PidTagBody](pidtagbody-canonical-property.md)) プロパティに加えて **、PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティを処理する必要があります。  主に、これは両方のプロパティを格納し、PR_BODYにテキストのプレーン テキスト バージョンが含まれている **PR_RTF_COMPRESSED。** [RTFSync 関数](rtfsync.md)は、この目的に役立ちます。 
  
メッセージ ストア オブジェクトの **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)プロパティには、メッセージ ストア 内のメッセージの **PR_BODY** プロパティと **PR_RTF_COMPRESSED** プロパティに関してクライアントがメッセージ ストア プロバイダーから期待できることを通知する 2 つのフラグがあります。 STORE_RTF_OK フラグは、ストアが **PR_RTF_COMPRESSED** プロパティから **PR_BODY** プロパティの値を動的に生成し、クライアントが明示的に同期する負担を軽減できます。 [STORE_UNCOMPRESSED_RTF] フラグは、メッセージ ストア プロバイダーが、メッセージ ストア プロバイダーで圧縮されていないデータを **サポートPR_RTF_COMPRESSED。**
  
RTF テキストをサポートしないメッセージ ストア プロバイダーは **、RTF** テキストをサポートするクライアント アプリケーションと適切に相互運用するために **、PR_BODY** プロパティが変更された場合に PR_RTF_IN_SYNC ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) プロパティを削除する必要があります。 
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

