---
title: Rtf 形式のテキストの添付ファイルを表示します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cf22e360a0319a662c9b7dd31856dbb6eccec02a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803742"
---
# <a name="rendering-an-attachment-in-rtf-text"></a>Rtf 形式のテキストの添付ファイルを表示します。

  
  
**適用されます**: Outlook 
  
リッチ テキスト形 (式 RTF) に対応していないクライアントはメッセージの**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のプロパティで、次のエスケープ シーケンスを探すことで RTF メッセージ テキストのレンダリング位置の情報を取得することができます。
  
 `\objattph`
  
 **書式設定されたテキストのレンダリング情報を検索するには**
  
1. メッセージの添付ファイル テーブルにアクセスするのには**IMessage::GetAttachmentTable**を呼び出します。 詳細については、 [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)を参照してください。
    
2. **PR_RENDERING_POSITION** -1 と等しくないの行にテーブルを制限するプロパティの制限を作成します。 詳細については、 **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) を参照してください。
    
3. 制限を強制するのには**IMAPITable::Restrict**を呼び出します。 詳細については、 [IMAPITable::Restrict](imapitable-restrict.md)を参照してください。
    
4. 添付ファイルを並べ替えるには**IMAPITable::SortTable**を呼び出します。 詳細については、 [IMAPITable::SortTable](imapitable-sorttable.md)を参照してください。
    
5. 適切な行を取得するために**IMAPITable::QueryRows**を呼び出します。 詳細については、 [IMAPITable::QueryRows](imapitable-queryrows.md)を参照してください。
    
6. **PR_RTF_COMPRESSED**を**IStream**インターフェイスを取得するために、メッセージの**IMAPIProp::OpenProperty**メソッドを呼び出します。 詳細については、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md) 、 **PR_RTF_COMPRESSED**を参照してください。
    
7. レンダリングのプレース ホルダーを探して、ストリームをスキャンする`\objattph`。 このプレース ホルダーを次の文字は、並べ替えられたテーブルに次の添付ファイルの場所です。
    

