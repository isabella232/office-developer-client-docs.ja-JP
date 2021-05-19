---
title: PidTagOriginalSentRepresentingEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingEntryId
api_type:
- COM
ms.assetid: ece3df57-47f3-4d27-854f-b511c920ac75
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: eaf91472794c5188a63897bccaa900c4882407bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341756"
---
# <a name="pidtagoriginalsentrepresentingentryid-canonical-property"></a>PidTagOriginalSentRepresentingEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
元のメッセージが送信されたメッセージング ユーザーのエントリ識別子を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINAL_SENT_REPRESENTING_ENTRYID  <br/> |
|識別子:  <br/> |0x005E  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、メッセージの元の送信者のアドレス プロパティの 1 つです。 会話スレッドで使用されます。
  
別のクライアントに代わってメッセージを送信するクライアント アプリケーションは、このプロパティをメッセージの最初の送信時に **PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId)](pidtagsentrepresentingentryid-canonical-property.md)プロパティの値に設定する必要があります。 一度設定した場合は、変更する必要はありません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
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

