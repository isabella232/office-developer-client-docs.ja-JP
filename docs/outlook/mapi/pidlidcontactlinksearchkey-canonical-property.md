---
title: PidLidContactLinkSearchKey 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactLinkSearchKey
api_type:
- COM
ms.assetid: 82d21d38-a6c6-4e12-85b1-8158b2f5cce7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 11e1bd22da480669f72768e5d75b637e1257b6d1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589351"
---
# <a name="pidlidcontactlinksearchkey-canonical-property"></a>PidLidContactLinkSearchKey 標準プロパティ

**適用されます**: Outlook 2013 |Outlook 2016 
  
このメッセージ オブジェクトにリンクされている連絡先の**SearchKeys**の一覧が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidContactLinkSearchKey  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x00008584  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>注釈

|**長さ (バイト単位)**|**説明**|**メモ**|
|:-----|:-----|:-----|
|2  <br/> |ContactEntryCount  <br/> |なし  <br/> |
|変数  <br/> |SearchKey データ  <br/> |ContactEntryCount 回繰り返されます  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目

- [MAPI プロパティ](mapi-properties.md) 
- [標準の MAPI プロパティ](mapi-canonical-properties.md)
- [標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
- [MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

