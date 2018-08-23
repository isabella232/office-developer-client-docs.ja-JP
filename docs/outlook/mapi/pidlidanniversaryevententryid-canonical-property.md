---
title: PidLidAnniversaryEventEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAnniversaryEventEntryId
api_type:
- COM
ms.assetid: 177b2b87-7a06-4d53-8f03-5bec5632c2dd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3e146fea9332cde5751fa12d7f8ebb1e1bb763e7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572355"
---
# <a name="pidlidanniversaryevententryid-canonical-property"></a>PidLidAnniversaryEventEntryId 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
予定、連絡先の記念日を表すエントリの識別子を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidAnniversaryEventEID  <br/> |
|プロパティを設定します。  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x0000804E  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>注釈

**DispidAnniversaryEventEID**プロパティで指定された予定は、 **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md))、 **dispidContactLinkSearchKey** ([を使用して、この連絡先にリンクする必要があります。PidLidContactLinkSearchKey](pidlidcontactlinksearchkey-canonical-property.md))、および**dispidContactLinkName** ([PidLidContactLinkName](pidlidcontactlinkname-canonical-property.md)) のプロパティ] で詳細な[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)とします。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> プロパティは、連絡先、個人用配布リストの許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

