---
title: テキスト形式での添付ファイルのレンダリング
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72b447e9-b4f2-4557-baf5-0afefe463749
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 587736e7ca2f30468b169a33cea34927f857382c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410876"
---
# <a name="rendering-an-attachment-in-plain-text"></a>テキスト形式での添付ファイルのレンダリング

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テキスト形式のメッセージに添付ファイルを表示するには、添付ファイルの**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) プロパティを取得し、 **PR_ATTACH_RENDERING**のデータに適用します ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md))。プロパティ. **PR_RENDERING_POSITION**を取得するには、次の2つの方法があります。
  
- メッセージの**IMessage:: openattach**メソッドを呼び出して添付ファイルを開き、添付ファイルの**imapiprop:: GetProps**メソッドを呼び出して**PR_RENDERING_POSITION**プロパティを要求します。 詳細については、「 [IMessage:: openattach](imessage-openattach.md) and [imapiprop:: GetProps](imapiprop-getprops.md)」を参照してください。
    
- メッセージの**IMessage:: getattachmenttable**メソッドを呼び出して、その添付ファイルテーブルにアクセスし、 **PR_RENDERING_POSITION**プロパティを保持する列を取得します。 この方法は常に推奨されます。 詳細については、「 [IMessage:: getattachmenttable](imessage-getattachmenttable.md)」を参照してください。
    
RTF 対応メッセージストアの多くは、クライアントがメッセージの**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティを要求するまで**PR_RENDERING_POSITION**を計算しないことに注意してください。 その時点まで、 **PR_RENDERING_POSITION**は通常近似値を表します。 メッセージストアプロバイダーは、パフォーマンスを向上させるために概数値をクライアントに提供できます。 
  
ファイルまたはバイナリ添付ファイルのレンダリングは、 **PR_ATTACH_RENDERING**プロパティに格納されます。 **PR_RENDERING_POSITION**を取得した場合と同じ方法で**PR_ATTACH_RENDERING**を取得する方法として、添付ファイルまたは添付ファイルテーブルから直接取得する方法があります。 **PR_ATTACH_RENDERING**の場合、最初の戦略は時間がかかることもありますが、より安全です。 一部のメッセージストアプロバイダーでは、表の列が255バイトに切り捨てられるか、場合によっては510バイトで切り捨てられることがあるため、 **PR_ATTACH_RENDERING**列に完全なレンダリングが含まれていることを確認するのは困難です。 添付ファイルから直接プロパティを取得する場合は、常に完了します。 
  
OLE もメッセージ添付ファイルも**PR_ATTACH_RENDERING**に設定することはできません。 代わりに、OLE 1 添付ファイルのレンダリング情報は、メッセージテキストストリームに格納されます。 OLE 2 の添付ファイルの場合は、ストレージオブジェクトの特別な子ストリームに格納されます。 メッセージの添付ファイルのレンダリング情報は、フォームマネージャーから使用できます。 
  
 **メッセージの添付ファイルのレンダリングを取得するには**
  
1. フォームマネージャーにアクセスするには、メッセージのメッセージクラスを使用します。
    
2. フォームマネージャーの**PR_MINI_ICON**プロパティにアクセスします。 詳細については、「 **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md))」を参照してください。
    

