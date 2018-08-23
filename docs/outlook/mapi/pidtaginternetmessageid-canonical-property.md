---
title: PidTagInternetMessageId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetMessageId
api_type:
- HeaderDef
ms.assetid: 5c93d00c-a199-4d45-9bf6-87bd2ffe4784
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ce5de883d28d7575a8abb83ec48454752ea7ba6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580482"
---
# <a name="pidtaginternetmessageid-canonical-property"></a>PidTagInternetMessageId 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
[RFC2822] で指定されているメッセージ ID] フィールドに対応します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_INTERNET_MESSAGE_ID、PR_INTERNET_MESSAGE_ID_A、PR_INTERNET_MESSAGE_ID_W  <br/> |
|識別子:  <br/> |0x1035  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、すべての電子メール メッセージに含める必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

