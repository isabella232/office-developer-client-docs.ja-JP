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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 074bcf7c051b78bc32caf66502747e7fb1ab6b79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355287"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a>PidTagRecipientTrackStatus 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
出席者が返す応答の状態を示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RECIPIENT_TRACKSTATUS  <br/> |
|識別子:  <br/> |0x5FFF  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |トランスポート受信者  <br/> |
   
## <a name="remarks"></a>注釈

この値が設定されていない場合は、respNone と見なす必要があります。 それ以外の場合は、次のいずれかを指定する必要があります。
  
|**応答の状態**|**値**|**説明**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |このオブジェクトには応答は必要ありません。 これは、予定オブジェクトと会議の応答オブジェクトの場合です。  <br/> |
|respTentative  <br/> |0x00000002  <br/> |出席者の会議オブジェクトのこの値は、出席者が会議出席依頼オブジェクトを暫定的に受け入れるかどうかを示します。  <br/> |
|respAccepted  <br/> |0x00000003  <br/> |出席者の会議オブジェクトのこの値は、出席者が会議出席依頼オブジェクトを承諾したかどうかを示します。  <br/> |
|respDeclined  <br/> |0x00000004  <br/> |出席者の会議オブジェクトのこの値は、出席者が会議出席依頼オブジェクトを拒否したかどうかを示します。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
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

