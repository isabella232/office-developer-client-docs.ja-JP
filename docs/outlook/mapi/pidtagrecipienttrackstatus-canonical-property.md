---
title: PidTagRecipientTrackStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientTrackStatus
api_type:
- COM
ms.assetid: d619b5e7-2867-44fc-9b42-123bb1bf7bde
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 074bcf7c051b78bc32caf66502747e7fb1ab6b79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355287"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a>PidTagRecipientTrackStatus 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
出席者から返される応答状態を示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECIPIENT_TRACKSTATUS  <br/> |
|識別子:  <br/> |0x5fff  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |トランスポート受信者  <br/> |
   
## <a name="remarks"></a>解説

この値が設定されていない場合は、[なし] を指定する必要があります。 それ以外の場合は、次のいずれかである必要があります。
  
|**応答状態**|**値**|**説明**|
|:-----|:-----|:-----|
|[火炎なし]  <br/> |0x00000000  <br/> |このオブジェクトに対する応答は必要ありません。 これは、予定オブジェクトおよび会議の応答オブジェクトに当てはまります。  <br/> |
|仮承諾  <br/> |0x00000002  <br/> |出席者の会議オブジェクトのこの値は、出席者が会議出席依頼オブジェクトを仮承諾したことを示します。  <br/> |
|受付  <br/> |0x00000003  <br/> |出席者の会議オブジェクトのこの値は、出席者が会議出席依頼オブジェクトを承諾したことを示します。  <br/> |
|辞退  <br/> |0x00000004  <br/> |出席者が会議出席依頼オブジェクトを辞退したことを、出席者の会議オブジェクトのこの値で指定します。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
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

