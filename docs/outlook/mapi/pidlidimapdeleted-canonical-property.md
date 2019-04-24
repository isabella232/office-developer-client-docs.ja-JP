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
ms.openlocfilehash: 790aa363522b9562f8f06c0806c87bba3816f566
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319944"
---
# <a name="pidlidimapdeleted-canonical-property"></a>PidLidImapDeleted 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
削除としてマークされているインターネットメールアクセスプロトコル (IMAP) アイテムを示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidImapDeleted  <br/> |
|プロパティセット:  <br/> |PSETID_Common  <br/> |
|ロング ID (LID):  <br/> |0x00008570  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |IMAP  <br/> |
   
## <a name="remarks"></a>解説

0以外の値に設定した場合、アイテムは削除対象としてマークされています。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]] 
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

