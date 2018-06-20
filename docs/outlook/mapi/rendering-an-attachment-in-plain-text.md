---
title: テキスト形式の添付ファイルを表示します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72b447e9-b4f2-4557-baf5-0afefe463749
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 38db1d18f240188c7566a57afa23291a307446dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803758"
---
# <a name="rendering-an-attachment-in-plain-text"></a>テキスト形式の添付ファイルを表示します。

  
  
**適用されます**: Outlook 
  
レンダリングするテキスト形式のメッセージで添付ファイル添付ファイルの**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) のプロパティを取得し、 **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) 内のデータに適用します。プロパティです。 **PR_RENDERING_POSITION**を取得する 2 とおりの方法があります。
  
- メッセージの**IMessage::OpenAttach**メソッドを呼び出すことによって、添付ファイルを開くし、 **PR_RENDERING_POSITION**プロパティの添付ファイルの**IMAPIProp::GetProps**メソッドを呼び出すことによって。 詳細については、 [IMessage::OpenAttach](imessage-openattach.md)および[IMAPIProp::GetProps](imapiprop-getprops.md)を参照してください。
    
- メソッドを呼び出してメッセージの**IMessage::GetAttachmentTable**を添付ファイル テーブルにアクセスし、 **PR_RENDERING_POSITION**プロパティを保持する列を取得します。 この方法は、常に推奨します。 詳細については、 [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)を参照してください。
    
RTF に対応していない多くのメッセージ ストアを計算しない**PR_RENDERING_POSITION**クライアントは、メッセージの**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) のプロパティを要求するまでに留意してください。 それまでは、 **PR_RENDERING_POSITION**は、通常、概算値を表します。 メッセージ ストア プロバイダーは、パフォーマンスを強化するために概算値をクライアントに提供できるのです。 
  
ファイルまたはバイナリ添付ファイルのレンダリングは、その**PR_ATTACH_RENDERING**プロパティに格納されます。 **PR_RENDERING_POSITION**を取得するのと同じ方法で**PR_ATTACH_RENDERING**を取得する選択がある: 添付ファイルや添付ファイル テーブルから直接。 **PR_ATTACH_RENDERING**、最初の方法のですより時間がかかる方が安全です。 メッセージ ストア プロバイダーの中では、255 バイト、または 510 バイトまでのいくつかの場合、テーブルの列を切り捨て、ためには、 **PR_ATTACH_RENDERING**列に完全なレンダリングが含まれていることを確認することは困難です。 添付ファイルから直接プロパティを検索する場合に常に完了となります。 
  
OLE もメッセージの添付ファイルは、 **PR_ATTACH_RENDERING**を設定します。 代わりに、OLE 1 の添付ファイルの表示については、メッセージのテキスト ストリームに格納されます。 OLE 2 の添付ファイルの記憶域オブジェクトの子の特別なストリームに格納されます。 メッセージの添付ファイルの情報を表示、フォーム マネージャーを通じて利用可能です。 
  
 **メッセージの添付ファイルのレンダリングを取得するには**
  
1. フォーム マネージャーにアクセスするのにには、メッセージのメッセージ クラスを使用します。
    
2. フォーム マネージャーの**PR_MINI_ICON**プロパティにアクセスします。 詳細については、 **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) を参照してください。
    

