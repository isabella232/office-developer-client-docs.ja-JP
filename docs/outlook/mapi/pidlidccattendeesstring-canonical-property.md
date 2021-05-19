---
title: PidLidCcAttendeesString 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCcAttendeesString
api_type:
- COM
ms.assetid: 697d5c93-ec7f-4608-9866-9e249a093dbc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 12cdbfcc140fb5ea3bb15a2db93f3689923d9390
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344969"
---
# <a name="pidlidccattendeesstring-canonical-property"></a>PidLidCcAttendeesString 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
省略可能な出席者であるすべての送信可能な出席者の一覧が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidCCAttendeesString  <br/> |
|プロパティ セット:  <br/> |PSETID_Appointment  <br/> |
|長い ID (LID):  <br/> |0x0000823C  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |会議  <br/> |
   
## <a name="remarks"></a>注釈

各出席者の値は、PR_DISPLAY_NAME **のアドレス** 帳のプロパティ ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) です。 個別のエントリは、セミコロンで区切り、その後にスペースを指定する必要があります。 このプロパティは必須ではありません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

