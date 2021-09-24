---
title: PidTagSentMailEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSentMailEntryId
api_type:
- COM
ms.assetid: 8f14dc15-d7d7-4894-b6a8-0d589f576c42
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 50e80e5d9ae84b9e319fe19276e285cd1cb3ed8a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550436"
---
# <a name="pidtagsentmailentryid-canonical-property"></a>PidTagSentMailEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
送信後にメッセージを移動するフォルダーのエントリ識別子を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SENTMAIL_ENTRYID  <br/> |
|識別子:  <br/> |0x0E0A  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI 送信不可  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、多くの場合、クライアント **アプリケーションの** 標準の送信アイテム フォルダーである PR_IPM_SENTMAIL_ENTRYID ([PidTagIpmSentMailEntryId)](pidtagipmsentmailentryid-canonical-property.md)プロパティからコピーされます。
  
クライアント アプリケーションは、このプロパティを **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティと一緒に使用して、送信後のメッセージの処理を制御します。 どちらか一方を設定する必要がありますが、両方を設定する必要はありません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。
    
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

