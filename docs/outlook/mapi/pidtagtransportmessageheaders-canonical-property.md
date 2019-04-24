---
title: PidTagTransportMessageHeaders 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTransportMessageHeaders
api_type:
- COM
ms.assetid: 9f8e3f20-6454-4dfd-9b35-e0401abac6b3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7ad9048a19123b94c10afaddcbedb7f54e8fe477
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360761"
---
# <a name="pidtagtransportmessageheaders-canonical-property"></a>PidTagTransportMessageHeaders 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート固有のメッセージエンベロープ情報が保存されています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_TRANSPORT_MESSAGE_HEADERS、PR_TRANSPORT_MESSAGE_HEADERS_A、PR_TRANSPORT_MESSAGE_HEADERS_W  <br/> |
|識別子:  <br/> |0x007d  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |電子メール  <br/> |
   
## <a name="remarks"></a>解説

トランスポートプロバイダーは、受信メッセージのメッセージヘッダー情報を生成できます。
  
これらのプロパティは、トランスポートメッセージヘッダー情報を破棄するか、またはメッセージテキストに先頭に付加する方法を提供します。 クライアントは、情報を表示するかどうかを選択できます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトで許容されるプロパティと操作を指定します。
    
[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagBody 標準プロパティ](pidtagbody-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

