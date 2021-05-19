---
title: PidTagAttachmentFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachmentFlags
api_type:
- HeaderDef
ms.assetid: 42981aac-f9e7-45dd-91a2-15d9784f30aa
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d494f1f14daff75be55e910da56204ecb3dbcf83
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345802"
---
# <a name="pidtagattachmentflags-canonical-property"></a>PidTagAttachmentFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
この Attachment オブジェクトの特別な処理を示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACHMENT_FLAGS  <br/> |
|識別子:  <br/> |0x7FFD  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |メッセージの添付ファイル  <br/> |
   
## <a name="remarks"></a>注釈

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)で0x00000000メッセージおよび添付ファイル オブジェクト プロトコルを拡張する他のプロトコルによってオーバーライドされない限り、このプロトコルを使用する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
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

