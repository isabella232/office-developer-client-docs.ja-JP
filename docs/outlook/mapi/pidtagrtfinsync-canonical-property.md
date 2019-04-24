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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ed038faf44f350b041191373cf573e7e185337c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357877"
---
# <a name="pidtagrtfinsync-canonical-property"></a>PidTagRtfInSync 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティのテキストコンテンツが、このメッセージの**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティと同じである場合は、TRUE が含まれます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RTF_IN_SYNC  <br/> |
|識別子:  <br/> |0x0e1f  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |電子メール  <br/> |
   
## <a name="remarks"></a>解説

値 TRUE は、 **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティ、このメッセージのプレーンテキストバージョン、および**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティ (リッチテキスト形式 (RTF)) が同一であることを意味します。ただし、**PR_BODY**の空白スペースと**PR_RTF_COMPRESSED**の書式設定。 2つのバージョンのテキストは、同じシーケンスの同じ文字で構成されています。
  
値が FALSE の場合は、テキストコンテンツに対して2つのバージョンが同期されませんが、 [rtfsync](rtfsync.md)関数による同期が可能であることを意味します。 1つのバージョンが変更され、もう一方のバージョンにはがありません。 
  
値がない場合、2つのバージョンが存在しているか、存在していた場合は、同期できないことを意味します。 1つのバージョンが削除または変更されたため、同期を実行できなくなりました。
  
**PR_RTF_COMPRESSED**を変更したクライアントアプリケーションでは、このプロパティの値を FALSE に設定して同期を強制する必要があります。 RTF 対応のメッセージストアは、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)呼び出しの間に**rtfsync**を使用して同期を実行する必要があります。 RTF 対応クライアントは**PR_RTF_COMPRESSED**を読み取る前に**PR_RTF_IN_SYNC**の設定を確認し、必要に応じて**rtfsync**を最初に呼び出す必要があります。 
  
**PR_BODY**に空白以外の変更があった場合、メッセージストアは、同期を終了するために**PR_RTF_IN_SYNC**を削除する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

