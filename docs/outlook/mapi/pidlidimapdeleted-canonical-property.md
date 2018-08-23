---
title: PidLidImapDeleted 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidImapDeleted
api_type:
- COM
ms.assetid: ee929306-8962-494d-bc47-9b4069f01267
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 59c0deefc680bdb5eafca681aedbee7fda29a273
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802002"
---
# <a name="pidlidimapdeleted-canonical-property"></a>PidLidImapDeleted 標準プロパティ

  
  
**適用対象**: Outlook 
  
削除対象としてマークされているインターネット メール アクセス プロトコル (IMAP) の項目を表します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidImapDeleted  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x00008570  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |IMAP  <br/> |
   
## <a name="remarks"></a>注釈

項目、0 以外の値に設定されている場合は、削除対象としてマークされています。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[MS OXPROPS] 
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

