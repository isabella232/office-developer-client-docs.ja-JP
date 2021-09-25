---
title: プレーン テキストで添付ファイルをレンダリングする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 72b447e9-b4f2-4557-baf5-0afefe463749
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 959716e6067f0eb4fd808c4ccacbd4ffb11db025
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591305"
---
# <a name="rendering-an-attachment-in-plain-text"></a>プレーン テキストで添付ファイルをレンダリングする

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テキスト形式でメッセージ内の添付ファイルをレンダリングするには、添付ファイルの **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) プロパティを取得し **、PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) プロパティのデータに適用します。 データを取得するには、次の **2 PR_RENDERING_POSITION。**
  
- メッセージの **IMessage::OpenAttach** メソッドを呼び出して添付ファイルを開き、添付ファイルの **IMAPIProp::GetProps** メソッドを呼び出して **PR_RENDERING_POSITION** プロパティを求める。 詳細については [、「IMessage::OpenAttach」](imessage-openattach.md) および [「IMAPIProp::GetProps」を参照してください](imapiprop-getprops.md)。
    
- メッセージの **IMessage::GetAttachmentTable** メソッドを呼び出して、添付ファイル テーブルにアクセスし、PR_RENDERING_POSITION プロパティ **を保持する列を取得** します。 この方法は常に望ましい方法です。 詳細については [、「IMessage::GetAttachmentTable」を参照してください](imessage-getattachmenttable.md)。
    
多くの RTF 対応メッセージ ストアは、クライアントがメッセージの **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティを要求するまで、PR_RENDERING_POSITION を計算しない点に注意してください。 この時間 **まで、PR_RENDERING_POSITION** は概算値を表します。 メッセージ ストア プロバイダーは、パフォーマンスを向上させる近似値をクライアントに提供できます。 
  
ファイルまたはバイナリ添付ファイルのレンダリングは、そのプロパティに **PR_ATTACH_RENDERING** されます。 添付ファイルから直接、または添付PR_ATTACH_RENDERINGファイルを取得した場合と同じ方法で、PR_RENDERING_POSITIONを取得することもできます。 この **PR_ATTACH_RENDERING、** 時間がかかりますが、最初の戦略の方が安全です。 一部のメッセージ ストア プロバイダーはテーブル列を 255 バイトに切り捨てるか、場合によっては 510 バイトに切り捨てるので **、PR_ATTACH_RENDERING** 列に完全なレンダリングが含まれているのを確認することは困難です。 添付ファイルから直接プロパティを取得すると、常に完了します。 
  
OLE 添付ファイルもメッセージ添付 **ファイルも設定** PR_ATTACH_RENDERING。 代わりに、OLE 1 添付ファイルのレンダリング情報がメッセージ テキスト ストリームに格納されます。 OLE 2 添付ファイルの場合は、ストレージ オブジェクトの特別な子ストリームに格納されます。 メッセージ添付ファイルのレンダリング情報は、フォーム マネージャーから利用できます。 
  
 **メッセージ添付ファイルのレンダリングを取得するには**
  
1. メッセージのメッセージ クラスを使用して、フォーム マネージャーにアクセスします。
    
2. フォーム マネージャーのプロパティに **PR_MINI_ICON** します。 詳細については、「PR_MINI_ICON **(** [PidTagMiniIcon )」を参照してください](pidtagminiicon-canonical-property.md)。
    

