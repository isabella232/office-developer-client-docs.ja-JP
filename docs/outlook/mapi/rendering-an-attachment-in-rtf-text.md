---
title: RTF テキスト形式での添付ファイルのレンダリング
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b2a1a23f073d05e85c8203826e3407c5ae193f19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280361"
---
# <a name="rendering-an-attachment-in-rtf-text"></a>RTF テキスト形式での添付ファイルのレンダリング

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
リッチテキスト形式 (rtf) 対応クライアントは、メッセージの**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティで次のエスケープシーケンスを検索することによって、rtf メッセージテキストからレンダリング位置情報を取得できます。
  
 `\objattph`
  
 **書式設定されたテキストでレンダリング情報を検索するには**
  
1. メッセージの添付ファイルテーブルにアクセスするには、 **IMessage:: getattachmenttable**を呼び出します。 詳細については、「 [IMessage:: getattachmenttable](imessage-getattachmenttable.md)」を参照してください。
    
2. **PR_RENDERING_POSITION**が-1 と等しくない行にテーブルを制限するプロパティ制限を構築します。 詳細については、「 **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))」を参照してください。
    
3. **IMAPITable:: Restrict**を呼び出して制限を適用します。 詳細については、「 [IMAPITable:: Restrict](imapitable-restrict.md)」を参照してください。
    
4. 呼び出し**IMAPITable:: sorttable**は、添付ファイルを並べ替えます。 詳細については、「 [IMAPITable:: sorttable](imapitable-sorttable.md)」を参照してください。
    
5. 必要な行を取得するには、 **IMAPITable:: QueryRows**を呼び出します。 詳細については、「 [IMAPITable:: QueryRows](imapitable-queryrows.md)」を参照してください。
    
6. メッセージの**imapiprop:: openproperty**メソッドを呼び出して、 **IStream**インターフェイスを使用して**PR_RTF_COMPRESSED**を取得します。 詳細については、「 [imapiprop:: openproperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**」を参照してください。
    
7. ストリームをスキャンして、レンダリングプレースホルダーを探し`\objattph`ます。 このプレースホルダーの後の文字は、並べ替えられたテーブルの次の添付ファイルの場所です。
    

