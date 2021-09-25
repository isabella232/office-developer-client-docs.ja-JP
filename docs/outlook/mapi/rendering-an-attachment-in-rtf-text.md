---
title: RTF テキストで添付ファイルをレンダリングする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 90e8c40833570927f488a053c7682af19bde9480
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609649"
---
# <a name="rendering-an-attachment-in-rtf-text"></a>RTF テキストで添付ファイルをレンダリングする

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
リッチ テキスト形式 (RTF) 対応のクライアントは、メッセージの **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティで次のエスケープ シーケンスを探して、RTF メッセージ テキストからレンダリングの位置情報を取得できます。
  
 `\objattph`
  
 **書式設定されたテキストでレンダリング情報を見つけるには**
  
1. **メッセージの添付ファイル テーブルにアクセスするには、IMessage::GetAttachmentTable** を呼び出します。 詳細については [、「IMessage::GetAttachmentTable」を参照してください](imessage-getattachmenttable.md)。
    
2. テーブルを -1 に等しくない行に制限 **PR_RENDERING_POSITIONプロパティ** 制限を作成します。 詳細については、「PR_RENDERING_POSITION **(** [PidTagRenderingPosition )」を参照してください](pidtagrenderingposition-canonical-property.md)。
    
3. **IMAPITable::Restrict を呼び出して** 制限を適用します。 詳細については [、「IMAPITable::Restrict」を参照してください](imapitable-restrict.md)。
    
4. **IMAPITable::SortTable を呼び出して** 添付ファイルを並べ替える。 詳細については [、「IMAPITable::SortTable」を参照してください](imapitable-sorttable.md)。
    
5. **IMAPITable::QueryRows を呼び出して、適切** な行を取得します。 詳細については [、「IMAPITable::QueryRows」を参照してください](imapitable-queryrows.md)。
    
6. メッセージの **IMAPIProp::OpenProperty** メソッドを呼び出して **、IStream** **インターフェイス** PR_RTF_COMPRESSEDを取得します。 詳細については [、「IMAPIProp::OpenProperty」および「PR_RTF_COMPRESSED」](imapiprop-openproperty.md) を **参照してください**。
    
7. ストリームをスキャンし、レンダリング プレースホルダーを探します  `\objattph` 。 このプレースホルダーに続く文字は、並べ替えたテーブル内の次の添付ファイルの場所です。
    

