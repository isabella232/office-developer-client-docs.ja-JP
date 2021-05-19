---
title: PidTagRtfInSync 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfInSync
api_type:
- COM
ms.assetid: 443cc68e-7898-4285-a606-f916fcd18554
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ed038faf44f350b041191373cf573e7e185337c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357877"
---
# <a name="pidtagrtfinsync-canonical-property"></a>PidTagRtfInSync 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このメッセージの **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティのテキスト コンテンツが **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティと同じ場合は TRUE を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RTF_IN_SYNC  <br/> |
|識別子:  <br/> |0x0E1F  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |メール  <br/> |
   
## <a name="remarks"></a>注釈

値が TRUE の場合 **、PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティ、このメッセージのプレーン テキスト バージョン、および **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティであるリッチ テキスト形式 (RTF) バージョンは **、PR_BODY** の空白と PR_RTF_COMPRESSED の書式設定を除いて同 **一** であることを意味します。 2 つのバージョンのテキストは、同じシーケンス内の同じ文字で構成されます。
  
FALSE の値は、2 つのバージョンがテキスト コンテンツに対して同期されるのではなく [、RTFSync](rtfsync.md) 関数によって同期可能な状態を意味します。 1 つのバージョンが変更され、もう 1 つのバージョンが変更されていない。 
  
値を指定しない場合は、2 つのバージョン (両方が存在する場合、または存在していた場合) を同期できないことを意味します。 1 つのバージョンが削除または変更されたので、同期は行えなくなりました。
  
このプロパティを変更したクライアント **PR_RTF_COMPRESSED、** このプロパティに FALSE の値を設定して、強制的に同期する必要があります。 RTF 対応のメッセージ ストアは [、IMAPIProp::SaveChanges](imapiprop-savechanges.md)呼び出し中に **RTFSync** を使用して同期を実行する必要があります。 RTF 対応のクライアントは、データを読み取る前PR_RTF_IN_SYNC設定をPR_RTF_COMPRESSED、必要に **応** じて **RTFSync** を最初に呼び出す必要があります。 
  
空白 **PR_BODY** に変更があった場合、メッセージ ストアは同期を終了するために **PR_RTF_IN_SYNC削除する** 必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

