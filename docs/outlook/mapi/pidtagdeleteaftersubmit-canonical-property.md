---
title: PidTagDeleteAfterSubmit 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDeleteAfterSubmit
api_type:
- HeaderDef
ms.assetid: ba69a557-120c-4b1e-bbb7-0e901e7d1ebf
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d7b12e4b9d8f6c6a6df87c52783e1bd84222b727
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583500"
---
# <a name="pidtagdeleteaftersubmit-canonical-property"></a>PidTagDeleteAfterSubmit 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアント アプリケーションが提出後に関連付けられたメッセージを MAPI で削除する場合は TRUE を含む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DELETE_AFTER_SUBMIT  <br/> |
|識別子:  <br/> |0x0E01  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |MAPI 送信不可  <br/> |
   
## <a name="remarks"></a>注釈

クライアント アプリケーションは、このプロパティを **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId)](pidtagsentmailentryid-canonical-property.md)プロパティと一緒に使用して、送信後のメッセージの処理を制御します。 どちらか一方を設定する必要がありますが、両方を設定する必要はありません。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> コア メッセージ ストア オブジェクトに対して許容される操作を指定します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

